# ABAP-CDS

Repositório para estudos.

CDS com publish: true, deve-se adaptar o arquivo "manifest.json" conforme abaixo

        "dataSources": {
            "mainService": {
                "uri": "/sap/opu/odata/sap/<NOME DA CDS>",
                "type": "OData",
                "settings": {
                    "odataVersion": "2.0",
                    "localUri": "localService/metadata.xml",
                    "annotations": ["secondaryService"] " (+)
                }
            }," (+) >>
            "secondaryService": {
                "uri": "/sap/opu/odata/IWFND/CATALOGSERVICE;v=2/Annotations(TechnicalName='<NOME DA ANNOTATION>_VAN',Version='0001')/$value",
                "type": "ODataAnnotation"
            }" (+) <<
        },
