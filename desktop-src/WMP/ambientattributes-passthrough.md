---
title: AmbientAttributes. passThrough
description: El atributo passThrough especifica o recupera un valor que indica si el control pasará todos los eventos del mouse por el control situado bajo él.
ms.assetid: 907ae233-3421-4e80-84be-64db4a3ab654
keywords:
- AmbientAttributes. passThrough Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.passThrough
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b786aeefc182caab904c644dfd00ab4e76fec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699430"
---
# <a name="ambientattributespassthrough"></a><span data-ttu-id="32c28-104">AmbientAttributes. passThrough</span><span class="sxs-lookup"><span data-stu-id="32c28-104">AmbientAttributes.passThrough</span></span>

<span data-ttu-id="32c28-105">El atributo **passThrough** especifica o recupera un valor que indica si el control pasará todos los eventos del mouse por el control situado bajo él.</span><span class="sxs-lookup"><span data-stu-id="32c28-105">The **passThrough** attribute specifies or retrieves a value indicating whether the control will pass all mouse events through to the control under it.</span></span>

``` syntax
        elementID.passThrough
```

## <a name="possible-values"></a><span data-ttu-id="32c28-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="32c28-106">Possible Values</span></span>

<span data-ttu-id="32c28-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="32c28-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="32c28-108">Value</span><span class="sxs-lookup"><span data-stu-id="32c28-108">Value</span></span> | <span data-ttu-id="32c28-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="32c28-109">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="32c28-110">true</span><span class="sxs-lookup"><span data-stu-id="32c28-110">true</span></span>  | <span data-ttu-id="32c28-111">El control pasa los eventos a través del control.</span><span class="sxs-lookup"><span data-stu-id="32c28-111">Control passes events through to the control under it.</span></span> |
| <span data-ttu-id="32c28-112">false</span><span class="sxs-lookup"><span data-stu-id="32c28-112">false</span></span> | <span data-ttu-id="32c28-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="32c28-113">Default.</span></span> <span data-ttu-id="32c28-114">El control no pasa los eventos a través de.</span><span class="sxs-lookup"><span data-stu-id="32c28-114">Control does not pass events through.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="32c28-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32c28-115">Remarks</span></span>

<span data-ttu-id="32c28-116">Este atributo es útil si, por ejemplo, un control de texto se coloca sobre un control de botón solo para proporcionar etiquetas.</span><span class="sxs-lookup"><span data-stu-id="32c28-116">This attribute is useful if, for example, a text control sits on top of a button control only to provide labeling.</span></span> <span data-ttu-id="32c28-117">En este caso, los clics en el control de texto se deben pasar al control de botón.</span><span class="sxs-lookup"><span data-stu-id="32c28-117">In this case, clicks on the text control must be passed through to the button control.</span></span>

<span data-ttu-id="32c28-118">Los elementos de **vista**, **subvista** y **lista de reproducción** no admiten el atributo **passThrough** .</span><span class="sxs-lookup"><span data-stu-id="32c28-118">The **passThrough** attribute is not supported by the **VIEW**, **SUBVIEW**, and **PLAYLIST** elements.</span></span> <span data-ttu-id="32c28-119">No funcionará con el elemento de **vídeo** si se trata de un *vídeo*. **Windowless** está establecido en false, y en el elemento **Effects** si tiene *efectos*. **windowed** está establecido en true.</span><span class="sxs-lookup"><span data-stu-id="32c28-119">It will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if *EFFECTS*.**windowed** is set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="32c28-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32c28-120">Requirements</span></span>



| <span data-ttu-id="32c28-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="32c28-121">Requirement</span></span> | <span data-ttu-id="32c28-122">Value</span><span class="sxs-lookup"><span data-stu-id="32c28-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="32c28-123">Versión</span><span class="sxs-lookup"><span data-stu-id="32c28-123">Version</span></span><br/> | <span data-ttu-id="32c28-124">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="32c28-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="32c28-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="32c28-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32c28-126">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="32c28-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





