# Open Refine Template for Thompson Brothers Remediation


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
{{if(isBlank(cells['adminDB'].value), '', '<identifier type="local">' + cells['adminDB'].value + '</identifier>')}}
<identifier type="pid">{{cells['PID'].value}}</identifier>
{{if(isBlank(cells['mcclung_identifier'].value), '', '<identifier type="photograph number">' + cells['mcclung_identifier'].value + '</identifier>')}}
<titleInfo><title>{{cells['title'].value}}</title></titleInfo>
{{if(isBlank(cells['abstract'].value), '', '<abstract>' + cells['abstract'].value + '</abstract>')}}
{{if(isBlank(cells['abstract2'].value), '', '<abstract>' + cells['abstract2'].value + '</abstract>')}}
{{if(isBlank(cells['abstract3'].value), '', '<abstract>' + cells['abstract3'].value + '</abstract>')}}
<name authority="naf" valueURI="{{cells['name_URI'].value}}"><namePart>{{cells['name'].value}}</namePart><role>
<roleTerm type="text" authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/pht">Photographer</roleTerm></role></name>
<originInfo><dateCreated>{{cells['date'].value}}</dateCreated>{{if(isBlank(cells['date_edtf'].value), '', '<dateCreated encoding="edtf">' + cells['date_edtf'].value + '</dateCreated>')}}
{{if(isBlank(cells['date_start_edtf'].value), '', '<dateCreated encoding="edtf" point="start">' + cells['date_start_edtf'].value + '</dateCreated><dateCreated encoding="edtf" point="end">' + cells['date_end_edtf'].value + '</dateCreated>')}}
</originInfo>
<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form>
{{if(isBlank(cells['form2'].value), '', '<form authority="aat" valueURI="' + cells['form2_URI'].value + '">' + cells['form2'].value + '</form>')}}
</physicalDescription>
{{if(isBlank(cells['subject_topic'].value), '', '<subject authority="lcsh" valueURI="' + if(isBlank(cells['subject_topic_URI'].value), '', cells['subject_topic_URI'].value) + '"><topic>' + cells['subject_topic'].value + '</topic></subject>')}} 
{{if(isBlank(cells['note'].value), '', '<note>' + cells['note'].value + '</note>')}}
{{if(isBlank(cells['note2'].value), '', '<note>' + cells['note2'].value + '</note>')}}
{{if(isBlank(cells['subject_topic'].value), '', '<subject' + if(isBlank(cells['subject_topic_URI'].value), '', ' authority="lcsh" valueURI="' + cells['subject_topic_URI'].value + '"') + '><topic>' + cells['subject_topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject'].value), '', '<subject' + if(isBlank(cells['subject_uri'].value), '', ' authority="lcsh" valueURI="' + cells['subject_uri'].value + '"') + '><topic>' + cells['subject'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject4'].value), '', '<subject' + if(isBlank(cells['subject4_uri'].value), '', ' authority="lcsh" valueURI="' + cells['subject4_uri'].value + '"') + '><topic>' + cells['subject4'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject6'].value), '', '<subject' + if(isBlank(cells['subject6_uri'].value), '', ' authority="lcsh" valueURI="' + cells['subject6_uri'].value + '"') + '><topic>' + cells['subject6'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_name'].value), '', '<subject' + if(isBlank(cells['subject_name_uri'].value), '', ' authority="naf" valueURI="' + cells['subject_name_uri'].value + '"') + '><name><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name2'].value), '', '<subject' + if(isBlank(cells['subject_name2_uri'].value), '', ' authority="naf" valueURI="' + cells['subject_name2_uri'].value + '"') + '><name><namePart>' + cells['subject_name2'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_geographic_name'].value), '', '<subject' + if(isBlank(cells['subject_geographic_uri'].value), '', ' authority="geonames" valueURI="' + cells['subject_geographic_uri'].value + '"') + '><geographic>' + cells['subject_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}
{{if(isBlank(cells['subject_geographic2_name'].value), '', '<subject' + if(isBlank(cells['subject_geographic2_uri'].value), '', ' authority="geonames" valueURI="' + cells['subject_geographic2_uri'].value + '"') + '><geographic>' + cells['subject_geographic2_name'].value + '</geographic>' + if(isBlank(cells['subject_geographic2_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_geographic2_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}
{{if(isBlank(cells['subject_geographic3_name'].value), '', '<subject' + if(isBlank(cells['subject_geographic3_uri'].value), '', ' authority="geonames" valueURI="' + cells['subject_geographic3_uri'].value + '"') + '><geographic>' + cells['subject_geographic3_name'].value + '</geographic>' + if(isBlank(cells['subject_geographic3_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_geographic3_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}
{{if(isBlank(cells['subject_geographic4_name'].value), '', '<subject' + if(isBlank(cells['subject_geographic4_uri'].value), '', ' authority="geonames" valueURI="' + cells['subject_geographic4_uri'].value + '"') + '><geographic>' + cells['subject_geographic4_name'].value + '</geographic>' + if(isBlank(cells['subject_geographic4_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_geographic4_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}
{{if(isBlank(cells['subject_blanket'].value), '', '<subject' + if(isBlank(cells['subject_blanket_URI'].value), '', ' authority="lcsh" valueURI="' + cells['subject_blanket_URI'].value + '"') + '><geographic>' + cells['subject_blanket'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_geographic_lcsh'].value), '', '<subject' + if(isBlank(cells['subject_geographic_lcsh_URI'].value), '', ' authority="lcsh" valueURI="' + cells['subject_geographic_lcsh_URI'].value + '"') + '><geographic>' + cells['subject_geographic_lcsh'].value + '</geographic></subject>')}}
<typeOfResource>still image</typeOfResource>
{{if(isBlank(cells['mcclung_uri'].value), '', '<relatedItem @type="original"><location><url>' + cells['mcclung_uri'].value + '</url></location></relatedItem>')}}
<relatedItem displayLabel="Project" type="host"><titleInfo><title>Thompson Brothers Photograph Collection</title></titleInfo></relatedItem>
{{if(isBlank(cells['archival_collection'].value), '', '<relatedItem displayLabel="Collection" type="host"><titleInfo><title>' + cells['archival_collection'].value + '</title></titleInfo><identifier>' + cells['archival_identifier'].value + '</identifier><location></location></relatedItem>')}}
<location><physicalLocation valueURI="{{cells['physicalLocation_URI'].value}}">{{cells['physicalLocation'].value}}</physicalLocation></location>
<recordInfo><recordContentSource valueURI="{{cells['physicalLocation_URI'].value}}">{{cells['physicalLocation'].value}}</recordContentSource></recordInfo>
<accessCondition type="use and reproduction" xlink:href="http://rightsstatements.org/vocab/InC/1.0/">In Copyright</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```