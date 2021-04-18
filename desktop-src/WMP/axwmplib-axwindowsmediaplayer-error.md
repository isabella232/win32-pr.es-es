---
title: Evento de error del objeto AxWindowsMediaPlayer
description: El evento de error se produce cuando el control de Media Player de Windows tiene una condición de error.
ms.assetid: d28c18a9-c650-4169-989b-8727b7a5a831
keywords:
- Evento de error del objeto AxWindowsMediaPlayer de Windows Media Player
topic_type:
- apiref
api_name:
- Error Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cfd3571538aa2cdd263a9f5d57e479e73818806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698546"
---
# <a name="error-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="7fbf8-104">Evento de error del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="7fbf8-104">Error Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="7fbf8-105">El evento de error se produce cuando el control de Media Player de Windows tiene una condición de error.</span><span class="sxs-lookup"><span data-stu-id="7fbf8-105">The Error event occurs when the Windows Media Player control has an error condition.</span></span>

``` syntax
[C#]
private void player_ErrorEvent(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_ErrorEvent(  
  sender As Object,  
  e As System.EventArgs
) Handles player.ErrorEvent
```

## <a name="event-data"></a><span data-ttu-id="7fbf8-106">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="7fbf8-106">Event Data</span></span>

<span data-ttu-id="7fbf8-107">Este evento no contiene datos.</span><span class="sxs-lookup"><span data-stu-id="7fbf8-107">This event does not contain data.</span></span>

## <a name="examples"></a><span data-ttu-id="7fbf8-108">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7fbf8-108">Examples</span></span>

<span data-ttu-id="7fbf8-109">En el ejemplo siguiente se crea un controlador de eventos para el evento de error con el fin de mostrar el texto de la descripción del primer error en la cola de errores.</span><span class="sxs-lookup"><span data-stu-id="7fbf8-109">The following example creates an event handler for the Error event to display the description text for the first error in the error queue.</span></span> <span data-ttu-id="7fbf8-110">El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="7fbf8-110">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Error event.
player.ErrorEvent += new EventHandler(player_ErrorEvent);

private void player_ErrorEvent(object sender, System.EventArgs e)
{
    // Get the description of the first error. 
    string errDesc = player.Error.get_Item(0).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the description of the first error. 
    Dim errDesc As String = player.Error.Item(0).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="7fbf8-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fbf8-111">Requirements</span></span>



| <span data-ttu-id="7fbf8-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fbf8-112">Requirement</span></span> | <span data-ttu-id="7fbf8-113">Value</span><span class="sxs-lookup"><span data-stu-id="7fbf8-113">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fbf8-114">Versión</span><span class="sxs-lookup"><span data-stu-id="7fbf8-114">Version</span></span><br/>   | <span data-ttu-id="7fbf8-115">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="7fbf8-115">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="7fbf8-116">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7fbf8-116">Namespace</span></span><br/> | <span data-ttu-id="7fbf8-117">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="7fbf8-117">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="7fbf8-118">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="7fbf8-118">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7fbf8-119"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7fbf8-119"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fbf8-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fbf8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fbf8-121">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="7fbf8-121">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7fbf8-122">**IWMPError. Item (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="7fbf8-122">**IWMPError.Item (VB and C#)**</span></span>](iwmperror-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7fbf8-123">**IWMPErrorItem. errorDescription (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="7fbf8-123">**IWMPErrorItem.errorDescription (VB and C#)**</span></span>](wmplibiwmperroritem-iwmperroritem-errordescription--vb-and-c.md)
</dt> </dl>

 

 





