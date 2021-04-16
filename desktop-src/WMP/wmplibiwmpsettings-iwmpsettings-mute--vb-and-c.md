---
title: Propiedad IWMPSettings MUTE
description: La propiedad MUTE obtiene o establece un valor que indica si el audio está silenciado.
ms.assetid: d99e47db-70cc-41e0-aca9-b765b075e7b4
keywords:
- silenciar las ventanas de propiedades Media Player
- propiedad silenciar Media Player de Windows, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, propiedad MUTE
topic_type:
- apiref
api_name:
- IWMPSettings.mute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67518bb9a6eccee13e4cc262f37341d30689439e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105719025"
---
# <a name="iwmpsettingsmute-property"></a><span data-ttu-id="3c94b-106">IWMPSettings:: MUTE (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3c94b-106">IWMPSettings::mute property</span></span>

<span data-ttu-id="3c94b-107">La propiedad **MUTE** obtiene o establece un valor que indica si el audio está silenciado.</span><span class="sxs-lookup"><span data-stu-id="3c94b-107">The **mute** property gets or sets a value indicating whether audio is muted.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c94b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c94b-108">Syntax</span></span>


```CSharp
public System.Boolean mute {get; set;}
```


```VB

Public Property mute As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="3c94b-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3c94b-109">Property value</span></span>

<span data-ttu-id="3c94b-110">Un valor **System. Boolean** que indica si el audio está silenciado.</span><span class="sxs-lookup"><span data-stu-id="3c94b-110">A **System.Boolean** value indicating whether audio is muted.</span></span> <span data-ttu-id="3c94b-111">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="3c94b-111">The default is **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="3c94b-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3c94b-112">Examples</span></span>

<span data-ttu-id="3c94b-113">En el ejemplo siguiente se crea una casilla y se alterna la propiedad **MUTE** para silenciar el audio y dejar de silenciarlo cuando se cambia el estado de activación del cuadro.</span><span class="sxs-lookup"><span data-stu-id="3c94b-113">The following example creates a check box, and toggles the **mute** property to mute and un-mute audio when the checked state of the box is changed.</span></span> <span data-ttu-id="3c94b-114">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="3c94b-114">**AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void Mute_CheckStateChanged(object sender, System.EventArgs e)
{
    System.Windows.Forms.CheckBox Mute = (System.Windows.Forms.CheckBox)sender;

    // Change the check box text depending on the checked state.
    Mute.Text = Mute.Checked ? "Un-mute Audio" : Mute.Text = "Mute Audio";

    // Use the checked state to set the mute property. 
    player.settings.mute = Mute.Checked;
}
```


```VB

Public Sub Mute_CheckStateChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles Mute.CheckStateChanged

    Dim cb As System.Windows.Forms.CheckBox = sender

    &#39;  Change the check box text depending on the checked state.
    If (cb.Checked) Then

        cb.Text = &quot;Un-mute Audio&quot;

    Else

        cb.Text = &quot;Mute Audio&quot;

    End If

    &#39;  Use the checked state to set the mute property. 
    player.settings.mute = cb.Checked

End Sub
```





## <a name="requirements"></a><span data-ttu-id="3c94b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c94b-115">Requirements</span></span>



| <span data-ttu-id="3c94b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c94b-116">Requirement</span></span> | <span data-ttu-id="3c94b-117">Value</span><span class="sxs-lookup"><span data-stu-id="3c94b-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c94b-118">Versión</span><span class="sxs-lookup"><span data-stu-id="3c94b-118">Version</span></span><br/>   | <span data-ttu-id="3c94b-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="3c94b-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3c94b-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3c94b-120">Namespace</span></span><br/> | <span data-ttu-id="3c94b-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3c94b-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3c94b-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="3c94b-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3c94b-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3c94b-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c94b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c94b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c94b-125">**Interfaz IWMPSettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3c94b-125">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3c94b-126">**IWMPSettings. Rate (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3c94b-126">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





