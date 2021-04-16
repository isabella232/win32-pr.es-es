---
title: Propiedad errorDescription de IWMPErrorItem
description: La propiedad errorDescription obtiene una descripción del error.
ms.assetid: a9914c24-1d10-422a-bcba-80be9fb85108
keywords:
- propiedades de errorDescription Media Player de Windows
- propiedad errorDescription de Windows Media Player, interfaz IWMPErrorItem
- Interfaz IWMPErrorItem Windows Media Player, propiedad errorDescription
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8725099d1ce49eae8f378b2571dc4030f60611e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709178"
---
# <a name="iwmperroritemerrordescription-property"></a><span data-ttu-id="df8cf-106">IWMPErrorItem:: errorDescription (propiedad)</span><span class="sxs-lookup"><span data-stu-id="df8cf-106">IWMPErrorItem::errorDescription property</span></span>

<span data-ttu-id="df8cf-107">La propiedad **errorDescription** obtiene una descripción del error.</span><span class="sxs-lookup"><span data-stu-id="df8cf-107">The **errorDescription** property gets a description of the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="df8cf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df8cf-108">Syntax</span></span>


```CSharp
public System.String errorDescription {get; set;}
```


```VB

Public ReadOnly Property errorDescription As System.String
```





## <a name="property-value"></a><span data-ttu-id="df8cf-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="df8cf-109">Property value</span></span>

<span data-ttu-id="df8cf-110">**System. String** que es la descripción del error.</span><span class="sxs-lookup"><span data-stu-id="df8cf-110">A **System.String** that is the error description.</span></span>

## <a name="remarks"></a><span data-ttu-id="df8cf-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="df8cf-111">Remarks</span></span>

<span data-ttu-id="df8cf-112">Debe establecer **IWMPSettings. enableErrorDialogs** en **false** si elige mostrar mensajes de error personalizados.</span><span class="sxs-lookup"><span data-stu-id="df8cf-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="df8cf-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="df8cf-113">Examples</span></span>

<span data-ttu-id="df8cf-114">En el ejemplo siguiente se usa **errorDescription** en un controlador de eventos de error para mostrar la descripción del error al usuario.</span><span class="sxs-lookup"><span data-stu-id="df8cf-114">The following example uses **errorDescription** in an Error event handler to display the error description to the user.</span></span> <span data-ttu-id="df8cf-115">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="df8cf-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorDescription(object sender, System.EventArgs e)
{
    // Get the error description for the first error item.
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show("Error: " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorDescription(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error description for the first error item.
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(&quot;Error: &quot; + errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="df8cf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df8cf-116">Requirements</span></span>



| <span data-ttu-id="df8cf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="df8cf-117">Requirement</span></span> | <span data-ttu-id="df8cf-118">Value</span><span class="sxs-lookup"><span data-stu-id="df8cf-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df8cf-119">Versión</span><span class="sxs-lookup"><span data-stu-id="df8cf-119">Version</span></span><br/>   | <span data-ttu-id="df8cf-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="df8cf-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="df8cf-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="df8cf-121">Namespace</span></span><br/> | <span data-ttu-id="df8cf-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="df8cf-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="df8cf-123">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="df8cf-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="df8cf-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="df8cf-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df8cf-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="df8cf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df8cf-126">**Interfaz IWMPErrorItem (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="df8cf-126">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="df8cf-127">**IWMPSettings. enableErrorDialogs (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="df8cf-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





