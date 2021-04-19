---
title: Controls. fastReverse (método)
description: El método fastReverse inicia el examen rápido del elemento multimedia en la dirección inversa.
ms.assetid: 4fc61739-9006-4d62-b2c1-2b8e8830f2d9
keywords:
- método fastReverse de Windows Media Player
- método fastReverse Windows Media Player, clase Controls
- Clase Controls Windows Media Player, método fastReverse
topic_type:
- apiref
api_name:
- Controls.fastReverse
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e5a63c4299bf08c25e36e2d61924f3fb171792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699566"
---
# <a name="controlsfastreverse-method"></a><span data-ttu-id="a1bb8-106">Controls. fastReverse (método)</span><span class="sxs-lookup"><span data-stu-id="a1bb8-106">Controls.fastReverse method</span></span>

<span data-ttu-id="a1bb8-107">El método **fastReverse** inicia el examen rápido del elemento multimedia en la dirección inversa.</span><span class="sxs-lookup"><span data-stu-id="a1bb8-107">The **fastReverse** method starts fast scanning of the media item in the reverse direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1bb8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1bb8-108">Syntax</span></span>


```JScript
Controls.fastReverse()
```



## <a name="parameters"></a><span data-ttu-id="a1bb8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1bb8-109">Parameters</span></span>

<span data-ttu-id="a1bb8-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a1bb8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a1bb8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1bb8-111">Return value</span></span>

<span data-ttu-id="a1bb8-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a1bb8-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1bb8-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1bb8-113">Remarks</span></span>

<span data-ttu-id="a1bb8-114">El método **fastReverse** recorre el clip en orden inverso cinco veces la velocidad normal, mostrando solo los fotogramas clave si se trata de un archivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a1bb8-114">The **fastReverse** method scans the clip in reverse at five times the normal speed, displaying only the key frames if it is a video file.</span></span> <span data-ttu-id="a1bb8-115">Al invocar **fastReverse** se cambia la *configuración*. propiedad **Rate** en 5,0.</span><span class="sxs-lookup"><span data-stu-id="a1bb8-115">Invoking **fastReverse** changes the *Settings*.**rate** property to  5.0.</span></span> <span data-ttu-id="a1bb8-116">Si la **velocidad** se cambia posteriormente, o si se llama a **Play** o **Stop** , Windows Media Player dejará de ser inversa rápido.</span><span class="sxs-lookup"><span data-stu-id="a1bb8-116">If **rate** is subsequently changed, or if **play** or **stop** is called, Windows Media Player will cease fast reverse.</span></span>

<span data-ttu-id="a1bb8-117">Si el elemento forma parte de una lista de reproducción, **fastReverse** se detiene al principio de la pista actual. Por ejemplo, si el seguimiento 3 está en **fastReverse**, cuando se alcanza el comienzo de la pista 3, Windows Media Player no irá al seguimiento 2.</span><span class="sxs-lookup"><span data-stu-id="a1bb8-117">If the item is part of a playlist, **fastReverse** stops at the beginning of the current track. For instance, if track 3 is in **fastReverse**, when the beginning of track 3 is reached, Windows Media Player will not go to track 2.</span></span> <span data-ttu-id="a1bb8-118">El recuento de reproducción no se incrementa al llamar a **fastReverse**.</span><span class="sxs-lookup"><span data-stu-id="a1bb8-118">The play count is not incremented when calling **fastReverse**.</span></span>

<span data-ttu-id="a1bb8-119">Si llama a **fastForward** mientras **fastReverse** está en vigor, **fastReverse** se detendrá y se iniciará **fastForward** .</span><span class="sxs-lookup"><span data-stu-id="a1bb8-119">If you call **fastForward** while **fastReverse** is in effect, **fastReverse** will be stopped and **fastForward** will begin.</span></span>

<span data-ttu-id="a1bb8-120">Este método no funciona para las difusiones en vivo y determinados tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="a1bb8-120">This method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="a1bb8-121">Para determinar si puede usar Fast Reverse en un clip, llame a **isavailable**("FastReverse").</span><span class="sxs-lookup"><span data-stu-id="a1bb8-121">To determine whether you can use fast reverse in a clip, call **isAvailable**("FastReverse").</span></span>

## <a name="examples"></a><span data-ttu-id="a1bb8-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a1bb8-122">Examples</span></span>

<span data-ttu-id="a1bb8-123">En el ejemplo siguiente se crea un elemento de botón HTML que usa **fastReverse** para iniciar la reproducción rápida y inversa del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="a1bb8-123">The following example creates an HTML BUTTON element that uses **fastReverse** to start fast-reverse play of the media item.</span></span> <span data-ttu-id="a1bb8-124">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="a1bb8-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "REW"  NAME = "REW"  VALUE = "<<"  

    /* Run JScript when the BUTTON is clicked. 
       Check first to make sure fast-reverse mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastReverse'))
        Player.controls.fastReverse();
">
```



## <a name="requirements"></a><span data-ttu-id="a1bb8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1bb8-125">Requirements</span></span>



| <span data-ttu-id="a1bb8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1bb8-126">Requirement</span></span> | <span data-ttu-id="a1bb8-127">Value</span><span class="sxs-lookup"><span data-stu-id="a1bb8-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1bb8-128">Versión</span><span class="sxs-lookup"><span data-stu-id="a1bb8-128">Version</span></span><br/> | <span data-ttu-id="a1bb8-129">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="a1bb8-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a1bb8-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a1bb8-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="a1bb8-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1bb8-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1bb8-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1bb8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1bb8-133">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="a1bb8-133">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="a1bb8-134">**Controls. fastForward**</span><span class="sxs-lookup"><span data-stu-id="a1bb8-134">**Controls.fastForward**</span></span>](controls-fastforward.md)
</dt> <dt>

[<span data-ttu-id="a1bb8-135">**Controls. isAvailable**</span><span class="sxs-lookup"><span data-stu-id="a1bb8-135">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> <dt>

[<span data-ttu-id="a1bb8-136">**Controls. Play**</span><span class="sxs-lookup"><span data-stu-id="a1bb8-136">**Controls.play**</span></span>](controls-play.md)
</dt> <dt>

[<span data-ttu-id="a1bb8-137">**Controls. STOP**</span><span class="sxs-lookup"><span data-stu-id="a1bb8-137">**Controls.stop**</span></span>](controls-stop.md)
</dt> <dt>

[<span data-ttu-id="a1bb8-138">**Settings. rate**</span><span class="sxs-lookup"><span data-stu-id="a1bb8-138">**Settings.rate**</span></span>](settings-rate.md)
</dt> </dl>

 

 





