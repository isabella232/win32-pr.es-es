---
title: Elemento color
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. | Elemento color
ms.assetid: 36fafe16-b708-4dc1-9325-d4f39265069a
keywords:
- Elemento de color Media Player de Windows
topic_type:
- apiref
api_name:
- Color Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c73aa9fe2c7f731e872c4a2e235bf9c0e29ce05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700132"
---
# <a name="color-element"></a><span data-ttu-id="dfeed-105">Elemento color</span><span class="sxs-lookup"><span data-stu-id="dfeed-105">Color Element</span></span>

> [!Note]  
> <span data-ttu-id="dfeed-106">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="dfeed-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="dfeed-107">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="dfeed-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="dfeed-108">El elemento color especifica el color de fondo de los botones de navegación de la tienda en línea, el texto del botón y la barra de tareas características.</span><span class="sxs-lookup"><span data-stu-id="dfeed-108">The Color element specifies the background color for online store navigation buttons, button text, and the Features taskbar.</span></span>

``` syntax
<Color
    MediaPlayer = "#FFFFFF"
    MediaPlayerText = "#FFFFFF"
/>
```

## <a name="attributes"></a><span data-ttu-id="dfeed-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="dfeed-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="dfeed-110"><span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**MediaPlayer** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="dfeed-110"><span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**MediaPlayer** (required)</span></span>
</dt> <dd>

<span data-ttu-id="dfeed-111">Valor de color RGB hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="dfeed-111">Hexadecimal RGB color value.</span></span> <span data-ttu-id="dfeed-112">Especifica el color de fondo de los botones y la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="dfeed-112">Specifies the background color for buttons and the taskbar.</span></span>

</dd> <dt>

<span data-ttu-id="dfeed-113"><span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**MediaPlayerText** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="dfeed-113"><span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**MediaPlayerText** (required)</span></span>
</dt> <dd>

<span data-ttu-id="dfeed-114">Valor de color RGB hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="dfeed-114">Hexadecimal RGB color value.</span></span> <span data-ttu-id="dfeed-115">Especifica el color del texto del botón.</span><span class="sxs-lookup"><span data-stu-id="dfeed-115">Specifies the color for the button text.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="dfeed-116">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="dfeed-116">Parent/Child Elements</span></span>



| <span data-ttu-id="dfeed-117">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="dfeed-117">Hierarchy</span></span>       | <span data-ttu-id="dfeed-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="dfeed-118">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="dfeed-119">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="dfeed-119">Parent elements</span></span> | <span data-ttu-id="dfeed-120">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="dfeed-120">**ServiceInfo**</span></span> |
| <span data-ttu-id="dfeed-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dfeed-121">Child elements</span></span>  | <span data-ttu-id="dfeed-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="dfeed-122">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="dfeed-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dfeed-123">Remarks</span></span>

<span data-ttu-id="dfeed-124">El valor predeterminado de **MediaPlayer** es \# 7C9AD6.</span><span class="sxs-lookup"><span data-stu-id="dfeed-124">The default value for **MediaPlayer** is \#7C9AD6.</span></span> <span data-ttu-id="dfeed-125">El valor predeterminado de **MediaPlayerText** es \# FFFFFF.</span><span class="sxs-lookup"><span data-stu-id="dfeed-125">The default value for **MediaPlayerText** is \#FFFFFF.</span></span>

<span data-ttu-id="dfeed-126">Asegúrese de usar colores que facilitan al usuario la lectura del texto del botón.</span><span class="sxs-lookup"><span data-stu-id="dfeed-126">Be sure to use colors that make it easy for the user to read the button text.</span></span> <span data-ttu-id="dfeed-127">Por ejemplo, debe evitar el uso de texto de botón blanco en botones de color claro.</span><span class="sxs-lookup"><span data-stu-id="dfeed-127">For example, you should avoid using white button text on light colored buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfeed-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfeed-128">Requirements</span></span>



| <span data-ttu-id="dfeed-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfeed-129">Requirement</span></span> | <span data-ttu-id="dfeed-130">Value</span><span class="sxs-lookup"><span data-stu-id="dfeed-130">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="dfeed-131">Versión</span><span class="sxs-lookup"><span data-stu-id="dfeed-131">Version</span></span><br/> | <span data-ttu-id="dfeed-132">Windows Media Player 10 o posterior.</span><span class="sxs-lookup"><span data-stu-id="dfeed-132">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dfeed-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfeed-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfeed-134">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="dfeed-134">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="dfeed-135">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="dfeed-135">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="dfeed-136">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="dfeed-136">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





