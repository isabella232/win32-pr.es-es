---
title: VER. titleBar
description: El atributo titleBar recupera un valor que indica si se muestra la barra de título de la ventana.
ms.assetid: 996aa2e0-0313-4a48-adcb-b82f76f38b6a
keywords:
- Ver ventanas de Media Player. titleBar
topic_type:
- apiref
api_name:
- VIEW.titleBar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea225103913e3906cf6cd3b129943fbf9b9f165
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718733"
---
# <a name="viewtitlebar"></a><span data-ttu-id="bf97b-104">VER. titleBar</span><span class="sxs-lookup"><span data-stu-id="bf97b-104">VIEW.titleBar</span></span>

<span data-ttu-id="bf97b-105">El atributo **TitleBar** recupera un valor que indica si se muestra la barra de título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="bf97b-105">The **titleBar** attribute retrieves a value indicating whether the window title bar is shown.</span></span>

``` syntax
        elementID.titleBar
```

## <a name="possible-values"></a><span data-ttu-id="bf97b-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="bf97b-106">Possible Values</span></span>

<span data-ttu-id="bf97b-107">Este atributo es un **valor booleano** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bf97b-107">This attribute is a read-only **Boolean**.</span></span>



| <span data-ttu-id="bf97b-108">Value</span><span class="sxs-lookup"><span data-stu-id="bf97b-108">Value</span></span> | <span data-ttu-id="bf97b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf97b-109">Description</span></span>                             |
|-------|-----------------------------------------|
| <span data-ttu-id="bf97b-110">true</span><span class="sxs-lookup"><span data-stu-id="bf97b-110">true</span></span>  | <span data-ttu-id="bf97b-111">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="bf97b-111">Default.</span></span> <span data-ttu-id="bf97b-112">Se muestra la barra de título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="bf97b-112">The window title bar is shown.</span></span> |
| <span data-ttu-id="bf97b-113">false</span><span class="sxs-lookup"><span data-stu-id="bf97b-113">false</span></span> | <span data-ttu-id="bf97b-114">No se muestra la barra de título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="bf97b-114">The window title bar is not shown.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="bf97b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf97b-115">Remarks</span></span>

<span data-ttu-id="bf97b-116">Si se muestra la barra de título, se mostrarán los botones cuadro de control, minimizar y cerrar.</span><span class="sxs-lookup"><span data-stu-id="bf97b-116">If the title bar is shown, the control box, minimize, and close buttons will be shown.</span></span> <span data-ttu-id="bf97b-117">El título de la ventana será el título del elemento de **vista** .</span><span class="sxs-lookup"><span data-stu-id="bf97b-117">The title of the window will be the title of the **VIEW** element.</span></span>

<span data-ttu-id="bf97b-118">Si **TitleBar** está establecido en true y el usuario intenta cambiar el valor de **video. zoom**, el cambio no tendrá lugar a menos que la máscara supervise el **zoom** y tome las medidas adecuadas para cambiar el tamaño.</span><span class="sxs-lookup"><span data-stu-id="bf97b-118">If **titleBar** is set to true and the user attempts to change the value of **Video.zoom**, the change will not take place unless the skin monitors **zoom** and takes appropriate action to resize itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf97b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf97b-119">Requirements</span></span>



| <span data-ttu-id="bf97b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf97b-120">Requirement</span></span> | <span data-ttu-id="bf97b-121">Value</span><span class="sxs-lookup"><span data-stu-id="bf97b-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="bf97b-122">Versión</span><span class="sxs-lookup"><span data-stu-id="bf97b-122">Version</span></span><br/> | <span data-ttu-id="bf97b-123">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="bf97b-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf97b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf97b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf97b-125">**Elemento de vista**</span><span class="sxs-lookup"><span data-stu-id="bf97b-125">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="bf97b-126">**VER. título**</span><span class="sxs-lookup"><span data-stu-id="bf97b-126">**VIEW.title**</span></span>](view-title.md)
</dt> <dt>

[<span data-ttu-id="bf97b-127">**VÍDEO. zoom**</span><span class="sxs-lookup"><span data-stu-id="bf97b-127">**VIDEO.zoom**</span></span>](video-zoom.md)
</dt> </dl>

 

 





