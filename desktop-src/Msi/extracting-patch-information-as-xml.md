---
description: La secuencia de revisión y la información de aplicabilidad que devuelve la función MsiExtractPatchXMLData o el método ExtractPatchXMLData se encuentran en el formato de un BLOB XML que contiene los elementos y atributos que se identifican en este tema.
ms.assetid: ea40ed1d-1ef9-44f3-8ae8-3d854e308a49
title: Extraer información de revisión como XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e1e594d3ff2870ca1aaf87245c537045f95d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155525"
---
# <a name="extracting-patch-information-as-xml"></a>Extraer información de revisión como XML

La secuencia de revisión y la información de aplicabilidad que devuelve la función [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) o el método [**ExtractPatchXMLData**](installer-extractpatchxmldata.md) se encuentran en el formato de un BLOB XML que contiene los elementos y atributos que se identifican en este tema. El BLOB XML se puede proporcionar a [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) y [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) en lugar del archivo de revisión completo.

-   El elemento MsiPatch es el elemento superior del BLOB XML y contiene información acerca de la revisión.

    El atributo SchemaVersion especifica la versión de la definición de esquema. MSIPatchApplicability. xsd especifica el esquema y la versión del esquema actual es 1.0.0.0. El valor del atributo PatchGUID es el código de revisión GUID para el paquete de revisión Obtenido de la propiedad [**Resumen del número de revisión**](revision-number-summary.md) en el flujo de información de [Resumen](summary-information-stream.md) de la revisión. MinMsiVersion es la versión mínima de la Windows Installer necesaria para instalar la revisión obtenida de la propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) .

-   El elemento TargetProduct es un elemento contenedor para obtener información sobre una aplicación de destino de una revisión.

    Puede haber varios elementos TargetProduct si la revisión puede aplicarse a varias aplicaciones. La información del elemento TargetProduct se extrae de las transformaciones que se incrustan dentro de la revisión.

-   El elemento TargetProductCode contiene el valor de la propiedad [**ProductCode**](productcode.md) de la aplicación de destino antes de que se aplique la revisión.

    Puede haber varios elementos TargetProductCode si la revisión puede aplicarse a varias aplicaciones.

-   El elemento UpdatedProductCode contiene el GUID del código de producto de la aplicación de destino una vez aplicada la revisión.

    Este elemento solo está presente si la revisión cambia el valor de la propiedad [**ProductCode**](productcode.md) . Una revisión que cambia el **ProductCode** se conoce como una [actualización principal](major-upgrades.md).

-   El elemento TargetVersion contiene la propiedad [**ProductVersion**](productversion.md) de la aplicación de destino antes de que se aplique la revisión.
-   El elemento UpdateVersion contiene el valor de la propiedad [**ProductVersion**](productversion.md) de la aplicación de destino después de aplicar la revisión.

    Este elemento solo está presente si la revisión cambia el valor de la propiedad [**ProductVersion**](productversion.md) . El BLOB XML de una revisión que implementa una [pequeña actualización](small-updates.md), también conocida como QFE, no incluirá este elemento. El BLOB XML de una revisión que implementa una actualización secundaria, también conocida como Service Pack, incluirá este elemento.

-   El elemento TargetLanguage contiene el valor de la propiedad [**ProductLanguage**](productlanguage.md) de la aplicación de destino antes de que se aplique la revisión.
-   El elemento UpdatedLanguages contiene el valor de la propiedad [**ProductLanguage**](productlanguage.md) una vez aplicada la revisión.
-   El elemento UpgradeCode contiene el valor de la propiedad [**UpgradeCode**](upgradecode.md) de la aplicación de destino.
-   El elemento ObsoletedPatch contiene los códigos de revisión (GUID) de las revisiones que se especifican como obsoletas en esta revisión.

    La lista de revisiones obsoletas se obtiene del [**Resumen de número de revisión**](revision-number-summary.md) en el [flujo de información de Resumen](summary-information-stream.md) de la revisión.

-   El elemento SequenceData contiene información de secuencia de revisión para la revisión.

    Puede haber varios elementos SequenceData en el BLOB XML. Cada elemento SequenceData contiene la información de una fila de la [tabla MsiPatchSequence](msipatchsequence-table.md) de la revisión. El elemento SequenceData contiene un subelemento ProductCode, Sequence y Attributes para la información de los campos correspondientes de la tabla MsiPatchSequence. Vea la sección de la [tabla MsiPatchSequence](msipatchsequence-table.md) para obtener una descripción de cada campo.

## <a name="extracting-applicability-information"></a>Extraer información de aplicabilidad

En el ejemplo siguiente se muestra cómo extraer la información de aplicabilidad de una revisión de Windows Installer (archivo. msp) mediante [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa). El BLOB XML extraído se basa en la definición de esquema de MSIPatchApplicability. xsd y se devuelve a szXMLData.


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



En el ejemplo siguiente se muestra cómo extraer la información de aplicabilidad de una revisión de Windows Installer (archivo. msp) en formato XML. El BLOB XML extraído se basa en la definición de esquema de MSIPatchApplicability. xsd y se devuelve en strPatchXML.

``` syntax
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")
strPatchXML = installer.ExtractPatchXMLData("c:\example\patch.msp")
```

## <a name="patch-applicability-schema-definition"></a>Definición del esquema de aplicabilidad de revisiones

Copie el siguiente texto en el Bloc de notas o en otro editor de texto para crear el archivo de definición de esquema para la información de aplicabilidad de la revisión en el BLOB XML. Asigne a este archivo el nombre MSIPatchApplicability. XSD.

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

 

 



