---
title: Player. enableContextMenu
description: La propiedad enableContextMenu especifica o recupera un valor que indica si se debe habilitar el menú contextual, que aparece al hacer clic con el botón secundario del mouse.
ms.assetid: 736c8714-5650-4912-9e97-914a20137b91
keywords:
- Media Player de Windows Player. enableContextMenu
topic_type:
- apiref
api_name:
- Player.enableContextMenu
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324ab0f14b83621651869e715c1fd4a882ceb650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698674"
---
# <a name="playerenablecontextmenu"></a><span data-ttu-id="42b14-104">Player. enableContextMenu</span><span class="sxs-lookup"><span data-stu-id="42b14-104">Player.enableContextMenu</span></span>

<span data-ttu-id="42b14-105">La propiedad **enableContextMenu** especifica o recupera un valor que indica si se debe habilitar el menú contextual, que aparece al hacer clic con el botón secundario del mouse.</span><span class="sxs-lookup"><span data-stu-id="42b14-105">The **enableContextMenu** property specifies or retrieves a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="42b14-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42b14-106">Syntax</span></span>

<span data-ttu-id="42b14-107">*reproductor*. **enableContextMenu**</span><span class="sxs-lookup"><span data-stu-id="42b14-107">*player*.**enableContextMenu**</span></span>

## <a name="possible-values"></a><span data-ttu-id="42b14-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="42b14-108">Possible Values</span></span>

<span data-ttu-id="42b14-109">Esta propiedad es un valor booleano de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="42b14-109">This property is a read/write Boolean.</span></span>



| <span data-ttu-id="42b14-110">Value</span><span class="sxs-lookup"><span data-stu-id="42b14-110">Value</span></span> | <span data-ttu-id="42b14-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="42b14-111">Description</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="42b14-112">true</span><span class="sxs-lookup"><span data-stu-id="42b14-112">true</span></span>  | <span data-ttu-id="42b14-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="42b14-113">Default.</span></span> <span data-ttu-id="42b14-114">Habilita el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="42b14-114">Enable the context menu.</span></span> |
| <span data-ttu-id="42b14-115">false</span><span class="sxs-lookup"><span data-stu-id="42b14-115">false</span></span> | <span data-ttu-id="42b14-116">No habilite el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="42b14-116">Do not enable the context menu.</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="42b14-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42b14-117">Remarks</span></span>

<span data-ttu-id="42b14-118">Durante la reproducción a pantalla completa, Windows Media Player oculta el cursor del mouse cuando **enableContextMenu** es igual a false y **uiMode** es igual a "none".</span><span class="sxs-lookup"><span data-stu-id="42b14-118">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="42b14-119">**Windows Media Player 10 Mobile:** Esta propiedad no se admite.</span><span class="sxs-lookup"><span data-stu-id="42b14-119">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="42b14-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42b14-120">Requirements</span></span>



| <span data-ttu-id="42b14-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="42b14-121">Requirement</span></span> | <span data-ttu-id="42b14-122">Value</span><span class="sxs-lookup"><span data-stu-id="42b14-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="42b14-123">Versión</span><span class="sxs-lookup"><span data-stu-id="42b14-123">Version</span></span><br/> | <span data-ttu-id="42b14-124">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="42b14-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="42b14-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="42b14-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="42b14-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42b14-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42b14-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="42b14-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42b14-128">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="42b14-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





