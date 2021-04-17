---
title: IWMPControls STOP (método)
description: El método Stop detiene la reproducción del elemento multimedia. | IWMPControls STOP (método)
ms.assetid: 4be601af-6321-4115-a94d-cfc9228991cb
keywords:
- detener el método Windows Media Player
- método STOP Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, método STOP
topic_type:
- apiref
api_name:
- IWMPControls.stop
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73271098340ea0cf0a645472b5ef6333ae0f4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690872"
---
# <a name="iwmpcontrolsstop-method"></a><span data-ttu-id="2e926-107">IWMPControls:: STOP (método)</span><span class="sxs-lookup"><span data-stu-id="2e926-107">IWMPControls::stop method</span></span>

<span data-ttu-id="2e926-108">El método **Stop** detiene la reproducción del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="2e926-108">The **stop** method stops playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e926-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e926-109">Syntax</span></span>


```CSharp
public void stop();
```


```VB

Public Sub stop()
Implements IWMPControls.stop
```





## <a name="parameters"></a><span data-ttu-id="2e926-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e926-110">Parameters</span></span>

<span data-ttu-id="2e926-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2e926-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e926-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e926-112">Return value</span></span>

<span data-ttu-id="2e926-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2e926-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e926-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e926-114">Remarks</span></span>

<span data-ttu-id="2e926-115">Este método hace que Windows Media Player libere cualquier recurso del sistema que esté usando, como el dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="2e926-115">This method causes Windows Media Player to release any system resources it is using, such as the audio device.</span></span> <span data-ttu-id="2e926-116">Sin embargo, el elemento multimedia actual no se libera.</span><span class="sxs-lookup"><span data-stu-id="2e926-116">The current media item, however, is not released.</span></span>

<span data-ttu-id="2e926-117">Cuando se detiene Windows Media Player, la posición de reproducción actual en el elemento multimedia se restablece al principio del elemento.</span><span class="sxs-lookup"><span data-stu-id="2e926-117">When Windows Media Player is stopped, the current playback position in the media item is reset to the beginning of the item.</span></span> <span data-ttu-id="2e926-118">Después de llamar a **IWMPControls. Play** se iniciará la reproducción desde el principio del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="2e926-118">Subsequently calling **IWMPControls.play** will start playback from the beginning of the media item.</span></span> <span data-ttu-id="2e926-119">Para detener una operación de reproducción sin cambiar la posición actual, use el método **IWMPControls. PAUSE** .</span><span class="sxs-lookup"><span data-stu-id="2e926-119">To halt a play operation without changing the current position, use the **IWMPControls.pause** method.</span></span>

## <a name="examples"></a><span data-ttu-id="2e926-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2e926-120">Examples</span></span>

<span data-ttu-id="2e926-121">En el ejemplo siguiente se usa **Stop** para detener el elemento multimedia actual en respuesta al evento click de un botón.</span><span class="sxs-lookup"><span data-stu-id="2e926-121">The following example uses **stop** to stop the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="2e926-122">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="2e926-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void stopButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("stop"))
    {
        controls.stop();
    }
}
```


```VB

Public Sub stopButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles stopButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;stop&quot;)) Then

        controls.stop()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="2e926-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e926-123">Requirements</span></span>



| <span data-ttu-id="2e926-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e926-124">Requirement</span></span> | <span data-ttu-id="2e926-125">Value</span><span class="sxs-lookup"><span data-stu-id="2e926-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e926-126">Versión</span><span class="sxs-lookup"><span data-stu-id="2e926-126">Version</span></span><br/>   | <span data-ttu-id="2e926-127">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="2e926-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2e926-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2e926-128">Namespace</span></span><br/> | <span data-ttu-id="2e926-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2e926-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2e926-130">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="2e926-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2e926-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2e926-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e926-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e926-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e926-133">**Interfaz IWMPControls (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="2e926-133">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2e926-134">**IWMPControls. Next (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="2e926-134">**IWMPControls.next (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2e926-135">**IWMPControls. PAUSE (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="2e926-135">**IWMPControls.pause (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2e926-136">**IWMPControls. Play (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="2e926-136">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2e926-137">**IWMPControls. Previous (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="2e926-137">**IWMPControls.previous (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> </dl>

 

 





