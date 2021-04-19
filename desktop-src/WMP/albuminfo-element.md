---
title: Elemento AlbumInfo
description: El elemento AlbumInfo especifica la dirección URL de la página web que Windows Media Player muestra cuando el usuario elige ver más información sobre un elemento multimedia determinado.
ms.assetid: c872e95a-3723-4ce8-8d61-e2bc9e12c785
keywords:
- Elemento AlbumInfo Media Player Windows
topic_type:
- apiref
api_name:
- AlbumInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3805ae2d5fca687ce024efca74e0254db7c8ae3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699751"
---
# <a name="albuminfo-element"></a><span data-ttu-id="1f566-104">Elemento AlbumInfo</span><span class="sxs-lookup"><span data-stu-id="1f566-104">AlbumInfo Element</span></span>

> [!Note]  
> <span data-ttu-id="1f566-105">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="1f566-105">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="1f566-106">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="1f566-106">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="1f566-107">El elemento **AlbumInfo** especifica la dirección URL de la página web que Windows Media Player muestra cuando el usuario elige ver más información sobre un elemento multimedia determinado.</span><span class="sxs-lookup"><span data-stu-id="1f566-107">The **AlbumInfo** element specifies the URL for the webpage that Windows Media Player displays when the user chooses to view more information about a particular media item.</span></span>

``` syntax
<AlbumInfo
   URL = "URL"
/>
      
```

## <a name="attributes"></a><span data-ttu-id="1f566-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1f566-108">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="1f566-109"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="1f566-109"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="1f566-110">Dirección URL de la página web que Windows Media Player muestra.</span><span class="sxs-lookup"><span data-stu-id="1f566-110">URL for the webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="1f566-111">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="1f566-111">Parent/Child Elements</span></span>



| <span data-ttu-id="1f566-112">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="1f566-112">Hierarchy</span></span>       | <span data-ttu-id="1f566-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="1f566-113">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="1f566-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="1f566-114">Parent elements</span></span> | <span data-ttu-id="1f566-115">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="1f566-115">**ServiceInfo**</span></span> |
| <span data-ttu-id="1f566-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1f566-116">Child elements</span></span>  | <span data-ttu-id="1f566-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1f566-117">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="1f566-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f566-118">Remarks</span></span>

<span data-ttu-id="1f566-119">Cuando el usuario hace clic en un botón de Windows Media Player para ver información adicional sobre un elemento multimedia determinado, el reproductor envía la solicitud de dirección URL con los parámetros adjuntos mediante un signo de interrogación (?) separador de cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="1f566-119">When the user clicks a button in Windows Media Player to view additional information about a particular media item, the Player sends the URL request with parameters attached using a question mark (?) query string separator.</span></span> <span data-ttu-id="1f566-120">En la tabla siguiente se detallan los parámetros que se envían con la solicitud URL.</span><span class="sxs-lookup"><span data-stu-id="1f566-120">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="1f566-121">Otros pueden estar presentes para fines de compatibilidad heredada.</span><span class="sxs-lookup"><span data-stu-id="1f566-121">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="1f566-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="1f566-122">Name</span></span>         | <span data-ttu-id="1f566-123">Value</span><span class="sxs-lookup"><span data-stu-id="1f566-123">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f566-124">*Álbum*</span><span class="sxs-lookup"><span data-stu-id="1f566-124">*Album*</span></span>      | <span data-ttu-id="1f566-125">Valor del atributo **WM/álbum** para el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="1f566-125">Value of the **WM/AlbumTitle** attribute for the media item.</span></span>                                                                                                        |
| <span data-ttu-id="1f566-126">*Artistas*</span><span class="sxs-lookup"><span data-stu-id="1f566-126">*Artist*</span></span>     | <span data-ttu-id="1f566-127">Valor del atributo **WM/AlbumArtist** , si existe, o el valor del atributo **Author** del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="1f566-127">Value of the **WM/AlbumArtist** attribute, if one exists, or else the value of the **Author** attribute for the media item.</span></span>                                         |
| <span data-ttu-id="1f566-128">*Geoid*</span><span class="sxs-lookup"><span data-stu-id="1f566-128">*geoid*</span></span>      | <span data-ttu-id="1f566-129">IDENTIFICADOR de ubicación geográfica de Windows.</span><span class="sxs-lookup"><span data-stu-id="1f566-129">Windows geographical location ID.</span></span> <span data-ttu-id="1f566-130">El ID. de ubicación lo especifica el usuario en el área **Ubicación** de la configuración de configuración regional y de idioma del panel de control.</span><span class="sxs-lookup"><span data-stu-id="1f566-130">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="1f566-131">*locale*</span><span class="sxs-lookup"><span data-stu-id="1f566-131">*locale*</span></span>     | <span data-ttu-id="1f566-132">IDENTIFICADOR de configuración regional de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="1f566-132">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="1f566-133">*Título*</span><span class="sxs-lookup"><span data-stu-id="1f566-133">*Title*</span></span>      | <span data-ttu-id="1f566-134">Valor del atributo **title** del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="1f566-134">Value of the **Title** attribute for the media item.</span></span>                                                                                                                |
| <span data-ttu-id="1f566-135">*UFID*</span><span class="sxs-lookup"><span data-stu-id="1f566-135">*UFID*</span></span>       | <span data-ttu-id="1f566-136">Valor del atributo **WM/UniqueFileIdentifier** para el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="1f566-136">Value of the **WM/UniqueFileIdentifier** attribute for the media item.</span></span>                                                                                              |
| <span data-ttu-id="1f566-137">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="1f566-137">*userlocale*</span></span> | <span data-ttu-id="1f566-138">IDENTIFICADOR de configuración regional de Windows.</span><span class="sxs-lookup"><span data-stu-id="1f566-138">Windows locale ID.</span></span> <span data-ttu-id="1f566-139">El usuario especifica la configuración regional en el área **estándares y formatos** de la configuración configuración regional y de idioma del panel de control.</span><span class="sxs-lookup"><span data-stu-id="1f566-139">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="1f566-140">*version*</span><span class="sxs-lookup"><span data-stu-id="1f566-140">*version*</span></span>    | <span data-ttu-id="1f566-141">Windows Media Player número de versión con el formato siguiente: 10.0. x. xxxx o 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="1f566-141">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="1f566-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f566-142">Requirements</span></span>



| <span data-ttu-id="1f566-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f566-143">Requirement</span></span> | <span data-ttu-id="1f566-144">Value</span><span class="sxs-lookup"><span data-stu-id="1f566-144">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="1f566-145">Versión</span><span class="sxs-lookup"><span data-stu-id="1f566-145">Version</span></span><br/> | <span data-ttu-id="1f566-146">Windows Media Player 10 o posterior.</span><span class="sxs-lookup"><span data-stu-id="1f566-146">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f566-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f566-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f566-148">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="1f566-148">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="1f566-149">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="1f566-149">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="1f566-150">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="1f566-150">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





