---
title: EFFECTs. fullScreen
description: El atributo fullScreen especifica o recupera un valor que indica si la visualización actual se muestra en pantalla completa. Este atributo solo se puede establecer en tiempo de ejecución.
ms.assetid: 319b46a4-b6c2-4dda-8285-f12af6836b25
keywords:
- EFFECTs. fullScreen Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e1824e35793a083eb88ea42de0eb8858a4b76f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700241"
---
# <a name="effectsfullscreen"></a><span data-ttu-id="7efc7-105">EFFECTs. fullScreen</span><span class="sxs-lookup"><span data-stu-id="7efc7-105">EFFECTS.fullScreen</span></span>

<span data-ttu-id="7efc7-106">El atributo **Fullscreen** especifica o recupera un valor que indica si la visualización actual se muestra en pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="7efc7-106">The **fullScreen** attribute specifies or retrieves a value indicating whether the current visualization is displayed full-screen.</span></span> <span data-ttu-id="7efc7-107">Este atributo solo se puede establecer en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="7efc7-107">This attribute can only be set at run time.</span></span>

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a><span data-ttu-id="7efc7-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="7efc7-108">Possible Values</span></span>

<span data-ttu-id="7efc7-109">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="7efc7-109">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="7efc7-110">Value</span><span class="sxs-lookup"><span data-stu-id="7efc7-110">Value</span></span> | <span data-ttu-id="7efc7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7efc7-111">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="7efc7-112">true</span><span class="sxs-lookup"><span data-stu-id="7efc7-112">true</span></span>  | <span data-ttu-id="7efc7-113">La visualización se muestra en pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="7efc7-113">Visualization is displayed full-screen.</span></span>              |
| <span data-ttu-id="7efc7-114">false</span><span class="sxs-lookup"><span data-stu-id="7efc7-114">false</span></span> | <span data-ttu-id="7efc7-115">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7efc7-115">Default.</span></span> <span data-ttu-id="7efc7-116">La visualización no se muestra en pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="7efc7-116">Visualization is not displayed full-screen.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7efc7-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7efc7-117">Remarks</span></span>

<span data-ttu-id="7efc7-118">Una visualización solo se puede poner en modo de pantalla completa mientras el contenido multimedia se reproduce o está en pausa.</span><span class="sxs-lookup"><span data-stu-id="7efc7-118">A visualization can be put into full-screen mode only while media is playing or paused.</span></span> <span data-ttu-id="7efc7-119">Si es *Player*. **currentMedia** es un vídeo, un complemento de vídeo debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="7efc7-119">If *Player*.**currentMedia** is video, a video plug-in must be present.</span></span> <span data-ttu-id="7efc7-120">Si es audio, debe existir un complemento de visualización que admita la presentación en pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="7efc7-120">If it is audio, a visualization plug-in that supports full-screen display must be present.</span></span>

## <a name="requirements"></a><span data-ttu-id="7efc7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7efc7-121">Requirements</span></span>



| <span data-ttu-id="7efc7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7efc7-122">Requirement</span></span> | <span data-ttu-id="7efc7-123">Value</span><span class="sxs-lookup"><span data-stu-id="7efc7-123">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7efc7-124">Versión</span><span class="sxs-lookup"><span data-stu-id="7efc7-124">Version</span></span><br/> | <span data-ttu-id="7efc7-125">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="7efc7-125">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7efc7-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7efc7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7efc7-127">**EFFECTs, elemento**</span><span class="sxs-lookup"><span data-stu-id="7efc7-127">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





