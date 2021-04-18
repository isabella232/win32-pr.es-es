---
title: IWMPMedia isMemberOf, método
description: El método isMemberOf devuelve un valor que indica si el elemento multimedia especificado es un miembro de la lista de reproducción especificada.
ms.assetid: 491e0dd5-38e5-47a5-9c94-f1d27d297f8d
keywords:
- método isMemberOf de Windows Media Player
- método isMemberOf Windows Media Player, interfaz IWMPMedia
- Interfaz IWMPMedia Windows Media Player, método isMemberOf
topic_type:
- apiref
api_name:
- IWMPMedia.isMemberOf
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f627e9b2f0e1c4b226dda13d280d521ad52df2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671574"
---
# <a name="iwmpmediaismemberof-method"></a><span data-ttu-id="bba21-106">IWMPMedia:: isMemberOf (método)</span><span class="sxs-lookup"><span data-stu-id="bba21-106">IWMPMedia::isMemberOf method</span></span>

<span data-ttu-id="bba21-107">El método **isMemberOf** devuelve un valor que indica si el elemento multimedia especificado es un miembro de la lista de reproducción especificada.</span><span class="sxs-lookup"><span data-stu-id="bba21-107">The **isMemberOf** method returns a value indicating whether the specified media item is a member of the specified playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="bba21-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bba21-108">Syntax</span></span>


```CSharp
public System.Boolean isMemberOf(
  IWMPPlaylist pPlaylist
);
```


```VB

Public Function isMemberOf( _
  ByVal pPlaylist As IWMPPlaylist _
) As System.Boolean
Implements IWMPMedia.isMemberOf
```





## <a name="parameters"></a><span data-ttu-id="bba21-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bba21-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bba21-110">*pPlaylist* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bba21-110">*pPlaylist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba21-111">Una interfaz **WMPLib. IWMPPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="bba21-111">A **WMPLib.IWMPPlaylist** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bba21-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bba21-112">Return value</span></span>

<span data-ttu-id="bba21-113">Valor **System. Boolean** que indica si el elemento multimedia es un miembro de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="bba21-113">A **System.Boolean** value that indicates whether the media item is a member of the playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="bba21-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bba21-114">Remarks</span></span>

<span data-ttu-id="bba21-115">Este método no puede comprobar las listas de reproducción recuperadas a través de la interfaz **IWMPMediaCollection** .</span><span class="sxs-lookup"><span data-stu-id="bba21-115">This method cannot check playlists retrieved through the **IWMPMediaCollection** interface.</span></span> <span data-ttu-id="bba21-116">Para probar si un elemento multimedia es miembro de una lista de reproducción con nombre determinada, recupere la colección de listas de reproducción con la propiedad **AxWindowsMediaPlayer. playlistCollection** .</span><span class="sxs-lookup"><span data-stu-id="bba21-116">To test whether a media item is a member of a particular named playlist, retrieve the playlist collection with the **AxWindowsMediaPlayer.playlistCollection** property.</span></span> <span data-ttu-id="bba21-117">Una vez recuperada la colección, recupere la lista de reproducción individual llamando al método **IWMPPlaylistCollection. getByName** .</span><span class="sxs-lookup"><span data-stu-id="bba21-117">Once you retrieve the collection, retrieve the individual playlist by calling the **IWMPPlaylistCollection.getByName** method.</span></span>

<span data-ttu-id="bba21-118">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="bba21-118">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="bba21-119">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="bba21-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bba21-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bba21-120">Examples</span></span>

<span data-ttu-id="bba21-121">En el ejemplo siguiente se usa **isMemberOf** para comprobar si el elemento multimedia actual es un miembro de la lista de reproducción denominada All Music.</span><span class="sxs-lookup"><span data-stu-id="bba21-121">The following example uses **isMemberOf** to test whether the current media item is a member of the playlist named All Music.</span></span> <span data-ttu-id="bba21-122">Si no es así, el elemento multimedia actual se anexa a la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="bba21-122">If it is not, the current media item is appended to the playlist.</span></span> <span data-ttu-id="bba21-123">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="bba21-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the playlist named All Music.
WMPLib.IWMPPlaylist sPlaylist = player.playlistCollection.getByName("All Music").Item(0);

// Test whether the current media item is a member of the All Music playlist.
// If it is not a member, append the current media item to the playlist.
if (player.currentMedia.isMemberOf(sPlaylist) == false)
{
    sPlaylist.appendItem(player.currentMedia);
}
```


```VB

' Get an interface to the playlist named All Music.
Dim sPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Test whether the current media item is a member of the All Music playlist.
&#39; If it is not a member, then append the current media item to the playlist.
If (player.currentMedia.isMemberOf(sPlaylist) = False) Then

    sPlaylist.appendItem(player.currentMedia)

End If
```





## <a name="requirements"></a><span data-ttu-id="bba21-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bba21-124">Requirements</span></span>



| <span data-ttu-id="bba21-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bba21-125">Requirement</span></span> | <span data-ttu-id="bba21-126">Value</span><span class="sxs-lookup"><span data-stu-id="bba21-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bba21-127">Versión</span><span class="sxs-lookup"><span data-stu-id="bba21-127">Version</span></span><br/>   | <span data-ttu-id="bba21-128">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="bba21-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="bba21-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bba21-129">Namespace</span></span><br/> | <span data-ttu-id="bba21-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="bba21-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="bba21-131">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="bba21-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bba21-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="bba21-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bba21-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="bba21-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba21-134">**AxWindowsMediaPlayer. playlistCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="bba21-134">**AxWindowsMediaPlayer.playlistCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bba21-135">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="bba21-135">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bba21-136">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="bba21-136">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bba21-137">**IWMPPlaylistCollection. getByName (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="bba21-137">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





