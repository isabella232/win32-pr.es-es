---
description: La información de secuenciación y aplicabilidad de revisiones que devuelve la función MsiExtractPatchXMLData o el método ExtractPatchXMLData tiene el formato de un blob XML que contiene los elementos y atributos identificados en este tema.
ms.assetid: ea40ed1d-1ef9-44f3-8ae8-3d854e308a49
title: Extracción de información de revisión como XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0574d953609b467c42467853f540dc85c9c24a31c07b3b3d006eaa6633472d53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821685"
---
# <a name="extracting-patch-information-as-xml"></a>Extracción de información de revisión como XML

La información de secuenciación y aplicabilidad de revisiones que devuelve la función [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) o el método [**ExtractPatchXMLData**](installer-extractpatchxmldata.md) tiene el formato de un blob XML que contiene los elementos y atributos identificados en este tema. El blob XML se puede proporcionar a [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) y [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) en lugar del archivo de revisión completo.

-   El elemento MsiPatch es el elemento superior del blob XML y contiene información sobre la revisión.

    El atributo SchemaVersion especifica la versión de la definición de esquema. MSIPatchApplicability.xsd especifica el esquema y la versión actual del esquema es 1.0.0.0. El valor del atributo PatchGUID es el código de revisión GUID del paquete [](summary-information-stream.md) de revisión obtenido de la propiedad [**Resumen**](revision-number-summary.md) del número de revisión en el flujo de información de resumen de la revisión. MinMsiVersion es la versión mínima del instalador de Windows necesario para instalar la revisión obtenida de la propiedad [**Resumen de**](word-count-summary.md) recuento de palabras.

-   El elemento TargetProduct es un elemento contenedor para obtener información sobre una aplicación a la que se dirige una revisión.

    Puede haber varios elementos TargetProduct si la revisión se puede aplicar a varias aplicaciones. La información del elemento TargetProduct se extrae de las transformaciones incrustadas dentro de la revisión.

-   El elemento TargetProductCode contiene el valor de la [**propiedad ProductCode**](productcode.md) de la aplicación de destino antes de aplicar la revisión.

    Puede haber varios elementos TargetProductCode si la revisión se puede aplicar a varias aplicaciones.

-   El elemento UpdatedProductCode contiene el GUID del código de producto de la aplicación de destino después de aplicar la revisión.

    Este elemento solo está presente si la revisión cambia el valor de la [**propiedad ProductCode.**](productcode.md) Una revisión que cambia **ProductCode** se conoce como [actualización principal.](major-upgrades.md)

-   El elemento TargetVersion contiene la [**propiedad ProductVersion**](productversion.md) de la aplicación de destino antes de aplicar la revisión.
-   El elemento UpdateVersion contiene el valor de la [**propiedad ProductVersion**](productversion.md) de la aplicación de destino después de aplicar la revisión.

    Este elemento solo está presente si la revisión cambia el valor de la [**propiedad ProductVersion.**](productversion.md) El blob XML para una revisión que implementa una [actualización pequeña](small-updates.md), también denominada QFE, no incluirá este elemento. El blob XML para una revisión que implementa una actualización secundaria, también denominada Service Pack, incluirá este elemento.

-   El elemento TargetLanguage contiene el valor de la [**propiedad ProductLanguage**](productlanguage.md) de la aplicación de destino antes de aplicar la revisión.
-   El elemento UpdatedLanguages contiene el valor de la [**propiedad ProductLanguage**](productlanguage.md) después de aplicar la revisión.
-   El elemento UpgradeCode contiene el valor de la [**propiedad UpgradeCode**](upgradecode.md) de la aplicación de destino.
-   El elemento ObsoletedPatch contiene los códigos de revisión (GUID) de las revisiones especificadas como obsoletas por esta revisión.

    La lista de revisiones obsoletas se obtiene del resumen del número [**de**](revision-number-summary.md) revisión en el flujo [de información de resumen](summary-information-stream.md) de la revisión.

-   El elemento SequenceData contiene información de secuenciación de revisiones para la revisión.

    Puede haber varios elementos SequenceData en el blob XML. Cada elemento SequenceData contiene la información de una fila de la [tabla MsiPatchSequence](msipatchsequence-table.md) de la revisión. El elemento SequenceData contiene un subelemento ProductCode, Sequence y Attributes para la información de los campos correspondientes de la tabla MsiPatchSequence. Consulte la [sección tabla MsiPatchSequence](msipatchsequence-table.md) para obtener una descripción de cada campo.

## <a name="extracting-applicability-information"></a>Extracción de información de aplicabilidad

En el ejemplo siguiente se muestra cómo extraer la información de aplicabilidad de una revisión del instalador de Windows (archivo .msp) [**mediante MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa). El blob XML extraído se basa en la definición de esquema de MSIPatchApplicability.xsd y se devuelve a szXMLData.


```C++
#include <windows.h>
#include <msi.h>

#pragma comment( lib, "msi.lib" )

void main()
{
     TCHAR szPatchPath[] = TEXT("c:\\scratch\\RTM-RTMQFE.msp");
    TCHAR* szXMLData = NULL;
    DWORD cchXMLData = 0;

    UINT uiStatus = ERROR_SUCCESS;

    // Determine size of XML blob buffer.
    if (ERROR_SUCCESS == (uiStatus = MsiExtractPatchXMLData(szPatchPath, 
         /*dwReserved: must be 0*/ 0, szXMLData, &cchXMLData)))
    {
        // cchXMLData now includes size of szXMLData in characters not including terminating NULL
        ++cchXMLData;

        szXMLData = new TCHAR[cchXMLData];
        if (ERROR_SUCCESS == (uiStatus = MsiExtractPatchXMLData(szPatchPath, 
            /*dwReserved: must be 0*/ 0, szXMLData, &cchXMLData)))
        {
            //
            // szXMLData now contains the XML patch applicability blob. This could be
            // provided to MsiDetermineApplicablePatches or MsiDeterminePatchSequence in the
            // proper format to evaluate patch applicability.
            //

        }

        delete [] szXMLData;
        szXMLData = NULL;
    }
}
```



En el ejemplo siguiente se muestra cómo extraer la información de aplicabilidad de un archivo Windows Installer Patch (archivo .msp) en formato XML. El blob XML extraído se basa en la definición de esquema de MSIPatchApplicability.xsd y se devuelve en strPatchXML.

``` syntax
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")
strPatchXML = installer.ExtractPatchXMLData("c:\example\patch.msp")
```

## <a name="patch-applicability-schema-definition"></a>Definición de esquema de aplicabilidad de revisiones

Copie el texto siguiente en Bloc de notas u otro editor de texto para crear el archivo de definición de esquema para la información de aplicabilidad de revisiones en el blob XML. Asigne a este archivo el nombre MSIPatchApplicability.XSD.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema id="Applicability" 
    targetNamespace="https://www.microsoft.com/msi/patch_applicability.xsd" 
    elementFormDefault="qualified" 
    xmlns="https://www.microsoft.com/msi/patch_applicability.xsd" 
    xmlns:mstns="https://www.microsoft.com/msi/patch_applicability.xsd" 
    xmlns:xs="https://www.w3.org/2001/XMLSchema">
    
    <xs:element name="MsiPatch">
        <xs:complexType>
            <xs:sequence>
                <xs:element name="TargetProduct" minOccurs="1" maxOccurs="unbounded">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element name="TargetProductCode" type="ValidateGUID" />
                            <xs:element name="UpdatedProductCode" type="GUID" minOccurs="0" maxOccurs="1" />
                            <xs:element name="TargetVersion" type="ValidateVersion" />
                            <xs:element name="UpdatedVersion" type="Version" minOccurs="0" maxOccurs="1" />
                            <xs:element name="TargetLanguage" type="ValidateLanguage" />
                            <xs:element name="UpdatedLanguages" type="intList" minOccurs="0" maxOccurs="1" />
                            <xs:element name="UpgradeCode" type="ValidateGUID" />
                            <xs:element name="UpdatedUpgradeCode" type="GUID" minOccurs="0" maxOccurs="1" />
                        </xs:sequence>
                        <xs:attribute name="MinMsiVersion" type="xs:int" />
                    </xs:complexType>
                </xs:element>
                <xs:element name="TargetProductCode" type="GUID" minOccurs="1" maxOccurs="unbounded" />
                <xs:element name="ObsoletedPatch" minOccurs="0" maxOccurs="unbounded" type="GUID" />
                <xs:element name="SequenceData" minOccurs="0" maxOccurs="unbounded">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element name="PatchFamily" type="Identifier" />
                            <xs:element name="ProductCode" type="GUID" minOccurs="0" maxOccurs="1" />
                            <xs:element name="Sequence" type="Version" />
                            <xs:element name="Attributes" type="xs:int" minOccurs="0" maxOccurs="1" />
                        </xs:sequence>
                    </xs:complexType>
                </xs:element>
            </xs:sequence>
            <xs:attribute name="SchemaVersion" type="Version" />
            <xs:attribute name="PatchGUID" type="GUID" />
            <xs:attribute name="MinMsiVersion" type="xs:int" />
            <xs:attribute name="TargetsRTM" type="xs:boolean" use="optional" />
        </xs:complexType>
    </xs:element>
    <xs:simpleType name="GUID">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[0-9A-Fa-f]{8}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{12}\}" />
        </xs:restriction>
    </xs:simpleType>
    <xs:simpleType name="Version">
        <xs:restriction base="xs:string">
            <xs:pattern value="[0-9]{1,5}(\.[0-9]{1,5}){0,3}" />
        </xs:restriction>
    </xs:simpleType>
    <xs:complexType name="ValidateGUID">
        <xs:simpleContent>
            <xs:extension base="GUID">
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:complexType name="ValidateVersion">
        <xs:simpleContent>
            <xs:extension base="Version">
                <xs:attribute name="ComparisonType">
                    <xs:simpleType>
                        <xs:restriction base="xs:string">
                            <xs:enumeration value="LessThan" />
                            <xs:enumeration value="LessThanOrEqual" />
                            <xs:enumeration value="Equal" />
                            <xs:enumeration value="GreaterThanOrEqual" />
                            <xs:enumeration value="GreaterThan" />
                            <xs:enumeration value="None" />
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
                <xs:attribute name="ComparisonFilter">
                    <xs:simpleType>
                        <xs:restriction base="xs:string">
                            <xs:enumeration value="Major" />
                            <xs:enumeration value="MajorMinor" />
                            <xs:enumeration value="MajorMinorUpdate" />
                            <xs:enumeration value="None" />
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:complexType name="ValidateLanguage">
        <xs:simpleContent>
            <xs:extension base="xs:int">
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:simpleType name="intList">
        <xs:list itemType="xs:int" />
    </xs:simpleType>
    <xs:simpleType name="Identifier">
        <xs:restriction base="xs:string">
            <xs:pattern value="[_a-zA-Z][_a-zA-Z0-9\.]*" />
        </xs:restriction>
    </xs:simpleType>
</xs:schema>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ExtractPatchXMLData**](installer-extractpatchxmldata.md)
</dt> <dt>

[**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
</dt> <dt>

[**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
</dt> <dt>

[**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> </dl>

 

 



