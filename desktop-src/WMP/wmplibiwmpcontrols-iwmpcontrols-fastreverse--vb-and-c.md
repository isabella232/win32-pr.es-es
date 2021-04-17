---
title: IWMPControls fastReverse, método
description: El método fastReverse inicia la reproducción rápida del elemento multimedia en la dirección inversa.
ms.assetid: 5c872e8d-2ffc-425f-a4dd-938ddd1426e0
keywords:
- método fastReverse de Windows Media Player
- método fastReverse Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, método fastReverse
topic_type:
- apiref
api_name:
- IWMPControls.fastReverse
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061481aea13b0ed83c3a3d0eb47ca24b940358b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690884"
---
# <a name="iwmpcontrolsfastreverse-method"></a><span data-ttu-id="390f7-106">IWMPControls:: fastReverse (método)</span><span class="sxs-lookup"><span data-stu-id="390f7-106">IWMPControls::fastReverse method</span></span>

<span data-ttu-id="390f7-107">El método **fastReverse** inicia la reproducción rápida del elemento multimedia en la dirección inversa.</span><span class="sxs-lookup"><span data-stu-id="390f7-107">The **fastReverse** method starts fast play of the media item in the reverse direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="390f7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="390f7-108">Syntax</span></span>


```CSharp
public void fastReverse();
```


```VB

Public Sub fastReverse()
Implements IWMPControls.fastReverse
```





## <a name="parameters"></a><span data-ttu-id="390f7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="390f7-109">Parameters</span></span>

<span data-ttu-id="390f7-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="390f7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="390f7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="390f7-111">Return value</span></span>

<span data-ttu-id="390f7-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="390f7-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="390f7-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="390f7-113">Remarks</span></span>

<span data-ttu-id="390f7-114">El método **fastReverse** recorre el clip en orden inverso cinco veces la velocidad normal, mostrando solo los fotogramas clave si se trata de un archivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="390f7-114">The **fastReverse** method scans the clip in reverse at five times the normal speed, displaying only the key frames if it is a video file.</span></span> <span data-ttu-id="390f7-115">Llamar a **fastReverse** es equivalente a especificar-5,0 para la tasa estableciendo la propiedad **IWMPSettings. rate** .</span><span class="sxs-lookup"><span data-stu-id="390f7-115">Calling **fastReverse** is equivalent to specifying -5.0 for the rate by setting the **IWMPSettings.rate** property.</span></span> <span data-ttu-id="390f7-116">Si posteriormente se cambia la frecuencia, o si se llama a **IWMPControls. Play** o **IWMPControls. stop** , Windows Media Player dejará de ser inversa rápido.</span><span class="sxs-lookup"><span data-stu-id="390f7-116">If the rate is subsequently changed, or if **IWMPControls.play** or **IWMPControls.stop** is called, Windows Media Player will cease fast reverse.</span></span>

<span data-ttu-id="390f7-117">Si el elemento forma parte de una lista de reproducción, **fastReverse** se detiene al principio de la pista actual. Por ejemplo, si el seguimiento 3 está en **fastReverse**, cuando se alcanza el comienzo de la pista 3, Windows Media Player no irá al seguimiento 2.</span><span class="sxs-lookup"><span data-stu-id="390f7-117">If the item is part of a playlist, **fastReverse** stops at the beginning of the current track. For instance, if track 3 is in **fastReverse**, when the beginning of track 3 is reached, Windows Media Player will not go to track 2.</span></span> <span data-ttu-id="390f7-118">El recuento de reproducción no se incrementa al llamar a **fastReverse**.</span><span class="sxs-lookup"><span data-stu-id="390f7-118">The play count is not incremented when calling **fastReverse**.</span></span>

<span data-ttu-id="390f7-119">Si llama a **IWMPControls. fastForward** mientras **fastReverse** se está ejecutando, se detendrá **fastReverse** y **IWMPControls. fastForward** comenzará.</span><span class="sxs-lookup"><span data-stu-id="390f7-119">If you call **IWMPControls.fastForward** while **fastReverse** is running, **fastReverse** will be stopped and **IWMPControls.fastForward** will begin.</span></span>

<span data-ttu-id="390f7-120">Este método no funciona para las difusiones en vivo y determinados tipos de medios digitales.</span><span class="sxs-lookup"><span data-stu-id="390f7-120">This method does not work for live broadcasts and certain digital media types.</span></span> <span data-ttu-id="390f7-121">Para determinar si puede usar Fast inverso en un clip, pase el valor **System. String** "FastReverse" a la propiedad **IWMPControls. isavailable** (el método **IWMPControls. Get \_ isavailable** en C#).</span><span class="sxs-lookup"><span data-stu-id="390f7-121">To determine whether you can use fast reverse in a clip, pass the **System.String** value "FastReverse" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="390f7-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="390f7-122">Examples</span></span>

<span data-ttu-id="390f7-123">En el ejemplo siguiente se usa **fastReverse** para invertir el elemento multimedia actual en respuesta al evento click de un botón.</span><span class="sxs-lookup"><span data-stu-id="390f7-123">The following example uses **fastReverse** to reverse the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="390f7-124">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="390f7-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void fastReverseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastReverse"))
    {
        controls.fastReverse();
    }
}
```


```VB

Public Sub fastReverseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastReverseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastReverse&quot;)) Then

        controls.fastReverse()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="390f7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="390f7-125">Requirements</span></span>



| <span data-ttu-id="390f7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="390f7-126">Requirement</span></span> | <span data-ttu-id="390f7-127">Value</span><span class="sxs-lookup"><span data-stu-id="390f7-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="390f7-128">Versión</span><span class="sxs-lookup"><span data-stu-id="390f7-128">Version</span></span><br/>   | <span data-ttu-id="390f7-129">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="390f7-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="390f7-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="390f7-130">Namespace</span></span><br/> | <span data-ttu-id="390f7-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="390f7-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="390f7-132">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="390f7-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="390f7-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="390f7-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="390f7-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="390f7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="390f7-135">**Interfaz IWMPControls (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="390f7-135">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="390f7-136">**IWMPControls. fastForward (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="390f7-136">**IWMPControls.fastForward (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="390f7-137">**IWMPControls. isAvailable (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="390f7-137">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="390f7-138">**IWMPControls. Play (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="390f7-138">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="390f7-139">**IWMPControls. STOP (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="390f7-139">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="390f7-140">**IWMPSettings. Rate (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="390f7-140">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





