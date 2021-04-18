---
title: Controls. PAUSE (método)
description: El método PAUSE pausa la reproducción del elemento multimedia. | Controls. PAUSE (método)
ms.assetid: 7307a3b2-e5d6-4067-bdb5-38011565142a
keywords:
- pausar el método Windows Media Player
- pausar método Windows Media Player, clase Controls
- Clase Controls Windows Media Player, PAUSE (método)
topic_type:
- apiref
api_name:
- Controls.pause
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 898efb51355a1301bc76717f6d0184d0b30d619d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700037"
---
# <a name="controlspause-method"></a><span data-ttu-id="f083a-107">Controls. PAUSE (método)</span><span class="sxs-lookup"><span data-stu-id="f083a-107">Controls.pause method</span></span>

<span data-ttu-id="f083a-108">El método **PAUSE pausa** la reproducción del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="f083a-108">The **pause** method pauses playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="f083a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f083a-109">Syntax</span></span>


```JScript
Controls.pause()
```



## <a name="parameters"></a><span data-ttu-id="f083a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f083a-110">Parameters</span></span>

<span data-ttu-id="f083a-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f083a-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f083a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f083a-112">Return value</span></span>

<span data-ttu-id="f083a-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f083a-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f083a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f083a-114">Remarks</span></span>

<span data-ttu-id="f083a-115">Cuando un archivo está en pausa, Windows Media Player no proporciona ningún recurso del sistema, como el dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="f083a-115">When a file is paused, Windows Media Player does not give up any system resources, such as the audio device.</span></span>

<span data-ttu-id="f083a-116">Algunos tipos de medios no se pueden pausar, como las secuencias en directo.</span><span class="sxs-lookup"><span data-stu-id="f083a-116">Certain media types cannot be paused, such as live streams.</span></span> <span data-ttu-id="f083a-117">Para determinar si se puede pausar un tipo de medio determinado, use *los controles*. **isavailable (' Pause ')**.</span><span class="sxs-lookup"><span data-stu-id="f083a-117">To determine whether a particular media type can be paused, use *Controls*.**isAvailable('Pause')**.</span></span>

## <a name="examples"></a><span data-ttu-id="f083a-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f083a-118">Examples</span></span>

<span data-ttu-id="f083a-119">En el ejemplo siguiente se crea un elemento de botón HTML que usa **PAUSE** para pausar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="f083a-119">The following example creates an HTML BUTTON element that uses **pause** to pause playback.</span></span> <span data-ttu-id="f083a-120">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f083a-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PAUSE"  NAME = "PAUSE"  VALUE = "||"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Pause'))

            /* Pause the Player. */
            Player.controls.pause();
">
```



## <a name="requirements"></a><span data-ttu-id="f083a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f083a-121">Requirements</span></span>



| <span data-ttu-id="f083a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f083a-122">Requirement</span></span> | <span data-ttu-id="f083a-123">Value</span><span class="sxs-lookup"><span data-stu-id="f083a-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f083a-124">Versión</span><span class="sxs-lookup"><span data-stu-id="f083a-124">Version</span></span><br/> | <span data-ttu-id="f083a-125">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="f083a-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f083a-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f083a-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="f083a-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f083a-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f083a-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f083a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f083a-129">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="f083a-129">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="f083a-130">**Controls. isAvailable**</span><span class="sxs-lookup"><span data-stu-id="f083a-130">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> </dl>

 

 





