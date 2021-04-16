---
title: Player. stretchToFit
description: La propiedad stretchToFit especifica o recupera un valor que indica si el vídeo mostrado por el control Media Player de Windows ajusta automáticamente su tamaño para ajustarse a la ventana de vídeo, cuando la ventana de vídeo es mayor que las dimensiones de la imagen de vídeo.
ms.assetid: 9ea02959-602e-4bac-a8aa-dce502d1bb54
keywords:
- Media Player de Windows Player. stretchToFit
topic_type:
- apiref
api_name:
- Player.stretchToFit
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7b68042cf2a5bd0e7f718d1e19641edecdf548
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708244"
---
# <a name="playerstretchtofit"></a><span data-ttu-id="e68f7-104">Player. stretchToFit</span><span class="sxs-lookup"><span data-stu-id="e68f7-104">Player.stretchToFit</span></span>

<span data-ttu-id="e68f7-105">La propiedad **stretchToFit** especifica o recupera un valor que indica si el vídeo mostrado por el control Media Player de Windows ajusta automáticamente su tamaño para ajustarse a la ventana de vídeo, cuando la ventana de vídeo es mayor que las dimensiones de la imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e68f7-105">The **stretchToFit** property specifies or retrieves a value indicating whether video displayed by the Windows Media Player control automatically sizes to fit the video window, when the video window is larger than the dimensions of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="e68f7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e68f7-106">Syntax</span></span>

<span data-ttu-id="e68f7-107">*reproductor*. **stretchToFit**</span><span class="sxs-lookup"><span data-stu-id="e68f7-107">*player*.**stretchToFit**</span></span>

## <a name="possible-values"></a><span data-ttu-id="e68f7-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="e68f7-108">Possible Values</span></span>

<span data-ttu-id="e68f7-109">Esta propiedad es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="e68f7-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="e68f7-110">Value</span><span class="sxs-lookup"><span data-stu-id="e68f7-110">Value</span></span> | <span data-ttu-id="e68f7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e68f7-111">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="e68f7-112">true</span><span class="sxs-lookup"><span data-stu-id="e68f7-112">true</span></span>  | <span data-ttu-id="e68f7-113">El vídeo se ajustará para ajustarse a la ventana.</span><span class="sxs-lookup"><span data-stu-id="e68f7-113">The video will stretch to fit the window.</span></span>              |
| <span data-ttu-id="e68f7-114">false</span><span class="sxs-lookup"><span data-stu-id="e68f7-114">false</span></span> | <span data-ttu-id="e68f7-115">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e68f7-115">Default.</span></span> <span data-ttu-id="e68f7-116">El vídeo no se ajustará para ajustarse a la ventana.</span><span class="sxs-lookup"><span data-stu-id="e68f7-116">The video will not stretch to fit the window.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e68f7-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e68f7-117">Remarks</span></span>

<span data-ttu-id="e68f7-118">Cuando **stretchToFit** se establece en true, el control de Media Player de Windows mantiene la relación de aspecto original del vídeo.</span><span class="sxs-lookup"><span data-stu-id="e68f7-118">When **stretchToFit** is set to true, the Windows Media Player control maintains the original aspect ratio of the video.</span></span> <span data-ttu-id="e68f7-119">Si la relación de aspecto del vídeo no coincide con la relación de aspecto de la ventana de vídeo, pueden aparecer áreas de máscara negra en la parte superior e inferior, o izquierda y derecha, de la imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e68f7-119">If the aspect ratio of the video does not match the aspect ratio of the video window, black mask areas may appear on either the top and the bottom, or left and right, of the video image.</span></span>

<span data-ttu-id="e68f7-120">Esta propiedad solo se aplica al control Media Player de Windows cuando se incrusta en una página web.</span><span class="sxs-lookup"><span data-stu-id="e68f7-120">This property applies to the Windows Media Player control only when embedded in a webpage.</span></span>

<span data-ttu-id="e68f7-121">**Windows Media Player 10 Mobile:** Esta propiedad no se admite.</span><span class="sxs-lookup"><span data-stu-id="e68f7-121">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="e68f7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e68f7-122">Requirements</span></span>



| <span data-ttu-id="e68f7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e68f7-123">Requirement</span></span> | <span data-ttu-id="e68f7-124">Value</span><span class="sxs-lookup"><span data-stu-id="e68f7-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e68f7-125">Versión</span><span class="sxs-lookup"><span data-stu-id="e68f7-125">Version</span></span><br/> | <span data-ttu-id="e68f7-126">Windows Media Player versión 7,1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="e68f7-126">Windows Media Player version 7.1 or later.</span></span><br/>                              |
| <span data-ttu-id="e68f7-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e68f7-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="e68f7-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e68f7-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e68f7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e68f7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e68f7-130">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="e68f7-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





