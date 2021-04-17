---
title: Método anterior IWMPControls
description: El método anterior establece el elemento anterior de la lista de reproducción como el elemento actual.
ms.assetid: 380524f5-e8b6-45c4-9f6c-3dbb49b1ac9f
keywords:
- método anterior de Windows Media Player
- método anterior de Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, método Previous
topic_type:
- apiref
api_name:
- IWMPControls.previous
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823038205a026afb7141491f562698eb60515a5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690873"
---
# <a name="iwmpcontrolsprevious-method"></a><span data-ttu-id="191b9-106">IWMPControls::p método rior</span><span class="sxs-lookup"><span data-stu-id="191b9-106">IWMPControls::previous method</span></span>

<span data-ttu-id="191b9-107">El método **anterior** establece el elemento anterior de la lista de reproducción como el elemento actual.</span><span class="sxs-lookup"><span data-stu-id="191b9-107">The **previous** method sets the previous item in the playlist as the current item.</span></span>

## <a name="syntax"></a><span data-ttu-id="191b9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="191b9-108">Syntax</span></span>


```CSharp
public void previous();
```


```VB

Public Sub previous()
Implements IWMPControls.previous
```





## <a name="parameters"></a><span data-ttu-id="191b9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="191b9-109">Parameters</span></span>

<span data-ttu-id="191b9-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="191b9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="191b9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="191b9-111">Return value</span></span>

<span data-ttu-id="191b9-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="191b9-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="191b9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="191b9-113">Remarks</span></span>

<span data-ttu-id="191b9-114">Si la lista de reproducción está en la primera entrada cuando se invoca el **anterior** , la última entrada de la lista de reproducción se convertirá en la actual.</span><span class="sxs-lookup"><span data-stu-id="191b9-114">If the playlist is on the first entry when **previous** is invoked, the last entry in the playlist will become the current one.</span></span>

## <a name="examples"></a><span data-ttu-id="191b9-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="191b9-115">Examples</span></span>

<span data-ttu-id="191b9-116">En el ejemplo siguiente se usa **Previous** para moverse al elemento anterior de la lista de reproducción actual en respuesta al evento click de un botón.</span><span class="sxs-lookup"><span data-stu-id="191b9-116">The following example uses **previous** to move to the previous item in the current playlist in response to the Click event of a button.</span></span> <span data-ttu-id="191b9-117">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="191b9-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void previousButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("previous"))
    {
        controls.previous();
    }
}
```


```VB

Public Sub previousButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles previousButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;previous&quot;)) Then

        controls.previous()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="191b9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="191b9-118">Requirements</span></span>



| <span data-ttu-id="191b9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="191b9-119">Requirement</span></span> | <span data-ttu-id="191b9-120">Value</span><span class="sxs-lookup"><span data-stu-id="191b9-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="191b9-121">Versión</span><span class="sxs-lookup"><span data-stu-id="191b9-121">Version</span></span><br/>   | <span data-ttu-id="191b9-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="191b9-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="191b9-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="191b9-123">Namespace</span></span><br/> | <span data-ttu-id="191b9-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="191b9-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="191b9-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="191b9-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="191b9-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="191b9-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="191b9-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="191b9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="191b9-128">**Interfaz IWMPControls (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="191b9-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="191b9-129">**IWMPControls. Next (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="191b9-129">**IWMPControls.next (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="191b9-130">**IWMPControls. STOP (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="191b9-130">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





