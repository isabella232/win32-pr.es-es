---
title: Controls. STOP (método)
description: El método Stop detiene la reproducción del elemento multimedia. | Controls. STOP (método)
ms.assetid: ace95fde-9c94-4737-88f2-94321cbc687c
keywords:
- detener el método Windows Media Player
- método STOP Windows Media Player, clase Controls
- Clase Controls Windows Media Player, método STOP
topic_type:
- apiref
api_name:
- Controls.stop
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1ffc581fffbce0a341559e82c6bd196f712149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699605"
---
# <a name="controlsstop-method"></a><span data-ttu-id="08bd2-107">Controls. STOP (método)</span><span class="sxs-lookup"><span data-stu-id="08bd2-107">Controls.stop method</span></span>

<span data-ttu-id="08bd2-108">El método **Stop** detiene la reproducción del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="08bd2-108">The **stop** method stops playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="08bd2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08bd2-109">Syntax</span></span>


```JScript
Controls.stop()
```



## <a name="parameters"></a><span data-ttu-id="08bd2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08bd2-110">Parameters</span></span>

<span data-ttu-id="08bd2-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="08bd2-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="08bd2-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08bd2-112">Return value</span></span>

<span data-ttu-id="08bd2-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="08bd2-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="08bd2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08bd2-114">Remarks</span></span>

<span data-ttu-id="08bd2-115">Este método hace que Windows Media Player libere cualquier recurso del sistema que esté usando, como el dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="08bd2-115">This method causes Windows Media Player to release any system resources it is using, such as the audio device.</span></span> <span data-ttu-id="08bd2-116">Sin embargo, el elemento multimedia actual no se libera.</span><span class="sxs-lookup"><span data-stu-id="08bd2-116">The current media item, however, is not released.</span></span>

<span data-ttu-id="08bd2-117">Cuando se detiene el reproductor, la pista se rebobina hasta el principio.</span><span class="sxs-lookup"><span data-stu-id="08bd2-117">When the player is stopped, the track rewinds to the beginning.</span></span> <span data-ttu-id="08bd2-118">La llamada a **Play** iniciará la reproducción del clip desde el principio.</span><span class="sxs-lookup"><span data-stu-id="08bd2-118">Calling **play** will then begin playback of the clip from the beginning.</span></span> <span data-ttu-id="08bd2-119">Para detener una operación de reproducción sin cambiar la posición actual, use el método **PAUSE** .</span><span class="sxs-lookup"><span data-stu-id="08bd2-119">To halt a play operation without changing the current position, use the **pause** method.</span></span>

## <a name="examples"></a><span data-ttu-id="08bd2-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="08bd2-120">Examples</span></span>

<span data-ttu-id="08bd2-121">En el ejemplo siguiente se crea un elemento de botón HTML que usa **Stop** para detener la reproducción.</span><span class="sxs-lookup"><span data-stu-id="08bd2-121">The following example creates an HTML BUTTON element that uses **stop** to stop playback.</span></span> <span data-ttu-id="08bd2-122">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="08bd2-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "STOP"  NAME = "STOP"  VALUE = "Stop"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Stop'))

            /* Stop the Player. */
            Player.controls.stop();
">

```



## <a name="requirements"></a><span data-ttu-id="08bd2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08bd2-123">Requirements</span></span>



| <span data-ttu-id="08bd2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="08bd2-124">Requirement</span></span> | <span data-ttu-id="08bd2-125">Value</span><span class="sxs-lookup"><span data-stu-id="08bd2-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="08bd2-126">Versión</span><span class="sxs-lookup"><span data-stu-id="08bd2-126">Version</span></span><br/> | <span data-ttu-id="08bd2-127">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="08bd2-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="08bd2-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="08bd2-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="08bd2-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08bd2-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08bd2-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="08bd2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08bd2-131">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="08bd2-131">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="08bd2-132">**Controls. Next**</span><span class="sxs-lookup"><span data-stu-id="08bd2-132">**Controls.next**</span></span>](controls-next.md)
</dt> <dt>

[<span data-ttu-id="08bd2-133">**Controls. PAUSE**</span><span class="sxs-lookup"><span data-stu-id="08bd2-133">**Controls.pause**</span></span>](controls-pause.md)
</dt> <dt>

[<span data-ttu-id="08bd2-134">**Controls. Previous**</span><span class="sxs-lookup"><span data-stu-id="08bd2-134">**Controls.previous**</span></span>](controls-previous.md)
</dt> </dl>

 

 





