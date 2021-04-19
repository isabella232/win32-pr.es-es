---
title: Elemento install
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El elemento install especifica valores usados por Windows Media Player para instalar una tienda en línea.
ms.assetid: 9a5e15ee-ec36-48d3-a1c2-bf20b6d2da48
keywords:
- Elemento Install Windows Media Player
topic_type:
- apiref
api_name:
- Install Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bba56240651f789b45c18b006b16e5e07b10676e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699323"
---
# <a name="install-element"></a><span data-ttu-id="8c110-106">Elemento install</span><span class="sxs-lookup"><span data-stu-id="8c110-106">Install Element</span></span>

> [!Note]  
> <span data-ttu-id="8c110-107">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="8c110-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="8c110-108">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="8c110-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="8c110-109">El elemento **install** especifica valores usados por Windows Media Player para instalar una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="8c110-109">The **Install** element specifies values used by Windows Media Player to install an online store.</span></span>

``` syntax
<Install
    EULAURL = "URL"
    CodeURL = "URL"
    PrivacyInfoURL = "URL"
    InstallApp = "filename"
    InstallData = "commandline"
    CatalogURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="8c110-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="8c110-110">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="8c110-111"><span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**EULAURL** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="8c110-111"><span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**EULAURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="8c110-112">Dirección URL completa de un archivo con una extensión de nombre de archivo. txt que Windows Media Player usa para mostrar un contrato de licencia para el usuario final (CLUF).</span><span class="sxs-lookup"><span data-stu-id="8c110-112">Fully qualified URL for a file with a .txt file name extension that Windows Media Player uses to display an End User License Agreement (EULA).</span></span> <span data-ttu-id="8c110-113">Este archivo debe estar codificado en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="8c110-113">This file must be encoded in ANSI format.</span></span>

</dd> <dt>

<span data-ttu-id="8c110-114"><span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**CodeURL** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="8c110-114"><span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**CodeURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="8c110-115">Dirección URL completa de un paquete, con la extensión de nombre de archivo. cab, que se usa para instalar la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="8c110-115">Fully qualified URL for a package, with a .cab file name extension, that is used to install the online store.</span></span> <span data-ttu-id="8c110-116">El paquete y todos los módulos de código del paquete deben estar firmados.</span><span class="sxs-lookup"><span data-stu-id="8c110-116">The package and all code modules in the package must be signed.</span></span> <span data-ttu-id="8c110-117">Para obtener información sobre la firma de código, vea [Introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) en MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="8c110-117">For information about code signing, see [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) in the MSDN Library.</span></span>

</dd> <dt>

<span data-ttu-id="8c110-118"><span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**PrivacyInfoURL** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="8c110-118"><span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**PrivacyInfoURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="8c110-119">Dirección URL completa de una página web que contiene información de la Directiva de privacidad de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="8c110-119">Fully qualified URL for a webpage that contains privacy policy information for the online store.</span></span>

</dd> <dt>

<span data-ttu-id="8c110-120"><span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**InstallApp** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="8c110-120"><span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**InstallApp** (required)</span></span>
</dt> <dd>

<span data-ttu-id="8c110-121">Nombre del archivo EXE o INF que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="8c110-121">Name of the EXE or INF file to run.</span></span> <span data-ttu-id="8c110-122">Este archivo debe estar incluido en el archivo CAB especificado por el atributo **CodeURL** .</span><span class="sxs-lookup"><span data-stu-id="8c110-122">This file must be contained in the CAB file specified by the **CodeURL** attribute.</span></span>

</dd> <dt>

<span data-ttu-id="8c110-123"><span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**InstallData** (opcional)</span><span class="sxs-lookup"><span data-stu-id="8c110-123"><span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**InstallData** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="8c110-124">Cadena de línea de comandos que se pasa a la aplicación especificada por el atributo **InstallApp** .</span><span class="sxs-lookup"><span data-stu-id="8c110-124">Command-line string that is passed to the application specified by the **InstallApp** attribute.</span></span> <span data-ttu-id="8c110-125">Este atributo solo es aplicable cuando el valor de **InstallApp** especifica un archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="8c110-125">This attribute is only applicable when the value for **InstallApp** specifies an executable.</span></span>

</dd> <dt>

<span data-ttu-id="8c110-126"><span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**CatalogURL** (necesario para el tipo 1, omitido para el tipo 2)</span><span class="sxs-lookup"><span data-stu-id="8c110-126"><span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**CatalogURL** (required for type 1, ignored for type 2)</span></span>
</dt> <dd>

<span data-ttu-id="8c110-127">Dirección URL completa del catálogo compilado de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="8c110-127">Fully qualified URL for the online store's compiled catalog.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="8c110-128">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="8c110-128">Parent/Child Elements</span></span>



| <span data-ttu-id="8c110-129">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="8c110-129">Hierarchy</span></span>       | <span data-ttu-id="8c110-130">Elemento</span><span class="sxs-lookup"><span data-stu-id="8c110-130">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="8c110-131">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="8c110-131">Parent elements</span></span> | <span data-ttu-id="8c110-132">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="8c110-132">**ServiceInfo**</span></span> |
| <span data-ttu-id="8c110-133">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8c110-133">Child elements</span></span>  | <span data-ttu-id="8c110-134">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8c110-134">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="8c110-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c110-135">Remarks</span></span>

<span data-ttu-id="8c110-136">Si falta alguno de los atributos necesarios o no está disponible, el programa de instalación de Windows Media Player no intentará descargar e instalar el código del proveedor de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="8c110-136">If any of the required attributes are missing or not available, Windows Media Player setup will not attempt to download and install the online store provider code.</span></span> <span data-ttu-id="8c110-137">El programa de instalación configurará los valores predeterminados sin conexión como se especifica en el documento **ServiceInfo** .</span><span class="sxs-lookup"><span data-stu-id="8c110-137">Setup will configure the offline default values as specified in the **ServiceInfo** document.</span></span> <span data-ttu-id="8c110-138">**ServiceInfo** se puede usar cuando no está conectado a Internet pasando el nombre del proveedor predeterminado y la información de **ServiceInfo** como parámetros de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="8c110-138">**ServiceInfo** can be used when not connected to the Internet by passing the default provider name and the **ServiceInfo** information as command-line parameters.</span></span> <span data-ttu-id="8c110-139">Consulte [redistribuir el software de Windows Media Player](redistributing-windows-media-player-software.md) para más información sobre las opciones de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="8c110-139">See [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md) for details about command-line options.</span></span>

> [!Note]  
> <span data-ttu-id="8c110-140">El uso de este elemento requiere que firme un contrato de redistribución con Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8c110-140">Use of this element requires that you sign a redistribution agreement with Microsoft.</span></span> <span data-ttu-id="8c110-141">Póngase en contacto con su representante comercial para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8c110-141">Contact your business representative for details.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8c110-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c110-142">Requirements</span></span>



| <span data-ttu-id="8c110-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c110-143">Requirement</span></span> | <span data-ttu-id="8c110-144">Value</span><span class="sxs-lookup"><span data-stu-id="8c110-144">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="8c110-145">Versión</span><span class="sxs-lookup"><span data-stu-id="8c110-145">Version</span></span><br/> | <span data-ttu-id="8c110-146">Windows Media Player 10 o posterior.</span><span class="sxs-lookup"><span data-stu-id="8c110-146">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8c110-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c110-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c110-148">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="8c110-148">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="8c110-149">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="8c110-149">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="8c110-150">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="8c110-150">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

