---
title: Player. windowlessVideo
description: La propiedad windowlessVideo especifica o recupera un valor que indica si el control de Windows Media Player representa el vídeo en el modo sin ventanas.
ms.assetid: 314a75a3-d096-4cd4-a747-e31367e0e265
keywords:
- Media Player de Windows Player. windowlessVideo
topic_type:
- apiref
api_name:
- Player.windowlessVideo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93f4a8a2b70a42cd0893d463eccca0427dde6c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708755"
---
# <a name="playerwindowlessvideo"></a><span data-ttu-id="cb4d5-104">Player. windowlessVideo</span><span class="sxs-lookup"><span data-stu-id="cb4d5-104">Player.windowlessVideo</span></span>

<span data-ttu-id="cb4d5-105">La propiedad **windowlessVideo** especifica o recupera un valor que indica si el control de Windows Media Player representa el vídeo en el modo sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-105">The **windowlessVideo** property specifies or retrieves a value indicating whether the Windows Media Player control renders video in windowless mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb4d5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb4d5-106">Syntax</span></span>

<span data-ttu-id="cb4d5-107">*reproductor*. **windowlessVideo**</span><span class="sxs-lookup"><span data-stu-id="cb4d5-107">*player*.**windowlessVideo**</span></span>

## <a name="possible-values"></a><span data-ttu-id="cb4d5-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="cb4d5-108">Possible Values</span></span>

<span data-ttu-id="cb4d5-109">Esta propiedad es un **valor booleano** que se especifica en tiempo de diseño y, a partir de ese momento, es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-109">This property is a **Boolean** that is specified at design time and is read-only thereafter.</span></span>



| <span data-ttu-id="cb4d5-110">Value</span><span class="sxs-lookup"><span data-stu-id="cb4d5-110">Value</span></span> | <span data-ttu-id="cb4d5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb4d5-111">Description</span></span>                                      |
|-------|--------------------------------------------------|
| <span data-ttu-id="cb4d5-112">true</span><span class="sxs-lookup"><span data-stu-id="cb4d5-112">true</span></span>  | <span data-ttu-id="cb4d5-113">El vídeo se representa en el modo sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-113">The video is rendered in windowless mode.</span></span>        |
| <span data-ttu-id="cb4d5-114">false</span><span class="sxs-lookup"><span data-stu-id="cb4d5-114">false</span></span> | <span data-ttu-id="cb4d5-115">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-115">Default.</span></span> <span data-ttu-id="cb4d5-116">El vídeo se representa en modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-116">The video is rendered in windowed mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="cb4d5-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb4d5-117">Remarks</span></span>

<span data-ttu-id="cb4d5-118">De forma predeterminada, un control incrustado de Windows Media Player representa el vídeo en su propia ventana dentro del área cliente.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-118">By default, an embedded Windows Media Player control renders video in its own window within the client area.</span></span> <span data-ttu-id="cb4d5-119">Cuando **windowlessVideo** se establece en true, el control Player representa el vídeo directamente en el área cliente, por lo que puede aplicar efectos especiales o capas el vídeo con texto.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-119">When **windowlessVideo** is set to true, the Player control renders video directly in the client area, so you can apply special effects or layer the video with text.</span></span>

<span data-ttu-id="cb4d5-120">En Windows Vista, la representación de vídeo en el modo sin ventanas puede degradar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-120">In Windows Vista, rendering video in windowless mode can degrade performance.</span></span>

<span data-ttu-id="cb4d5-121">La propiedad **windowlessVideo** no es compatible con Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-121">The **windowlessVideo** property is not supported for Netscape Navigator.</span></span> <span data-ttu-id="cb4d5-122">Establecer un valor para esta propiedad en el navegador puede producir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-122">Setting a value for this property in Navigator may yield unexpected results.</span></span>

<span data-ttu-id="cb4d5-123">**Windows Media Player 10 Mobile:** Esta propiedad no se admite.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-123">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb4d5-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb4d5-124">Requirements</span></span>



| <span data-ttu-id="cb4d5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb4d5-125">Requirement</span></span> | <span data-ttu-id="cb4d5-126">Value</span><span class="sxs-lookup"><span data-stu-id="cb4d5-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4d5-127">Versión</span><span class="sxs-lookup"><span data-stu-id="cb4d5-127">Version</span></span><br/> | <span data-ttu-id="cb4d5-128">Windows Media Player para Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="cb4d5-128">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="cb4d5-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cb4d5-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="cb4d5-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb4d5-130"><dt>Wmp.dll</dt></span></span> </dl> |



 

 





