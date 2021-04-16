---
title: Controls. fastForward (método)
description: El método fastForward inicia la reproducción rápida del elemento multimedia en la dirección de avance. | Controls. fastForward (método)
ms.assetid: 69cee803-f76b-4a8c-a2c2-1870665afaf9
keywords:
- método fastForward de Windows Media Player
- método fastForward Windows Media Player, clase Controls
- Clase Controls Windows Media Player, método fastForward
topic_type:
- apiref
api_name:
- Controls.fastForward
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20d033b8b025955e57a9c3ebed00a6d7a92a666e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699567"
---
# <a name="controlsfastforward-method"></a><span data-ttu-id="6051e-107">Controls. fastForward (método)</span><span class="sxs-lookup"><span data-stu-id="6051e-107">Controls.fastForward method</span></span>

<span data-ttu-id="6051e-108">El método **fastForward** inicia la reproducción rápida del elemento multimedia en la dirección de avance.</span><span class="sxs-lookup"><span data-stu-id="6051e-108">The **fastForward** method starts fast play of the media item in the forward direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="6051e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6051e-109">Syntax</span></span>


```JScript
Controls.fastForward()
```



## <a name="parameters"></a><span data-ttu-id="6051e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6051e-110">Parameters</span></span>

<span data-ttu-id="6051e-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6051e-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6051e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6051e-112">Return value</span></span>

<span data-ttu-id="6051e-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6051e-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6051e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6051e-114">Remarks</span></span>

<span data-ttu-id="6051e-115">El método **fastForward** vuelve a reproducir el clip cinco veces la velocidad normal.</span><span class="sxs-lookup"><span data-stu-id="6051e-115">The **fastForward** method plays the clip back at five times the normal speed.</span></span> <span data-ttu-id="6051e-116">Al invocar **fastForward** se cambia la *configuración*. propiedad **Rate** en 5,0.</span><span class="sxs-lookup"><span data-stu-id="6051e-116">Invoking **fastForward** changes the *Settings*.**rate** property to 5.0.</span></span> <span data-ttu-id="6051e-117">Si la **velocidad** se cambia posteriormente, o si se llama a **Play** o **Stop** , Windows Media Player dejará de reenviarse rápidamente.</span><span class="sxs-lookup"><span data-stu-id="6051e-117">If **rate** is subsequently changed, or if **play** or **stop** is called, Windows Media Player will cease fast forwarding.</span></span>

<span data-ttu-id="6051e-118">El método **fastForward** no funciona para las difusiones en vivo y determinados tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="6051e-118">The **fastForward** method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="6051e-119">Para determinar si puede avanzar rápidamente en un clip, llame a **isavailable**("Fastforward").</span><span class="sxs-lookup"><span data-stu-id="6051e-119">To determine whether you can fast forward in a clip, call **isAvailable**("FastForward").</span></span>

## <a name="examples"></a><span data-ttu-id="6051e-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6051e-120">Examples</span></span>

<span data-ttu-id="6051e-121">En el ejemplo siguiente se crea un elemento de botón HTML que usa **fastForward** para iniciar la reproducción rápida del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="6051e-121">The following example creates an HTML BUTTON element that uses **fastForward** to start fast play of the media item.</span></span> <span data-ttu-id="6051e-122">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="6051e-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "FF"  NAME = "FF"  VALUE = ">>"  

    /* Execute JScript when the BUTTON is clicked. 
       Check first to make sure fast-forward mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastForward'))
        Player.controls.fastForward();
">

```



## <a name="requirements"></a><span data-ttu-id="6051e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6051e-123">Requirements</span></span>



| <span data-ttu-id="6051e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6051e-124">Requirement</span></span> | <span data-ttu-id="6051e-125">Value</span><span class="sxs-lookup"><span data-stu-id="6051e-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6051e-126">Versión</span><span class="sxs-lookup"><span data-stu-id="6051e-126">Version</span></span><br/> | <span data-ttu-id="6051e-127">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="6051e-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6051e-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6051e-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="6051e-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6051e-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6051e-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="6051e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6051e-131">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="6051e-131">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="6051e-132">**Controls. isAvailable**</span><span class="sxs-lookup"><span data-stu-id="6051e-132">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> <dt>

[<span data-ttu-id="6051e-133">**Controls. Play**</span><span class="sxs-lookup"><span data-stu-id="6051e-133">**Controls.play**</span></span>](controls-play.md)
</dt> <dt>

[<span data-ttu-id="6051e-134">**Controls. STOP**</span><span class="sxs-lookup"><span data-stu-id="6051e-134">**Controls.stop**</span></span>](controls-stop.md)
</dt> <dt>

[<span data-ttu-id="6051e-135">**Settings. rate**</span><span class="sxs-lookup"><span data-stu-id="6051e-135">**Settings.rate**</span></span>](settings-rate.md)
</dt> </dl>

 

 





