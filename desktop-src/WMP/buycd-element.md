---
title: Elemento BuyCD
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. | Elemento BuyCD
ms.assetid: 01aaf20a-49ee-420b-a612-f09155390d4a
keywords:
- Elemento BuyCD Media Player Windows
topic_type:
- apiref
api_name:
- BuyCD Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca1ebe4bd85015ca9ce1c0bece24e7dc47ff9fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699625"
---
# <a name="buycd-element"></a><span data-ttu-id="34e12-105">Elemento BuyCD</span><span class="sxs-lookup"><span data-stu-id="34e12-105">BuyCD Element</span></span>

> [!Note]  
> <span data-ttu-id="34e12-106">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="34e12-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="34e12-107">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="34e12-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="34e12-108">El elemento **BuyCD** especifica las direcciones URL de las páginas web que Windows Media Player muestra cuando el usuario decide hacer una compra.</span><span class="sxs-lookup"><span data-stu-id="34e12-108">The **BuyCD** element specifies the URLs for webpages that Windows Media Player displays when the user chooses to make a purchase.</span></span>

``` syntax
<BuyCD
    MediaPlayerURL = "URL"
    MediaCenterURL = "URL"
    BrowserURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="34e12-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="34e12-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="34e12-110"><span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**MediaPlayerURL** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="34e12-110"><span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**MediaPlayerURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="34e12-111">Dirección URL de la página web que muestra la tienda en línea para ofrecer un CD o DVD para la compra en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="34e12-111">URL for the webpage that the online store displays to offer a CD or DVD for purchase in Windows Media Player.</span></span>

</dd> <dt>

<span data-ttu-id="34e12-112"><span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**</span><span class="sxs-lookup"><span data-stu-id="34e12-112"><span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**</span></span>
</dt> <dd>

<span data-ttu-id="34e12-113">Dirección URL de la página web que se muestra en la tienda en línea para ofrecer un CD o DVD para la compra en la actualización 2004 de Windows XP Media Center Edition.</span><span class="sxs-lookup"><span data-stu-id="34e12-113">URL for the webpage the online store displays to offer a CD or DVD for purchase in Windows XP Media Center Edition 2004 Update.</span></span>

</dd> <dt>

<span data-ttu-id="34e12-114"><span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**</span><span class="sxs-lookup"><span data-stu-id="34e12-114"><span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**</span></span>
</dt> <dd>

<span data-ttu-id="34e12-115">Dirección URL de la página web que la tienda en línea muestra para ofrecer un CD o DVD para la compra en una ventana del explorador independiente.</span><span class="sxs-lookup"><span data-stu-id="34e12-115">URL for the webpage that the online store displays to offer a CD or DVD for purchase in a separate browser window.</span></span> <span data-ttu-id="34e12-116">Windows XP Service Pack 2 o posterior usa esta dirección URL para la característica de la **tienda de música en línea** .</span><span class="sxs-lookup"><span data-stu-id="34e12-116">This URL is also used by Windows XP Service Pack 2 or later for the **Shop for music online** feature.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="34e12-117">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="34e12-117">Parent/Child Elements</span></span>



| <span data-ttu-id="34e12-118">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="34e12-118">Hierarchy</span></span>       | <span data-ttu-id="34e12-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="34e12-119">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="34e12-120">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="34e12-120">Parent elements</span></span> | <span data-ttu-id="34e12-121">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="34e12-121">**ServiceInfo**</span></span> |
| <span data-ttu-id="34e12-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="34e12-122">Child elements</span></span>  | <span data-ttu-id="34e12-123">Ninguno</span><span class="sxs-lookup"><span data-stu-id="34e12-123">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="34e12-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34e12-124">Remarks</span></span>

<span data-ttu-id="34e12-125">Cuando el usuario hace clic en un botón o vínculo de Windows Media Player para adquirir un CD o DVD, el reproductor envía la solicitud de dirección URL a ServiceTask1 con los parámetros adjuntos mediante un signo de interrogación (?) separador de cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="34e12-125">When the user clicks a button or link in Windows Media Player to purchase a CD or DVD, the Player sends the URL request to ServiceTask1 with parameters attached using a question mark (?) query string separator.</span></span> <span data-ttu-id="34e12-126">En la tabla siguiente se detallan los parámetros que se envían con la solicitud URL.</span><span class="sxs-lookup"><span data-stu-id="34e12-126">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="34e12-127">Otros pueden estar presentes para fines de compatibilidad heredada.</span><span class="sxs-lookup"><span data-stu-id="34e12-127">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="34e12-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="34e12-128">Name</span></span>         | <span data-ttu-id="34e12-129">Value</span><span class="sxs-lookup"><span data-stu-id="34e12-129">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34e12-130">*Álbum*</span><span class="sxs-lookup"><span data-stu-id="34e12-130">*Album*</span></span>      | <span data-ttu-id="34e12-131">Valor del atributo **WM/álbum** para el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="34e12-131">Value of the **WM/AlbumTitle** attribute for the media item.</span></span>                                                                                                        |
| <span data-ttu-id="34e12-132">*Artistas*</span><span class="sxs-lookup"><span data-stu-id="34e12-132">*Artist*</span></span>     | <span data-ttu-id="34e12-133">Valor del atributo **WM/AlbumArtist** , si existe, o el valor del atributo **Author** del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="34e12-133">Value of the **WM/AlbumArtist** attribute, if one exists, or else the value of the **Author** attribute for the media item.</span></span>                                         |
| <span data-ttu-id="34e12-134">*Geoid*</span><span class="sxs-lookup"><span data-stu-id="34e12-134">*geoid*</span></span>      | <span data-ttu-id="34e12-135">IDENTIFICADOR de ubicación geográfica de Windows.</span><span class="sxs-lookup"><span data-stu-id="34e12-135">Windows geographical location ID.</span></span> <span data-ttu-id="34e12-136">El ID. de ubicación lo especifica el usuario en el área **Ubicación** de la configuración de configuración regional y de idioma del panel de control.</span><span class="sxs-lookup"><span data-stu-id="34e12-136">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="34e12-137">*locale*</span><span class="sxs-lookup"><span data-stu-id="34e12-137">*locale*</span></span>     | <span data-ttu-id="34e12-138">IDENTIFICADOR de configuración regional de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="34e12-138">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="34e12-139">*Título*</span><span class="sxs-lookup"><span data-stu-id="34e12-139">*Title*</span></span>      | <span data-ttu-id="34e12-140">Valor del atributo **title** del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="34e12-140">Value of the **Title** attribute for the media item.</span></span>                                                                                                                |
| <span data-ttu-id="34e12-141">*UFID*</span><span class="sxs-lookup"><span data-stu-id="34e12-141">*UFID*</span></span>       | <span data-ttu-id="34e12-142">Valor del atributo **WM/UniqueFileIdentifier** para el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="34e12-142">Value of the **WM/UniqueFileIdentifier** attribute for the media item.</span></span>                                                                                              |
| <span data-ttu-id="34e12-143">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="34e12-143">*userlocale*</span></span> | <span data-ttu-id="34e12-144">IDENTIFICADOR de configuración regional de Windows.</span><span class="sxs-lookup"><span data-stu-id="34e12-144">Windows locale ID.</span></span> <span data-ttu-id="34e12-145">El usuario especifica la configuración regional en el área **estándares y formatos** de la configuración configuración regional y de idioma del panel de control.</span><span class="sxs-lookup"><span data-stu-id="34e12-145">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="34e12-146">*version*</span><span class="sxs-lookup"><span data-stu-id="34e12-146">*version*</span></span>    | <span data-ttu-id="34e12-147">Windows Media Player número de versión con el formato siguiente: 10.0. x. xxxx o 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="34e12-147">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

<span data-ttu-id="34e12-148">Windows XP Media Center Edition 2004 proporciona a los usuarios una interfaz de usuario diseñada para su visualización a distancia.</span><span class="sxs-lookup"><span data-stu-id="34e12-148">Windows XP Media Center Edition 2004 provides users with a user interface designed to be viewed at a distance.</span></span> <span data-ttu-id="34e12-149">Debe crear páginas web para que el parámetro *MediaCenterURL* se vea en pantallas de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="34e12-149">You should create webpages for the *MediaCenterURL* parameter to be viewed on large displays.</span></span>

## <a name="requirements"></a><span data-ttu-id="34e12-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34e12-150">Requirements</span></span>



| <span data-ttu-id="34e12-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="34e12-151">Requirement</span></span> | <span data-ttu-id="34e12-152">Value</span><span class="sxs-lookup"><span data-stu-id="34e12-152">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="34e12-153">Versión</span><span class="sxs-lookup"><span data-stu-id="34e12-153">Version</span></span><br/> | <span data-ttu-id="34e12-154">Windows Media Player 10 o posterior.</span><span class="sxs-lookup"><span data-stu-id="34e12-154">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34e12-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="34e12-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34e12-156">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="34e12-156">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="34e12-157">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="34e12-157">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="34e12-158">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="34e12-158">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





