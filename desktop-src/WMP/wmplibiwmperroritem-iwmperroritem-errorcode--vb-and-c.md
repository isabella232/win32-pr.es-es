---
title: Propiedad errorCode de IWMPErrorItem
description: La propiedad errorCode obtiene el código de error actual.
ms.assetid: 00719067-685d-4ef2-9eec-72c7892fcdb9
keywords:
- propiedad errorCode Windows Media Player
- propiedad errorCode Windows Media Player, interfaz IWMPErrorItem
- Interfaz IWMPErrorItem Windows Media Player, propiedad errorCode
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorCode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f284d5655fc1f4007695a1f681c744a9c5c6fc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709179"
---
# <a name="iwmperroritemerrorcode-property"></a><span data-ttu-id="29cf0-106">IWMPErrorItem:: errorCode (propiedad)</span><span class="sxs-lookup"><span data-stu-id="29cf0-106">IWMPErrorItem::errorCode property</span></span>

<span data-ttu-id="29cf0-107">La propiedad **ErrorCode** obtiene el código de error actual.</span><span class="sxs-lookup"><span data-stu-id="29cf0-107">The **errorCode** property gets the current error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="29cf0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29cf0-108">Syntax</span></span>


```CSharp
public System.Int32 errorCode {get; set;}
```


```VB

Public ReadOnly Property errorCode As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="29cf0-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="29cf0-109">Property value</span></span>

<span data-ttu-id="29cf0-110">**System. Int32** que es el código de error.</span><span class="sxs-lookup"><span data-stu-id="29cf0-110">A **System.Int32** that is the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="29cf0-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29cf0-111">Remarks</span></span>

<span data-ttu-id="29cf0-112">Debe establecer **IWMPSettings. enableErrorDialogs** en **false** si elige mostrar mensajes de error personalizados.</span><span class="sxs-lookup"><span data-stu-id="29cf0-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="29cf0-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="29cf0-113">Examples</span></span>

<span data-ttu-id="29cf0-114">En el ejemplo siguiente se usa **ErrorCode** en un controlador de eventos de error para mostrar el código de error al usuario.</span><span class="sxs-lookup"><span data-stu-id="29cf0-114">The following example uses **errorCode** in an Error event handler to display the error code to the user.</span></span> <span data-ttu-id="29cf0-115">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="29cf0-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorCode(object sender, System.EventArgs e)
{
    // Get the error code for the first error item.
    int errCode = player.Error.get_Item(0).errorCode;

    // Display the error code.
    System.Windows.Forms.MessageBox.Show("Error number: " + errCode.ToString());
}
```


```VB

Public Sub player_ErrorEvent_errorCode(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error code for the first error item.
    Dim errCode As Integer = player.Error.Item(0).errorCode

    &#39; Display the error code.
    System.Windows.Forms.MessageBox.Show(&quot;Error number: &quot; + errCode.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="29cf0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29cf0-116">Requirements</span></span>



| <span data-ttu-id="29cf0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="29cf0-117">Requirement</span></span> | <span data-ttu-id="29cf0-118">Value</span><span class="sxs-lookup"><span data-stu-id="29cf0-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29cf0-119">Versión</span><span class="sxs-lookup"><span data-stu-id="29cf0-119">Version</span></span><br/>   | <span data-ttu-id="29cf0-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="29cf0-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="29cf0-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="29cf0-121">Namespace</span></span><br/> | <span data-ttu-id="29cf0-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="29cf0-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="29cf0-123">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="29cf0-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="29cf0-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="29cf0-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29cf0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="29cf0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29cf0-126">**Interfaz IWMPErrorItem (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="29cf0-126">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="29cf0-127">**IWMPSettings. enableErrorDialogs (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="29cf0-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





