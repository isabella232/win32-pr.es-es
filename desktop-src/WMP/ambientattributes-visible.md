---
title: AmbientAttributes. visible
description: El atributo visible especifica o recupera la visibilidad del control.
ms.assetid: 8347d42a-4af1-4ea1-b968-a2ae58278430
keywords:
- AmbientAttributes. visible Media Player de Windows
topic_type:
- apiref
api_name:
- AmbientAttributes.visible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72794b7bbba0237a687dc70bda761c505b839e59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700095"
---
# <a name="ambientattributesvisible"></a><span data-ttu-id="1532d-104">AmbientAttributes. visible</span><span class="sxs-lookup"><span data-stu-id="1532d-104">AmbientAttributes.visible</span></span>

<span data-ttu-id="1532d-105">El atributo **visible** especifica o recupera la visibilidad del control.</span><span class="sxs-lookup"><span data-stu-id="1532d-105">The **visible** attribute specifies or retrieves the visibility for the control.</span></span>

``` syntax
        elementID.visible
```

## <a name="possible-values"></a><span data-ttu-id="1532d-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="1532d-106">Possible Values</span></span>

<span data-ttu-id="1532d-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="1532d-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="1532d-108">Value</span><span class="sxs-lookup"><span data-stu-id="1532d-108">Value</span></span> | <span data-ttu-id="1532d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="1532d-109">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="1532d-110">true</span><span class="sxs-lookup"><span data-stu-id="1532d-110">true</span></span>  | <span data-ttu-id="1532d-111">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1532d-111">Default.</span></span> <span data-ttu-id="1532d-112">El control está visible.</span><span class="sxs-lookup"><span data-stu-id="1532d-112">The control is visible.</span></span> |
| <span data-ttu-id="1532d-113">false</span><span class="sxs-lookup"><span data-stu-id="1532d-113">false</span></span> | <span data-ttu-id="1532d-114">El control no se puede ver.</span><span class="sxs-lookup"><span data-stu-id="1532d-114">The control is not visible.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="1532d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1532d-115">Remarks</span></span>

<span data-ttu-id="1532d-116">Este atributo es útil para ocultar controles, por ejemplo, al intercambiar un botón de pausa para un botón de reproducción.</span><span class="sxs-lookup"><span data-stu-id="1532d-116">This attribute is useful for hiding controls, for example when swapping a pause button for a play button.</span></span>

<span data-ttu-id="1532d-117">Si el valor es false, el control no es visible y los eventos de clic se pasan al control subyacente.</span><span class="sxs-lookup"><span data-stu-id="1532d-117">If the value is false, the control is not visible and click events are passed to the control behind it.</span></span> <span data-ttu-id="1532d-118">Si el valor es true, el control es visible y recibe el propio evento de clic.</span><span class="sxs-lookup"><span data-stu-id="1532d-118">If the value is true, the control is visible and receives the click event itself.</span></span>

<span data-ttu-id="1532d-119">El valor predeterminado del elemento de **menú automenu** es false.</span><span class="sxs-lookup"><span data-stu-id="1532d-119">The default value for the **AUTOMENU** element is false.</span></span>

## <a name="requirements"></a><span data-ttu-id="1532d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1532d-120">Requirements</span></span>



| <span data-ttu-id="1532d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1532d-121">Requirement</span></span> | <span data-ttu-id="1532d-122">Value</span><span class="sxs-lookup"><span data-stu-id="1532d-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1532d-123">Versión</span><span class="sxs-lookup"><span data-stu-id="1532d-123">Version</span></span><br/> | <span data-ttu-id="1532d-124">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="1532d-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1532d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="1532d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1532d-126">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="1532d-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





