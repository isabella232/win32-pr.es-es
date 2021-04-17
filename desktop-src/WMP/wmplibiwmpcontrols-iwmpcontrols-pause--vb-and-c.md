---
title: IWMPControls PAUSE (método)
description: El método PAUSE pausa la reproducción del elemento multimedia. | IWMPControls PAUSE (método)
ms.assetid: 1d9ebaf3-84b4-458d-a393-2b685cd0dbfb
keywords:
- pausar el método Windows Media Player
- pausar el método Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, pausar método
topic_type:
- apiref
api_name:
- IWMPControls.pause
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf89cfef66c84be76a529d9c0cef6ec3ae6ac40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690876"
---
# <a name="iwmpcontrolspause-method"></a><span data-ttu-id="bc577-107">IWMPControls::p método ause</span><span class="sxs-lookup"><span data-stu-id="bc577-107">IWMPControls::pause method</span></span>

<span data-ttu-id="bc577-108">El método **PAUSE pausa** la reproducción del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="bc577-108">The **pause** method pauses playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc577-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc577-109">Syntax</span></span>


```CSharp
public void pause();
```


```VB

Public Sub pause()
Implements IWMPControls.pause
```





## <a name="parameters"></a><span data-ttu-id="bc577-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc577-110">Parameters</span></span>

<span data-ttu-id="bc577-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bc577-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bc577-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc577-112">Return value</span></span>

<span data-ttu-id="bc577-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="bc577-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc577-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc577-114">Remarks</span></span>

<span data-ttu-id="bc577-115">Cuando un archivo está en pausa, Windows Media Player no proporciona ningún recurso del sistema, como el dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="bc577-115">When a file is paused, Windows Media Player does not give up any system resources, such as the audio device.</span></span>

<span data-ttu-id="bc577-116">Para determinar si un tipo de medio determinado se puede pausar, pase el valor **System. String** "PAUSE" a la propiedad **IWMPControls. isavailable** (el método **IWMPControls. Get \_ isavailable** en C#).</span><span class="sxs-lookup"><span data-stu-id="bc577-116">To determine whether a particular media type can be paused, pass the **System.String** value "pause" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="bc577-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bc577-117">Examples</span></span>

<span data-ttu-id="bc577-118">En el ejemplo siguiente se usa **PAUSE** para pausar la reproducción del elemento multimedia actual en respuesta al evento click de un botón.</span><span class="sxs-lookup"><span data-stu-id="bc577-118">The following example uses **pause** to pause playback of the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="bc577-119">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="bc577-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void pauseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("pause"))
    {
        controls.pause();
    }
}
```


```VB

Public Sub pauseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles pauseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;pause&quot;)) Then

        controls.pause()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="bc577-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc577-120">Requirements</span></span>



| <span data-ttu-id="bc577-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc577-121">Requirement</span></span> | <span data-ttu-id="bc577-122">Value</span><span class="sxs-lookup"><span data-stu-id="bc577-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc577-123">Versión</span><span class="sxs-lookup"><span data-stu-id="bc577-123">Version</span></span><br/>   | <span data-ttu-id="bc577-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="bc577-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="bc577-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bc577-125">Namespace</span></span><br/> | <span data-ttu-id="bc577-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="bc577-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="bc577-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="bc577-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bc577-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="bc577-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc577-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc577-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc577-130">**Interfaz IWMPControls (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="bc577-130">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bc577-131">**IWMPControls. isAvailable (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="bc577-131">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> </dl>

 

 





