---
title: Elemento Image (SDK de WMP)
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. | Elemento Image (SDK de WMP)
ms.assetid: 06804c26-e847-43a7-bb75-60da600c7d4f
keywords:
- Elemento de imagen Media Player de Windows
topic_type:
- apiref
api_name:
- Image Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c10b62365453f395c1aaf373e355c21260900f8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699983"
---
# <a name="image-element-wmp-sdk"></a><span data-ttu-id="d31ca-105">Elemento Image (SDK de WMP)</span><span class="sxs-lookup"><span data-stu-id="d31ca-105">Image Element (WMP SDK)</span></span>

> [!Note]  
> <span data-ttu-id="d31ca-106">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="d31ca-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="d31ca-107">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="d31ca-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="d31ca-108">El elemento **Image** especifica las imágenes que Windows Media Player muestra al usuario para representar la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="d31ca-108">The **Image** element specifies the images that Windows Media Player displays to the user to represent the online store.</span></span>

``` syntax
<Image
    EulaURL = "URL"
    MenuURL = "URL"
    ServiceLargeURL = "URL"
    ServiceSmallURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="d31ca-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="d31ca-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="d31ca-110"><span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**EulaURL** (necesario para los almacenes de tipo 1, omitido para el tipo 2)</span><span class="sxs-lookup"><span data-stu-id="d31ca-110"><span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**EulaURL** (required for type 1 stores, ignored for type 2)</span></span>
</dt> <dd>

<span data-ttu-id="d31ca-111">Dirección URL del logotipo que Windows Media Player muestra en el cuadro de diálogo contrato de licencia para el usuario final (CLUF).</span><span class="sxs-lookup"><span data-stu-id="d31ca-111">URL for the logo that Windows Media Player displays in the end user license agreement (EULA) dialog box.</span></span> <span data-ttu-id="d31ca-112">Debe ser una imagen PNG de 80 x 80 píxeles.</span><span class="sxs-lookup"><span data-stu-id="d31ca-112">This must be a PNG image that is 80 x 80 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="d31ca-113"><span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (opcional)</span><span class="sxs-lookup"><span data-stu-id="d31ca-113"><span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="d31ca-114">Dirección URL de la imagen que Windows Media Player muestra en el menú servicios.</span><span class="sxs-lookup"><span data-stu-id="d31ca-114">URL for the image that Windows Media Player displays on the services menu.</span></span> <span data-ttu-id="d31ca-115">Esta imagen debe tener 15 x 15 píxeles.</span><span class="sxs-lookup"><span data-stu-id="d31ca-115">This image must be 15 x 15 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="d31ca-116"><span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (opcional)</span><span class="sxs-lookup"><span data-stu-id="d31ca-116"><span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="d31ca-117">En el caso de una tienda en línea de tipo 1, se trata de la dirección URL de la imagen que Windows Media Player muestra en la pestaña **tiendas en línea** . En Windows Media Player 11, esta imagen debe tener una anchura de 45 píxeles de ancho por 13 píxeles de alto.</span><span class="sxs-lookup"><span data-stu-id="d31ca-117">For a type 1 online store, this is the URL for the image that Windows Media Player displays on the **Online Stores** tab. For Windows Media Player 11, this image must be 45 pixels wide by 13 pixels high.</span></span> <span data-ttu-id="d31ca-118">En Windows Media Player 12, esta imagen debe tener una anchura de 45 píxeles de ancho por 30 píxeles de alto.</span><span class="sxs-lookup"><span data-stu-id="d31ca-118">For Windows Media Player 12, this image must be 45 pixels wide by 30 pixels high.</span></span> <span data-ttu-id="d31ca-119">Para admitir las versiones 11 y 12 de Windows Media Player, debe proporcionar dos documentos ServiceInfo.xml independientes, cada uno de los cuales señala a la imagen de tamaño adecuado para ServiceLargeURL.</span><span class="sxs-lookup"><span data-stu-id="d31ca-119">To support both versions 11 and 12 of Windows Media Player, you must provide two separate ServiceInfo.xml documents, each of which points to the appropriately sized image for ServiceLargeURL.</span></span>

<span data-ttu-id="d31ca-120">En el caso de una tienda en línea de tipo 2, se trata de la dirección URL de la imagen que Windows Media Player muestra junto a la ficha **tiendas en línea** o junto a los botones del panel de tareas.</span><span class="sxs-lookup"><span data-stu-id="d31ca-120">For a type 2 online store, this is the URL for the image that Windows Media Player displays beside the **Online Stores** tab or beside the task pane buttons.</span></span> <span data-ttu-id="d31ca-121">Esta imagen debe ser 30 x 30 píxeles.</span><span class="sxs-lookup"><span data-stu-id="d31ca-121">This image must be 30 x 30 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="d31ca-122"><span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (opcional)</span><span class="sxs-lookup"><span data-stu-id="d31ca-122"><span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="d31ca-123">Dirección URL del logotipo que se muestra junto con la descripción de marketing especificada en el elemento **Description** .</span><span class="sxs-lookup"><span data-stu-id="d31ca-123">URL for the logo that is displayed along with the marketing description specified in the **Description** element.</span></span> <span data-ttu-id="d31ca-124">Si no se proporciona, estará en blanco.</span><span class="sxs-lookup"><span data-stu-id="d31ca-124">If it is not supplied, it will be blank.</span></span> <span data-ttu-id="d31ca-125">(Todos los tipos, opcional) Debe ser una imagen PNG de 45 píxeles de ancho y 13 píxeles de alto.</span><span class="sxs-lookup"><span data-stu-id="d31ca-125">(All types, optional) This must be a PNG image that is 45 pixels wide and 13 pixels high.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="d31ca-126">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="d31ca-126">Parent/Child Elements</span></span>



| <span data-ttu-id="d31ca-127">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="d31ca-127">Hierarchy</span></span>       | <span data-ttu-id="d31ca-128">Elemento</span><span class="sxs-lookup"><span data-stu-id="d31ca-128">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="d31ca-129">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="d31ca-129">Parent elements</span></span> | <span data-ttu-id="d31ca-130">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="d31ca-130">**ServiceInfo**</span></span> |
| <span data-ttu-id="d31ca-131">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d31ca-131">Child elements</span></span>  | <span data-ttu-id="d31ca-132">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d31ca-132">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="d31ca-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d31ca-133">Remarks</span></span>

<span data-ttu-id="d31ca-134">Los formatos de imagen admitidos son. gif,. jpg,. bmp y. png (que es el formato recomendado).</span><span class="sxs-lookup"><span data-stu-id="d31ca-134">The supported image formats are .gif, .jpg, .bmp, and .png (which is the recommended format).</span></span> <span data-ttu-id="d31ca-135">El uso de la transparencia web es compatible y recomendado.</span><span class="sxs-lookup"><span data-stu-id="d31ca-135">Using Web transparency is both supported and recommended.</span></span> <span data-ttu-id="d31ca-136">No se admiten archivos GIF animados.</span><span class="sxs-lookup"><span data-stu-id="d31ca-136">Animated GIF files are not supported.</span></span>

<span data-ttu-id="d31ca-137">Si no proporciona un valor para **MenuURL**, Windows Media Player no muestra ningún gráfico en el menú de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="d31ca-137">If you do not supply a value for **MenuURL**, Windows Media Player displays no graphic on the menu for your online store.</span></span>

<span data-ttu-id="d31ca-138">Puede proporcionar una imagen animada para ServiceLargeURL.</span><span class="sxs-lookup"><span data-stu-id="d31ca-138">You can provide an animated image for ServiceLargeURL.</span></span> <span data-ttu-id="d31ca-139">En Windows Media Player 10 u 11, la imagen se anima.</span><span class="sxs-lookup"><span data-stu-id="d31ca-139">In Windows Media Player 10 or 11, the image is animated.</span></span> <span data-ttu-id="d31ca-140">En Windows Media Player 12, solo se muestra el primer fotograma de la imagen.</span><span class="sxs-lookup"><span data-stu-id="d31ca-140">In Windows Media Player 12, only the first frame of the image is displayed.</span></span> <span data-ttu-id="d31ca-141">Para proporcionar una imagen animada, cree un único archivo de imagen que contenga fotogramas sucesivos de la animación.</span><span class="sxs-lookup"><span data-stu-id="d31ca-141">To provide an animated image, create a single image file that contains successive frames of your animation.</span></span> <span data-ttu-id="d31ca-142">Por ejemplo, para una imagen de 30 píxeles de ancho y 30 píxeles de alto, puede proporcionar 20 imágenes sucesivas en paralelo en una imagen de 600 píxeles de ancho y 30 píxeles de alto.</span><span class="sxs-lookup"><span data-stu-id="d31ca-142">For example, for an image that is 30 pixels wide and 30 pixels high, you could supply 20 successive images side by side in an image that is 600 pixels wide and 30 pixels high.</span></span> <span data-ttu-id="d31ca-143">Windows Media Player animaría automáticamente una imagen de este tipo mostrando las 20 imágenes individuales una tras otra.</span><span class="sxs-lookup"><span data-stu-id="d31ca-143">Windows Media Player would automatically animate such an image by showing the 20 individual images one after another.</span></span> <span data-ttu-id="d31ca-144">Esta animación se produce una sola vez cuando se abre la tienda en línea; no se repite.</span><span class="sxs-lookup"><span data-stu-id="d31ca-144">This animation occurs only once when the online store opens; it does not repeat.</span></span>

## <a name="requirements"></a><span data-ttu-id="d31ca-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d31ca-145">Requirements</span></span>



| <span data-ttu-id="d31ca-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="d31ca-146">Requirement</span></span> | <span data-ttu-id="d31ca-147">Value</span><span class="sxs-lookup"><span data-stu-id="d31ca-147">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="d31ca-148">Versión</span><span class="sxs-lookup"><span data-stu-id="d31ca-148">Version</span></span><br/> | <span data-ttu-id="d31ca-149">Windows Media Player 10 o posterior</span><span class="sxs-lookup"><span data-stu-id="d31ca-149">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d31ca-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="d31ca-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d31ca-151">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="d31ca-151">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="d31ca-152">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="d31ca-152">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="d31ca-153">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="d31ca-153">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





