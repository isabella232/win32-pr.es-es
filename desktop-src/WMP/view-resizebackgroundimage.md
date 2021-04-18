---
title: VER. resizeBackgroundImage
description: El atributo resizeBackgroundImage especifica o recupera un valor que indica si se puede cambiar el tamaño de la imagen de fondo.
ms.assetid: d18f3def-777f-4a71-961e-73bae98a4c64
keywords:
- VIEW. resizeBackgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.resizeBackgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397929d69cc6ac6ad51c29883898c153218afdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718608"
---
# <a name="viewresizebackgroundimage"></a><span data-ttu-id="a7018-104">VER. resizeBackgroundImage</span><span class="sxs-lookup"><span data-stu-id="a7018-104">VIEW.resizeBackgroundImage</span></span>

<span data-ttu-id="a7018-105">El atributo **resizeBackgroundImage** especifica o recupera un valor que indica si se puede cambiar el tamaño de la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="a7018-105">The **resizeBackgroundImage** attribute specifies or retrieves a value indicating whether the background image can be resized.</span></span>

``` syntax
        elementID.resizeBackgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="a7018-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="a7018-106">Possible Values</span></span>

<span data-ttu-id="a7018-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="a7018-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="a7018-108">Valores</span><span class="sxs-lookup"><span data-stu-id="a7018-108">Values</span></span> | <span data-ttu-id="a7018-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7018-109">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="a7018-110">true</span><span class="sxs-lookup"><span data-stu-id="a7018-110">true</span></span>   | <span data-ttu-id="a7018-111">Se puede cambiar el tamaño de la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="a7018-111">The background image can be resized.</span></span>             |
| <span data-ttu-id="a7018-112">false</span><span class="sxs-lookup"><span data-stu-id="a7018-112">false</span></span>  | <span data-ttu-id="a7018-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a7018-113">Default.</span></span> <span data-ttu-id="a7018-114">No se puede cambiar el tamaño de la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="a7018-114">The background image cannot be resized.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a7018-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7018-115">Remarks</span></span>

<span data-ttu-id="a7018-116">Si establece este atributo en true, la imagen de fondo cambiará de tamaño para ajustarse a los valores actuales de los atributos de **ancho** y **alto** .</span><span class="sxs-lookup"><span data-stu-id="a7018-116">If you set this attribute to true, the background image will resize to fit the current values of the **width** and **height** attributes.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7018-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7018-117">Requirements</span></span>



| <span data-ttu-id="a7018-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7018-118">Requirement</span></span> | <span data-ttu-id="a7018-119">Value</span><span class="sxs-lookup"><span data-stu-id="a7018-119">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="a7018-120">Versión</span><span class="sxs-lookup"><span data-stu-id="a7018-120">Version</span></span><br/> | <span data-ttu-id="a7018-121">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="a7018-121">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a7018-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7018-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7018-123">**Elemento de vista**</span><span class="sxs-lookup"><span data-stu-id="a7018-123">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="a7018-124">**VIEW. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="a7018-124">**VIEW.backgroundImage**</span></span>](view-backgroundimage.md)
</dt> </dl>

 

 





