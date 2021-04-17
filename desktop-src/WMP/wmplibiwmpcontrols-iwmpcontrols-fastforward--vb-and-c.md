---
title: IWMPControls fastForward, método
description: El método fastForward inicia la reproducción rápida del elemento multimedia en la dirección de avance. | IWMPControls fastForward, método
ms.assetid: 44609d63-1d1a-489c-ac17-60b6d3ddc588
keywords:
- método fastForward de Windows Media Player
- método fastForward Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, método fastForward
topic_type:
- apiref
api_name:
- IWMPControls.fastForward
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d99307a7b188b238157af62833273b8c724eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690887"
---
# <a name="iwmpcontrolsfastforward-method"></a><span data-ttu-id="1d4b3-107">IWMPControls:: fastForward (método)</span><span class="sxs-lookup"><span data-stu-id="1d4b3-107">IWMPControls::fastForward method</span></span>

<span data-ttu-id="1d4b3-108">El método **fastForward** inicia la reproducción rápida del elemento multimedia en la dirección de avance.</span><span class="sxs-lookup"><span data-stu-id="1d4b3-108">The **fastForward** method starts fast play of the media item in the forward direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d4b3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d4b3-109">Syntax</span></span>


```CSharp
public void fastForward();
```


```VB

Public Sub fastForward()
Implements IWMPControls.fastForward
```





## <a name="parameters"></a><span data-ttu-id="1d4b3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d4b3-110">Parameters</span></span>

<span data-ttu-id="1d4b3-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1d4b3-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d4b3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d4b3-112">Return value</span></span>

<span data-ttu-id="1d4b3-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1d4b3-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d4b3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d4b3-114">Remarks</span></span>

<span data-ttu-id="1d4b3-115">El método **fastForward** reproduce el clip cinco veces la velocidad normal.</span><span class="sxs-lookup"><span data-stu-id="1d4b3-115">The **fastForward** method plays the clip at five times the normal speed.</span></span> <span data-ttu-id="1d4b3-116">Llamar a **fastForward** es equivalente a especificar 5,0 para la velocidad estableciendo la propiedad **IWMPSettings. rate** .</span><span class="sxs-lookup"><span data-stu-id="1d4b3-116">Calling **fastForward** is equivalent to specifying 5.0 for the rate by setting the **IWMPSettings.rate** property.</span></span> <span data-ttu-id="1d4b3-117">Si posteriormente se cambia la frecuencia, o si se llama a **IWMPControls. Play** o **IWMPControls. stop** , Windows Media Player dejará de reenviar rápidamente.</span><span class="sxs-lookup"><span data-stu-id="1d4b3-117">If the rate is subsequently changed, or if **IWMPControls.play** or **IWMPControls.stop** is called, Windows Media Player will cease fast forwarding.</span></span>

<span data-ttu-id="1d4b3-118">El método **fastForward** no funciona para las difusiones en vivo y determinados tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="1d4b3-118">The **fastForward** method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="1d4b3-119">Para determinar si puede avanzar rápidamente en un clip, pase el valor **System. String** "Fastforward" a la propiedad **IWMPControls. isavailable** (el método **IWMPControls. Get \_ isavailable** en C#).</span><span class="sxs-lookup"><span data-stu-id="1d4b3-119">To determine whether you can fast forward in a clip, pass the **System.String** value "FastForward" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="1d4b3-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1d4b3-120">Examples</span></span>

<span data-ttu-id="1d4b3-121">En el ejemplo siguiente se usa **fastForward** para reenviar rápidamente el elemento multimedia actual en respuesta al evento click de un botón.</span><span class="sxs-lookup"><span data-stu-id="1d4b3-121">The following example uses **fastForward** to fast-forward the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="1d4b3-122">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="1d4b3-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void fastForwardButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastForward"))
    {
        controls.fastForward();
    }
}
```


```VB

Public Sub fastForwardButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastForwardButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface. 
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastForward&quot;)) Then

        controls.fastForward()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="1d4b3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d4b3-123">Requirements</span></span>



| <span data-ttu-id="1d4b3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d4b3-124">Requirement</span></span> | <span data-ttu-id="1d4b3-125">Value</span><span class="sxs-lookup"><span data-stu-id="1d4b3-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d4b3-126">Versión</span><span class="sxs-lookup"><span data-stu-id="1d4b3-126">Version</span></span><br/>   | <span data-ttu-id="1d4b3-127">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="1d4b3-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1d4b3-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1d4b3-128">Namespace</span></span><br/> | <span data-ttu-id="1d4b3-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1d4b3-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1d4b3-130">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="1d4b3-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1d4b3-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1d4b3-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d4b3-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d4b3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d4b3-133">**Interfaz IWMPControls (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="1d4b3-133">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1d4b3-134">**IWMPControls. isAvailable (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="1d4b3-134">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1d4b3-135">**IWMPControls. Play (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="1d4b3-135">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1d4b3-136">**IWMPControls. STOP (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="1d4b3-136">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1d4b3-137">**IWMPSettings. Rate (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="1d4b3-137">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





