---
title: Elemento HTMLView
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El elemento HTMLView especifica la dirección URL base de una página web de HTMLView.
ms.assetid: 741db1ed-9452-4cae-9185-15668abe06b3
keywords:
- Elemento HTMLView Media Player Windows
topic_type:
- apiref
api_name:
- HTMLView Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f11a60e41b7f78be3440e16a7d2b3934f75e8ee3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699678"
---
# <a name="htmlview-element"></a><span data-ttu-id="ee868-106">Elemento HTMLView</span><span class="sxs-lookup"><span data-stu-id="ee868-106">HTMLView Element</span></span>

> [!Note]  
> <span data-ttu-id="ee868-107">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="ee868-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="ee868-108">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="ee868-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="ee868-109">El elemento **HTMLView** especifica la dirección URL base de una página web de HTMLView.</span><span class="sxs-lookup"><span data-stu-id="ee868-109">The **HTMLView** element specifies the base URL of an HTMLView webpage.</span></span>

``` syntax
<HTMLView
    BaseURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="ee868-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="ee868-110">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="ee868-111"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**Baseurl** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="ee868-111"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="ee868-112">Dirección URL base para la Página Web de HTMLView que Windows Media Player muestra.</span><span class="sxs-lookup"><span data-stu-id="ee868-112">Base URL for the HTMLView webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="ee868-113">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="ee868-113">Parent/Child Elements</span></span>



| <span data-ttu-id="ee868-114">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="ee868-114">Hierarchy</span></span>       | <span data-ttu-id="ee868-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="ee868-115">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="ee868-116">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="ee868-116">Parent elements</span></span> | <span data-ttu-id="ee868-117">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="ee868-117">**ServiceInfo**</span></span> |
| <span data-ttu-id="ee868-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ee868-118">Child elements</span></span>  | <span data-ttu-id="ee868-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ee868-119">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="ee868-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee868-120">Remarks</span></span>

<span data-ttu-id="ee868-121">Puede usar este elemento para integrar la característica HTMLView con la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="ee868-121">You can use this element to integrate the HTMLView feature with your online store.</span></span> <span data-ttu-id="ee868-122">Si el dominio de la dirección URL especificada por la tienda en línea actual coincide con el de la Página Web de HTMLView, el cambio a **reproducción** en curso se produce sin la intervención del usuario y se muestra el contenido de HTMLView.</span><span class="sxs-lookup"><span data-stu-id="ee868-122">If the domain of the URL specified by the current online store matches the one for the HTMLView webpage, the switch to **Now Playing** happens without user intervention and the HTMLView content is displayed.</span></span> <span data-ttu-id="ee868-123">De lo contrario, Windows Media Player solicita al usuario permiso para mostrar el contenido de HTMLView.</span><span class="sxs-lookup"><span data-stu-id="ee868-123">Otherwise, Windows Media Player prompts the user for permission to show the HTMLView content.</span></span>

<span data-ttu-id="ee868-124">Por ejemplo, si la dirección URL de la Página Web de HTMLView es https://www.proseware.com/html/HTMLView.htm y la dirección URL del atributo **baseurl** se especifica como https://www.proseware.com , se muestra la página web HTMLView sin preguntar al usuario.</span><span class="sxs-lookup"><span data-stu-id="ee868-124">For example, if the URL for the HTMLView webpage is https://www.proseware.com/html/HTMLView.htm and the URL for the **BaseURL** attribute is specified as https://www.proseware.com, the HTMLView webpage displays without prompting the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee868-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee868-125">Requirements</span></span>



| <span data-ttu-id="ee868-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee868-126">Requirement</span></span> | <span data-ttu-id="ee868-127">Value</span><span class="sxs-lookup"><span data-stu-id="ee868-127">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="ee868-128">Versión</span><span class="sxs-lookup"><span data-stu-id="ee868-128">Version</span></span><br/> | <span data-ttu-id="ee868-129">Windows Media Player 10 o posterior</span><span class="sxs-lookup"><span data-stu-id="ee868-129">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee868-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee868-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee868-131">**Mostrar páginas web en Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="ee868-131">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="ee868-132">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="ee868-132">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="ee868-133">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="ee868-133">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="ee868-134">**Elemento PARAM**</span><span class="sxs-lookup"><span data-stu-id="ee868-134">**PARAM Element**</span></span>](param-element.md)
</dt> <dt>

[<span data-ttu-id="ee868-135">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="ee868-135">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





