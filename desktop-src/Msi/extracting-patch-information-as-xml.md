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
# <a name="extracting-patch-information-as-xml"></a><span data-ttu-id="cd60b-103">Extraer información de revisión como XML</span><span class="sxs-lookup"><span data-stu-id="cd60b-103">Extracting Patch Information as XML</span></span>

<span data-ttu-id="cd60b-104">La secuencia de revisión y la información de aplicabilidad que devuelve la función [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) o el método [**ExtractPatchXMLData**](installer-extractpatchxmldata.md) se encuentran en el formato de un BLOB XML que contiene los elementos y atributos que se identifican en este tema.</span><span class="sxs-lookup"><span data-stu-id="cd60b-104">The patch sequencing and applicability information that is returned by the [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) function or the [**ExtractPatchXMLData**](installer-extractpatchxmldata.md) method is in the format of an XML blob that contains the elements and attributes that are identified in this topic.</span></span> <span data-ttu-id="cd60b-105">El BLOB XML se puede proporcionar a [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) y [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) en lugar del archivo de revisión completo.</span><span class="sxs-lookup"><span data-stu-id="cd60b-105">The XML blob can be provided to [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) and [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) instead of the full patch file.</span></span>

-   <span data-ttu-id="cd60b-106">El elemento MsiPatch es el elemento superior del BLOB XML y contiene información acerca de la revisión.</span><span class="sxs-lookup"><span data-stu-id="cd60b-106">The MsiPatch element is the top element of the XML blob, and contains information about the patch.</span></span>

    <span data-ttu-id="cd60b-107">El atributo SchemaVersion especifica la versión de la definición de esquema.</span><span class="sxs-lookup"><span data-stu-id="cd60b-107">The SchemaVersion attribute specifies the version of the schema definition.</span></span> <span data-ttu-id="cd60b-108">MSIPatchApplicability. xsd especifica el esquema y la versión del esquema actual es 1.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="cd60b-108">The schema is specified by MSIPatchApplicability.xsd and the current schema version is 1.0.0.0.</span></span> <span data-ttu-id="cd60b-109">El valor del atributo PatchGUID es el código de revisión GUID para el paquete de revisión Obtenido de la propiedad [**Resumen del número de revisión**](revision-number-summary.md) en el flujo de información de [Resumen](summary-information-stream.md) de la revisión.</span><span class="sxs-lookup"><span data-stu-id="cd60b-109">The value of the PatchGUID attribute is the GUID patch code for the patch package obtained from the [**Revision Number Summary**](revision-number-summary.md) Property in the [Summary Information Stream](summary-information-stream.md) of the patch.</span></span> <span data-ttu-id="cd60b-110">MinMsiVersion es la versión mínima de la Windows Installer necesaria para instalar la revisión obtenida de la propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="cd60b-110">The MinMsiVersion is the minimum version of the Windows Installer required to install the patch obtained from the [**Word Count Summary**](word-count-summary.md) Property.</span></span>

-   <span data-ttu-id="cd60b-111">El elemento TargetProduct es un elemento contenedor para obtener información sobre una aplicación de destino de una revisión.</span><span class="sxs-lookup"><span data-stu-id="cd60b-111">The TargetProduct element is a container element for information about an application that a patch targets.</span></span>

    <span data-ttu-id="cd60b-112">Puede haber varios elementos TargetProduct si la revisión puede aplicarse a varias aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="cd60b-112">There can be multiple TargetProduct elements if the patch can be applied to multiple applications.</span></span> <span data-ttu-id="cd60b-113">La información del elemento TargetProduct se extrae de las transformaciones que se incrustan dentro de la revisión.</span><span class="sxs-lookup"><span data-stu-id="cd60b-113">The information in the TargetProduct element is extracted from transforms that are embedded within the patch.</span></span>

-   <span data-ttu-id="cd60b-114">El elemento TargetProductCode contiene el valor de la propiedad [**ProductCode**](productcode.md) de la aplicación de destino antes de que se aplique la revisión.</span><span class="sxs-lookup"><span data-stu-id="cd60b-114">The TargetProductCode element contains the value of the [**ProductCode**](productcode.md) property of the target application before the patch has been applied.</span></span>

    <span data-ttu-id="cd60b-115">Puede haber varios elementos TargetProductCode si la revisión puede aplicarse a varias aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="cd60b-115">There can be multiple TargetProductCode elements if the patch can be applied to multiple applications.</span></span>

-   <span data-ttu-id="cd60b-116">El elemento UpdatedProductCode contiene el GUID del código de producto de la aplicación de destino una vez aplicada la revisión.</span><span class="sxs-lookup"><span data-stu-id="cd60b-116">The UpdatedProductCode element contains the product code GUID of the target application after the patch is applied.</span></span>

    <span data-ttu-id="cd60b-117">Este elemento solo está presente si la revisión cambia el valor de la propiedad [**ProductCode**](productcode.md) .</span><span class="sxs-lookup"><span data-stu-id="cd60b-117">This element is only present if the patch changes the value of the [**ProductCode**](productcode.md) property.</span></span> <span data-ttu-id="cd60b-118">Una revisión que cambia el **ProductCode** se conoce como una [actualización principal](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="cd60b-118">A patch that changes the **ProductCode** is referred to as a [Major Upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="cd60b-119">El elemento TargetVersion contiene la propiedad [**ProductVersion**](productversion.md) de la aplicación de destino antes de que se aplique la revisión.</span><span class="sxs-lookup"><span data-stu-id="cd60b-119">The TargetVersion element contains the [**ProductVersion**](productversion.md) property of the target application before the patch has been applied.</span></span>
-   <span data-ttu-id="cd60b-120">El elemento UpdateVersion contiene el valor de la propiedad [**ProductVersion**](productversion.md) de la aplicación de destino después de aplicar la revisión.</span><span class="sxs-lookup"><span data-stu-id="cd60b-120">The UpdateVersion element contains the value of the [**ProductVersion**](productversion.md) property of the target application after the patch is applied.</span></span>

    <span data-ttu-id="cd60b-121">Este elemento solo está presente si la revisión cambia el valor de la propiedad [**ProductVersion**](productversion.md) .</span><span class="sxs-lookup"><span data-stu-id="cd60b-121">This element is only present if the patch changes the value of the [**ProductVersion**](productversion.md) property.</span></span> <span data-ttu-id="cd60b-122">El BLOB XML de una revisión que implementa una [pequeña actualización](small-updates.md), también conocida como QFE, no incluirá este elemento.</span><span class="sxs-lookup"><span data-stu-id="cd60b-122">The XML blob for a patch that implements a [Small Update](small-updates.md), also referred to as a QFE, will not include this element.</span></span> <span data-ttu-id="cd60b-123">El BLOB XML de una revisión que implementa una actualización secundaria, también conocida como Service Pack, incluirá este elemento.</span><span class="sxs-lookup"><span data-stu-id="cd60b-123">The XML blob for a patch that implements a minor upgrade, also referred to as a service pack, will include this element.</span></span>

-   <span data-ttu-id="cd60b-124">El elemento TargetLanguage contiene el valor de la propiedad [**ProductLanguage**](productlanguage.md) de la aplicación de destino antes de que se aplique la revisión.</span><span class="sxs-lookup"><span data-stu-id="cd60b-124">The TargetLanguage element contains the value of the [**ProductLanguage**](productlanguage.md) property of the target application before the patch has been applied.</span></span>
-   <span data-ttu-id="cd60b-125">El elemento UpdatedLanguages contiene el valor de la propiedad [**ProductLanguage**](productlanguage.md) una vez aplicada la revisión.</span><span class="sxs-lookup"><span data-stu-id="cd60b-125">The UpdatedLanguages element contains the value of the [**ProductLanguage**](productlanguage.md) property after the patch has been applied.</span></span>
-   <span data-ttu-id="cd60b-126">El elemento UpgradeCode contiene el valor de la propiedad [**UpgradeCode**](upgradecode.md) de la aplicación de destino.</span><span class="sxs-lookup"><span data-stu-id="cd60b-126">The UpgradeCode element contains the value of the [**UpgradeCode**](upgradecode.md) property of the target application.</span></span>
-   <span data-ttu-id="cd60b-127">El elemento ObsoletedPatch contiene los códigos de revisión (GUID) de las revisiones que se especifican como obsoletas en esta revisión.</span><span class="sxs-lookup"><span data-stu-id="cd60b-127">The ObsoletedPatch element contains the patch codes (GUIDs) of the patches that are specified as obsolete by this patch.</span></span>

    <span data-ttu-id="cd60b-128">La lista de revisiones obsoletas se obtiene del [**Resumen de número de revisión**](revision-number-summary.md) en el [flujo de información de Resumen](summary-information-stream.md) de la revisión.</span><span class="sxs-lookup"><span data-stu-id="cd60b-128">The list of obsolete patches is obtained from [**Revision Number Summary**](revision-number-summary.md) in the [Summary Information Stream](summary-information-stream.md) of the patch.</span></span>

-   <span data-ttu-id="cd60b-129">El elemento SequenceData contiene información de secuencia de revisión para la revisión.</span><span class="sxs-lookup"><span data-stu-id="cd60b-129">The SequenceData element contains patch sequencing information for the patch.</span></span>

    <span data-ttu-id="cd60b-130">Puede haber varios elementos SequenceData en el BLOB XML.</span><span class="sxs-lookup"><span data-stu-id="cd60b-130">There can be multiple SequenceData elements in the XML blob.</span></span> <span data-ttu-id="cd60b-131">Cada elemento SequenceData contiene la información de una fila de la [tabla MsiPatchSequence](msipatchsequence-table.md) de la revisión.</span><span class="sxs-lookup"><span data-stu-id="cd60b-131">Each SequenceData element contains the information in one row of the [MsiPatchSequence table](msipatchsequence-table.md) of the patch.</span></span> <span data-ttu-id="cd60b-132">El elemento SequenceData contiene un subelemento ProductCode, Sequence y Attributes para la información de los campos correspondientes de la tabla MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="cd60b-132">The SequenceData element contains a ProductCode, Sequence, and Attributes subelement for the information in the corresponding fields in the MsiPatchSequence table.</span></span> <span data-ttu-id="cd60b-133">Vea la sección de la [tabla MsiPatchSequence](msipatchsequence-table.md) para obtener una descripción de cada campo.</span><span class="sxs-lookup"><span data-stu-id="cd60b-133">See the [MsiPatchSequence table](msipatchsequence-table.md) section for a description of each field.</span></span>

## <a name="extracting-applicability-information"></a><span data-ttu-id="cd60b-134">Extraer información de aplicabilidad</span><span class="sxs-lookup"><span data-stu-id="cd60b-134">Extracting Applicability Information</span></span>

<span data-ttu-id="cd60b-135">En el ejemplo siguiente se muestra cómo extraer la información de aplicabilidad de una revisión de Windows Installer (archivo. msp) mediante [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span><span class="sxs-lookup"><span data-stu-id="cd60b-135">The following example shows you how to extract the applicability information for a Windows Installer Patch (.msp file) using [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span></span> <span data-ttu-id="cd60b-136">El BLOB XML extraído se basa en la definición de esquema de MSIPatchApplicability. xsd y se devuelve a szXMLData.</span><span class="sxs-lookup"><span data-stu-id="cd60b-136">The extracted XML blob is based on the schema definition in MSIPatchApplicability.xsd and returned to szXMLData.</span></span>


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



<span data-ttu-id="cd60b-137">En el ejemplo siguiente se muestra cómo extraer la información de aplicabilidad de una revisión de Windows Installer (archivo. msp) en formato XML.</span><span class="sxs-lookup"><span data-stu-id="cd60b-137">The following example shows you how to extract the applicability information for a Windows Installer Patch (.msp file) in XML form.</span></span> <span data-ttu-id="cd60b-138">El BLOB XML extraído se basa en la definición de esquema de MSIPatchApplicability. xsd y se devuelve en strPatchXML.</span><span class="sxs-lookup"><span data-stu-id="cd60b-138">The extracted XML blob is based on the schema definition in MSIPatchApplicability.xsd and returned in strPatchXML.</span></span>

``` syntax
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")
strPatchXML = installer.ExtractPatchXMLData("c:\example\patch.msp")
```

## <a name="patch-applicability-schema-definition"></a><span data-ttu-id="cd60b-139">Definición del esquema de aplicabilidad de revisiones</span><span class="sxs-lookup"><span data-stu-id="cd60b-139">Patch Applicability Schema Definition</span></span>

<span data-ttu-id="cd60b-140">Copie el siguiente texto en el Bloc de notas o en otro editor de texto para crear el archivo de definición de esquema para la información de aplicabilidad de la revisión en el BLOB XML.</span><span class="sxs-lookup"><span data-stu-id="cd60b-140">Copy the following text into Notepad or another text editor to create the schema definition file for the patch applicability information in the XML blob.</span></span> <span data-ttu-id="cd60b-141">Asigne a este archivo el nombre MSIPatchApplicability. XSD.</span><span class="sxs-lookup"><span data-stu-id="cd60b-141">Name this file MSIPatchApplicability.XSD.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="cd60b-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cd60b-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd60b-143">**ExtractPatchXMLData**</span><span class="sxs-lookup"><span data-stu-id="cd60b-143">**ExtractPatchXMLData**</span></span>](installer-extractpatchxmldata.md)
</dt> <dt>

[<span data-ttu-id="cd60b-144">**MsiDeterminePatchSequence**</span><span class="sxs-lookup"><span data-stu-id="cd60b-144">**MsiDeterminePatchSequence**</span></span>](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
</dt> <dt>

[<span data-ttu-id="cd60b-145">**MsiDetermineApplicablePatches**</span><span class="sxs-lookup"><span data-stu-id="cd60b-145">**MsiDetermineApplicablePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
</dt> <dt>

[<span data-ttu-id="cd60b-146">**MsiExtractPatchXMLData**</span><span class="sxs-lookup"><span data-stu-id="cd60b-146">**MsiExtractPatchXMLData**</span></span>](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> </dl>

 

 



