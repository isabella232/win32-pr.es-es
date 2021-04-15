---
title: Propiedad errorCount de IWMPError
description: La propiedad errorCount obtiene el número de errores en la cola de errores.
ms.assetid: a30750c8-2025-4087-bd2b-f313ccbde38c
keywords:
- propiedades de errorCount Media Player de Windows
- propiedad errorCount de Windows Media Player, interfaz IWMPError
- Interfaz IWMPError Windows Media Player, propiedad errorCount
topic_type:
- apiref
api_name:
- IWMPError.errorCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b62c16f07260847c91f1c9f18885587444a4ceb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709184"
---
# <a name="iwmperrorerrorcount-property"></a><span data-ttu-id="991d5-106">IWMPError:: errorCount (propiedad)</span><span class="sxs-lookup"><span data-stu-id="991d5-106">IWMPError::errorCount property</span></span>

<span data-ttu-id="991d5-107">La propiedad **errorCount** obtiene el número de errores en la cola de errores.</span><span class="sxs-lookup"><span data-stu-id="991d5-107">The **errorCount** property gets the number of errors in the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="991d5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="991d5-108">Syntax</span></span>


```CSharp
public System.Int32 errorCount {get; set;}
```


```VB

Public ReadOnly Property errorCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="991d5-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="991d5-109">Property value</span></span>

<span data-ttu-id="991d5-110">**System. Int32** que es el número de errores.</span><span class="sxs-lookup"><span data-stu-id="991d5-110">A **System.Int32** that is the number of errors.</span></span>

## <a name="remarks"></a><span data-ttu-id="991d5-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="991d5-111">Remarks</span></span>

<span data-ttu-id="991d5-112">Debe establecer **IWMPSettings. enableErrorDialogs** en **false** si elige mostrar mensajes de error personalizados.</span><span class="sxs-lookup"><span data-stu-id="991d5-112">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="991d5-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="991d5-113">Examples</span></span>

<span data-ttu-id="991d5-114">En el ejemplo siguiente se usa **errorCount** en un controlador de eventos de error para avisar al usuario sobre el error más reciente en la cola de errores.</span><span class="sxs-lookup"><span data-stu-id="991d5-114">The following example uses **errorCount** in an Error event handler to alert the user about the most recent error in the error queue.</span></span> <span data-ttu-id="991d5-115">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="991d5-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_errorCount(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Get the description of the last error. Error items start at zero,
    // so the item index will always be one less than the error count.
    string errDesc = player.Error.get_Item(max-1).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorCount(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Get the description of the last error. Error items start at zero,
    &#39; so the item index will always be one less than the error count.
    Dim errDesc As String = player.Error.Item(max - 1).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="991d5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="991d5-116">Requirements</span></span>



| <span data-ttu-id="991d5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="991d5-117">Requirement</span></span> | <span data-ttu-id="991d5-118">Value</span><span class="sxs-lookup"><span data-stu-id="991d5-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="991d5-119">Versión</span><span class="sxs-lookup"><span data-stu-id="991d5-119">Version</span></span><br/>   | <span data-ttu-id="991d5-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="991d5-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="991d5-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="991d5-121">Namespace</span></span><br/> | <span data-ttu-id="991d5-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="991d5-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="991d5-123">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="991d5-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="991d5-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="991d5-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="991d5-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="991d5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="991d5-126">**Interfaz IWMPError (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="991d5-126">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="991d5-127">**IWMPSettings. enableErrorDialogs (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="991d5-127">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





