---
title: Evento CurrentPlaylistChange del objeto AxWindowsMediaPlayer
description: El evento CurrentPlaylistChange se produce cuando hay algún cambio en la lista de reproducción actual. | Evento CurrentPlaylistChange del objeto AxWindowsMediaPlayer
ms.assetid: 1f9c99a4-7d10-48bf-b5ff-b1c1d6753b20
keywords:
- Evento CurrentPlaylistChange del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- CurrentPlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f99f34f0e02d03352a61bbfca6767295d63d59a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698504"
---
# <a name="currentplaylistchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="576ef-105">Evento CurrentPlaylistChange del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="576ef-105">CurrentPlaylistChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="576ef-106">El evento CurrentPlaylistChange se produce cuando hay algún cambio en la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="576ef-106">The CurrentPlaylistChange event occurs when something changes within the current playlist.</span></span>

``` syntax
[C#]
private void player_CurrentPlaylistChange(
  object sender,
  _WMPOCXEvents_CurrentPlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_CurrentPlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_CurrentPlaylistChangeEvent
) Handles player.CurrentPlaylistChange
```

## <a name="event-data"></a><span data-ttu-id="576ef-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="576ef-107">Event Data</span></span>

<span data-ttu-id="576ef-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="576ef-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistChangeEventHandler**.</span></span> <span data-ttu-id="576ef-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistChangeEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="576ef-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="576ef-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="576ef-110">Property</span></span> | <span data-ttu-id="576ef-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="576ef-111">Description</span></span>                                                                                                                   |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="576ef-112">cambiar</span><span class="sxs-lookup"><span data-stu-id="576ef-112">change</span></span>   | <span data-ttu-id="576ef-113">Valor de enumeración WMPLib. WMPPlaylistChangeEventTypeAn que indica el tipo de cambio que se produjo en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="576ef-113">WMPLib.WMPPlaylistChangeEventTypeAn enumeration value indicating the type of change that occurred to the playlist.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="576ef-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="576ef-114">Remarks</span></span>

<span data-ttu-id="576ef-115">Este evento no se produce cuando una lista de reproducción distinta se convierte en la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="576ef-115">This event does not occur when a different playlist becomes the current playlist.</span></span> <span data-ttu-id="576ef-116">Solo se produce cuando se produce un cambio en la lista de reproducción actual, como un elemento multimedia que se anexa a la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="576ef-116">It occurs only when a change happens within the current playlist, such as a media item being appended to the playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="576ef-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="576ef-117">Examples</span></span>

<span data-ttu-id="576ef-118">En el ejemplo siguiente se muestran los nombres de todos los elementos multimedia de la lista de reproducción actual en respuesta al evento CurrentPlaylistChange.</span><span class="sxs-lookup"><span data-stu-id="576ef-118">The following example displays the names of all the media items in the current playlist in response to the CurrentPlaylistChange Event.</span></span> <span data-ttu-id="576ef-119">El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="576ef-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the CurrentPlaylistChange event.
player.CurrentPlaylistChange += new AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEventHandler(player_CurrentPlaylistChange);  


private void player_CurrentPlaylistChange(object sender, AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEvent e)
{
    switch(e.change)
    {
        // Only update the list for the move, delete, insert, and append event types.
        case WMPLib.WMPPlaylistChangeEventType.wmplcMove:    // Value = 3
        case WMPLib.WMPPlaylistChangeEventType.wmplcDelete:  // Value = 4
        case WMPLib.WMPPlaylistChangeEventType.wmplcInsert:  // Value = 5
        case WMPLib.WMPPlaylistChangeEventType.wmplcAppend:  // Value = 6

        // Create a string array large enough to hold all of the media item names.
        int count = player.currentPlaylist.count;
        string[] mediaItems = new string[count];

        // Clear any previous contents of the text box.
        playlistItems.Clear();

        // Loop through the playlist and store each media item name.
        for (int i = 0; i < count; i++)
        {
            mediaItems[i] = player.currentPlaylist.get_Item(i).name;
        }

        // Display the media item names.
        playlistItems.Lines = mediaItems;
        break;
      
        default:
            break;
    }
}
```


```VB

Public Sub player_CurrentPlaylistChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEvent) Handles player.CurrentPlaylistChange

    Select Case e.change

        &#39; Only update the list for the move, delete, insert, and append event types.
        Case WMPLib.WMPPlaylistChangeEventType.wmplcMove   &#39; Value = 3
        Case WMPLib.WMPPlaylistChangeEventType.wmplcDelete &#39; Value = 4
        Case WMPLib.WMPPlaylistChangeEventType.wmplcInsert &#39; Value = 5
        Case WMPLib.WMPPlaylistChangeEventType.wmplcAppend &#39; Value = 6

            &#39; Create a string array large enough to hold all of the media item names.
            Dim count As Integer = player.currentPlaylist.count
            Dim mediaItems(count) As String

            &#39; Clear any previous contents of the text box.
            playlistItems.Clear()

            &#39; Loop through the playlist and store each media item name.
            For i As Integer = 0 To (count - 1)

                mediaItems(i) = player.currentPlaylist.Item(i).name

            Next i

            &#39; Display the media item names.
            playlistItems.Lines = mediaItems
    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="576ef-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="576ef-120">Requirements</span></span>



| <span data-ttu-id="576ef-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="576ef-121">Requirement</span></span> | <span data-ttu-id="576ef-122">Value</span><span class="sxs-lookup"><span data-stu-id="576ef-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="576ef-123">Versión</span><span class="sxs-lookup"><span data-stu-id="576ef-123">Version</span></span><br/>   | <span data-ttu-id="576ef-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="576ef-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="576ef-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="576ef-125">Namespace</span></span><br/> | <span data-ttu-id="576ef-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="576ef-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="576ef-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="576ef-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="576ef-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="576ef-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="576ef-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="576ef-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="576ef-130">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="576ef-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="576ef-131">**AxWindowsMediaPlayer. currentPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="576ef-131">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="576ef-132">**Evento AxWindowsMediaPlayer. PlaylistChange (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="576ef-132">**AxWindowsMediaPlayer.PlaylistChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playlistchange.md)
</dt> <dt>

[<span data-ttu-id="576ef-133">**WMPPlaylistChangeEventType**</span><span class="sxs-lookup"><span data-stu-id="576ef-133">**WMPPlaylistChangeEventType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaylistchangeeventtype)
</dt> </dl>

 

 





