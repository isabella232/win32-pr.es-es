---
title: Método Next IWMPControls
description: El siguiente método establece el elemento siguiente de la lista de reproducción como el elemento actual.
ms.assetid: 3f82ef25-a1e0-4845-b0ed-dd6463719577
keywords:
- siguiente método de Windows Media Player
- siguiente método de Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, método Next
topic_type:
- apiref
api_name:
- IWMPControls.next
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8444ba7d9209759cb64c4b582e1af9d074332ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690877"
---
# <a name="iwmpcontrolsnext-method"></a><span data-ttu-id="c6c2a-106">IWMPControls:: Next (método)</span><span class="sxs-lookup"><span data-stu-id="c6c2a-106">IWMPControls::next method</span></span>

<span data-ttu-id="c6c2a-107">El **siguiente** método establece el elemento siguiente de la lista de reproducción como el elemento actual.</span><span class="sxs-lookup"><span data-stu-id="c6c2a-107">The **next** method sets the next item in the playlist as the current item.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6c2a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6c2a-108">Syntax</span></span>


```CSharp
public void next();
```


```VB

Public Sub next()
Implements IWMPControls.next
```





## <a name="parameters"></a><span data-ttu-id="c6c2a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6c2a-109">Parameters</span></span>

<span data-ttu-id="c6c2a-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c6c2a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c6c2a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6c2a-111">Return value</span></span>

<span data-ttu-id="c6c2a-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c6c2a-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6c2a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6c2a-113">Remarks</span></span>

<span data-ttu-id="c6c2a-114">Si la lista de reproducción está en la última entrada cuando se invoca **siguiente** , la primera entrada de la lista de reproducción se convertirá en la actual.</span><span class="sxs-lookup"><span data-stu-id="c6c2a-114">If the playlist is on the last entry when **next** is invoked, the first entry in the playlist will become the current one.</span></span>

<span data-ttu-id="c6c2a-115">En las listas de reproducción del lado servidor, este método omite el siguiente elemento de la lista de reproducción del servidor, no la lista de reproducción del cliente.</span><span class="sxs-lookup"><span data-stu-id="c6c2a-115">For server-side playlists, this method skips to the next item in the server-side playlist, not the client playlist.</span></span>

<span data-ttu-id="c6c2a-116">Al reproducir un DVD, este método omite el siguiente capítulo lógico de la secuencia de reproducción, que puede no ser el siguiente capítulo de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="c6c2a-116">When playing a DVD, this method skips to the next logical chapter in the playback sequence, which may not be the next chapter in the playlist.</span></span> <span data-ttu-id="c6c2a-117">Al reproducir imágenes de DVD seguidas, este método pasa a la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="c6c2a-117">When playing DVD still images, this method skips to the next image.</span></span>

## <a name="examples"></a><span data-ttu-id="c6c2a-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c6c2a-118">Examples</span></span>

<span data-ttu-id="c6c2a-119">En el ejemplo siguiente se usa **Next** para moverse al siguiente elemento de la lista de reproducción actual en respuesta al evento click de un botón.</span><span class="sxs-lookup"><span data-stu-id="c6c2a-119">The following example uses **next** to move to the next item in the current playlist in response to the Click event of a button.</span></span> <span data-ttu-id="c6c2a-120">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="c6c2a-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void nextButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("next"))
    {
        controls.next();
    }
}
```


```VB

Public Sub nextButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles nextButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;next&quot;)) Then

        controls.next()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="c6c2a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6c2a-121">Requirements</span></span>



| <span data-ttu-id="c6c2a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6c2a-122">Requirement</span></span> | <span data-ttu-id="c6c2a-123">Value</span><span class="sxs-lookup"><span data-stu-id="c6c2a-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c2a-124">Versión</span><span class="sxs-lookup"><span data-stu-id="c6c2a-124">Version</span></span><br/>   | <span data-ttu-id="c6c2a-125">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="c6c2a-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c6c2a-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c6c2a-126">Namespace</span></span><br/> | <span data-ttu-id="c6c2a-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c6c2a-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c6c2a-128">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="c6c2a-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c6c2a-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c6c2a-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6c2a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6c2a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c2a-131">**Interfaz IWMPControls (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c6c2a-131">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c6c2a-132">**IWMPControls. Previous (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c6c2a-132">**IWMPControls.previous (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c6c2a-133">**IWMPControls. STOP (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c6c2a-133">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





