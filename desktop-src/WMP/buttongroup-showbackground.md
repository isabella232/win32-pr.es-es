---
title: BUTTONGROUP.showBackground
description: El atributo showBackground especifica o recupera un valor que indica si el BUTTONGROUP muestra solo los botones o muestra el mapa de bits completo especificado en el atributo de imagen.
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- BUTTONGROUP. showBackground Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.showBackground
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31cc87260d4b0fca74d6063c757e6c3dae0db850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699518"
---
# <a name="buttongroupshowbackground"></a><span data-ttu-id="3f66b-104">BUTTONGROUP.showBackground</span><span class="sxs-lookup"><span data-stu-id="3f66b-104">BUTTONGROUP.showBackground</span></span>

<span data-ttu-id="3f66b-105">El atributo **showBackground** especifica o recupera un valor que indica si el **BUTTONGROUP** muestra solo los botones o muestra el mapa de bits completo especificado en el atributo de **imagen** .</span><span class="sxs-lookup"><span data-stu-id="3f66b-105">The **showBackground** attribute specifies or retrieves a value indicating whether the **BUTTONGROUP** displays only the buttons, or displays the full bitmap specified in the **image** attribute.</span></span>

``` syntax
        elementID.showBackground
```

## <a name="possible-values"></a><span data-ttu-id="3f66b-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="3f66b-106">Possible Values</span></span>

<span data-ttu-id="3f66b-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="3f66b-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="3f66b-108">Value</span><span class="sxs-lookup"><span data-stu-id="3f66b-108">Value</span></span> | <span data-ttu-id="3f66b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f66b-109">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f66b-110">true</span><span class="sxs-lookup"><span data-stu-id="3f66b-110">true</span></span>  | <span data-ttu-id="3f66b-111">Se muestran los botones y el área no ocupada por los botones se dibuja desde el mapa de bits de la imagen.</span><span class="sxs-lookup"><span data-stu-id="3f66b-111">Buttons are displayed and the area not occupied by buttons is drawn from the Image bitmap.</span></span> |
| <span data-ttu-id="3f66b-112">false</span><span class="sxs-lookup"><span data-stu-id="3f66b-112">false</span></span> | <span data-ttu-id="3f66b-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3f66b-113">Default.</span></span> <span data-ttu-id="3f66b-114">Solo se muestran los botones.</span><span class="sxs-lookup"><span data-stu-id="3f66b-114">Only the buttons are displayed.</span></span>                                                   |



 

## <a name="remarks"></a><span data-ttu-id="3f66b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f66b-115">Remarks</span></span>

<span data-ttu-id="3f66b-116">Cuando **showBackground** es true, toda la **imagen** principal será visible.</span><span class="sxs-lookup"><span data-stu-id="3f66b-116">When **showBackground** is true, the entire main **image** will be visible.</span></span>

<span data-ttu-id="3f66b-117">Cuando **showBackground** es false, solo se representarán las áreas correspondientes a los colores **mappingImage** asignados.</span><span class="sxs-lookup"><span data-stu-id="3f66b-117">When **showBackground** is false, only the areas corresponding to assigned **mappingImage** colors will be rendered.</span></span> <span data-ttu-id="3f66b-118">En otras palabras, solo estarán visibles los **BUTTONELEMENTs** con sus **mappingColor** asignados.</span><span class="sxs-lookup"><span data-stu-id="3f66b-118">In other words, only **BUTTONELEMENTs** with their **mappingColor** assigned will be visible.</span></span>

<span data-ttu-id="3f66b-119">Si se especifica un valor no válido, se mantiene el estado anterior.</span><span class="sxs-lookup"><span data-stu-id="3f66b-119">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f66b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f66b-120">Requirements</span></span>



| <span data-ttu-id="3f66b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f66b-121">Requirement</span></span> | <span data-ttu-id="3f66b-122">Value</span><span class="sxs-lookup"><span data-stu-id="3f66b-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3f66b-123">Versión</span><span class="sxs-lookup"><span data-stu-id="3f66b-123">Version</span></span><br/> | <span data-ttu-id="3f66b-124">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="3f66b-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3f66b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f66b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f66b-126">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="3f66b-126">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="3f66b-127">**BUTTONELEMENT. mappingColor**</span><span class="sxs-lookup"><span data-stu-id="3f66b-127">**BUTTONELEMENT.mappingColor**</span></span>](buttonelement-mappingcolor.md)
</dt> <dt>

[<span data-ttu-id="3f66b-128">**BUTTONGROUP. Image**</span><span class="sxs-lookup"><span data-stu-id="3f66b-128">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="3f66b-129">**BUTTONGROUP.mappingImage**</span><span class="sxs-lookup"><span data-stu-id="3f66b-129">**BUTTONGROUP.mappingImage**</span></span>](buttongroup-mappingimage.md)
</dt> </dl>

 

 





