---
title: IWMPControls Play (método)
description: El método play comienza la reproducción del elemento multimedia actual o reanuda la reproducción de un elemento en pausa.
ms.assetid: 02e00df6-4dc1-44bb-9826-e69e8298ccaa
keywords:
- método play Windows Media Player
- método play Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, método play
topic_type:
- apiref
api_name:
- IWMPControls.play
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fd87a2e2ba3d53b119df328fa68668c91c78d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690875"
---
# <a name="iwmpcontrolsplay-method"></a><span data-ttu-id="4dee6-106">IWMPControls::p establecer método</span><span class="sxs-lookup"><span data-stu-id="4dee6-106">IWMPControls::play method</span></span>

<span data-ttu-id="4dee6-107">El método **Play** comienza la reproducción del elemento multimedia actual o reanuda la reproducción de un elemento en pausa.</span><span class="sxs-lookup"><span data-stu-id="4dee6-107">The **play** method begins playback of the current media item, or resumes playback of a paused item.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dee6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4dee6-108">Syntax</span></span>


```CSharp
public void play();
```


```VB

Public Sub play()
Implements IWMPControls.play
```





## <a name="parameters"></a><span data-ttu-id="4dee6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4dee6-109">Parameters</span></span>

<span data-ttu-id="4dee6-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4dee6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4dee6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4dee6-111">Return value</span></span>

<span data-ttu-id="4dee6-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4dee6-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dee6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4dee6-113">Remarks</span></span>

<span data-ttu-id="4dee6-114">Si se llama a este método durante el reenvío rápido o el rebobinado, la velocidad de reproducción (el valor de **IWMPSettings. rate**) se establece en 1,0.</span><span class="sxs-lookup"><span data-stu-id="4dee6-114">If this method is called while fast-forwarding or rewinding, the rate of playback (the value of **IWMPSettings.rate**) is set to 1.0.</span></span>

## <a name="examples"></a><span data-ttu-id="4dee6-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4dee6-115">Examples</span></span>

<span data-ttu-id="4dee6-116">En el ejemplo siguiente se usa **Play** para reproducir el elemento multimedia actual en respuesta al evento click de un botón.</span><span class="sxs-lookup"><span data-stu-id="4dee6-116">The following example uses **play** to play the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="4dee6-117">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="4dee6-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("play"))
    {
        controls.play();
    }
}
```


```VB

Public Sub playButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;play&quot;)) Then

        controls.play()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="4dee6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4dee6-118">Requirements</span></span>



| <span data-ttu-id="4dee6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dee6-119">Requirement</span></span> | <span data-ttu-id="4dee6-120">Value</span><span class="sxs-lookup"><span data-stu-id="4dee6-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dee6-121">Versión</span><span class="sxs-lookup"><span data-stu-id="4dee6-121">Version</span></span><br/>   | <span data-ttu-id="4dee6-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="4dee6-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4dee6-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4dee6-123">Namespace</span></span><br/> | <span data-ttu-id="4dee6-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4dee6-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4dee6-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="4dee6-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4dee6-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4dee6-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dee6-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4dee6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dee6-128">**Interfaz IWMPControls (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="4dee6-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4dee6-129">**IWMPControls. playItem (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="4dee6-129">**IWMPControls.playItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4dee6-130">**IWMPSettings. Rate (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="4dee6-130">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





