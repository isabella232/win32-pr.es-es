---
title: Propiedad AxWindowsMediaPlayer. currentPlaylist
description: La propiedad currentPlaylist obtiene o establece la interfaz IWMPPlaylist actual que proporciona una manera sencilla de organizar y manipular los elementos multimedia de una lista.
ms.assetid: d5a9f126-a628-499c-a012-8a47c6c987ef
keywords:
- propiedades de currentPlaylist Media Player de Windows
- propiedad currentPlaylist Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad currentPlaylist
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0f5b91a2e65b81fd1f13da0bad5f77c5ea1415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699938"
---
# <a name="axwindowsmediaplayercurrentplaylist-property"></a><span data-ttu-id="08a54-106">Propiedad AxWindowsMediaPlayer. currentPlaylist</span><span class="sxs-lookup"><span data-stu-id="08a54-106">AxWindowsMediaPlayer.currentPlaylist property</span></span>

<span data-ttu-id="08a54-107">La propiedad currentPlaylist obtiene o establece la interfaz **IWMPPlaylist** actual que proporciona una manera sencilla de organizar y manipular los elementos multimedia de una lista.</span><span class="sxs-lookup"><span data-stu-id="08a54-107">The currentPlaylist property gets or sets the current **IWMPPlaylist** interface that provides an easy way to organize and manipulate media items in a list.</span></span>

## <a name="syntax"></a><span data-ttu-id="08a54-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08a54-108">Syntax</span></span>


```CSharp
public IWMPPlaylist currentPlaylist {get; set;}
```


```VB

Public Property currentPlaylist As IWMPPlaylist
```





## <a name="property-value"></a><span data-ttu-id="08a54-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="08a54-109">Property value</span></span>

<span data-ttu-id="08a54-110">La interfaz WMPLib. IWMPPlaylist que proporciona acceso a la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="08a54-110">The WMPLib.IWMPPlaylist interface that provides access to the current playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="08a54-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08a54-111">Remarks</span></span>

<span data-ttu-id="08a54-112">Si la propiedad IWMPSettings. autoStart (también tiene acceso a través de AxWindowsMediaPlayer. Settings.**autoStart**) es true, la reproducción se inicia automáticamente cada vez que se establece **currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="08a54-112">If the IWMPSettings.autoStart property (also accessed via AxWindowsMediaPlayer.settings.**autoStart**) is true, playback begins automatically whenever you set **currentPlaylist**.</span></span>

<span data-ttu-id="08a54-113">Esta propiedad toma una interfaz IWMPPlaylist, que se puede adquirir de varias maneras, por ejemplo, obteniendo el valor de *IWMPPlaylistArray*. **Elemento** o *IWMPPlaylistCollection*. propiedades de **reproducción** .</span><span class="sxs-lookup"><span data-stu-id="08a54-113">This property takes an IWMPPlaylist interface, which can be acquired in several ways, such as by getting the value from the *IWMPPlaylistArray*.**Item** or *IWMPPlaylistCollection*.**newPlaylist** properties.</span></span> <span data-ttu-id="08a54-114">Para cargar un elemento de **lista de reproducción** con un nombre de archivo, establezca la propiedad URL o use AxWindowsMediaPlayer. **reproducción**.</span><span class="sxs-lookup"><span data-stu-id="08a54-114">To load a **playlist** item using a file name, set the URL property or use AxWindowsMediaPlayer.**newPlaylist**.</span></span>

## <a name="examples"></a><span data-ttu-id="08a54-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="08a54-115">Examples</span></span>

<span data-ttu-id="08a54-116">En el ejemplo siguiente se recupera la primera lista de reproducción de la biblioteca y se usa la propiedad currentPlaylist para establecer la lista de reproducción recuperada como la lista de reproducción actual y se muestra su nombre.</span><span class="sxs-lookup"><span data-stu-id="08a54-116">The following example retrieves the first playlist in the library and uses the currentPlaylist property to set the retrieved playlist as the current playlist, and display its name.</span></span> <span data-ttu-id="08a54-117">El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="08a54-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first playlist from the library. 
WMPLib.IWMPPlaylist firstPlaylist = player.playlistCollection.getAll().Item(0);

// Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist;

// Display the name of the current playlist.
currentPlaylistLabel.Text = ("Found first playlist. Name = " + player.currentPlaylist.name);
```


```VB

' Get an interface to the first playlist from the library. 
Dim firstPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getAll().Item(0)

&#39; Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist

&#39; Display the name of the current playlist.
currentPlaylistLabel.Text = (&quot;Found first playlist. Name = &quot; + player.currentPlaylist.name)
```





## <a name="requirements"></a><span data-ttu-id="08a54-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08a54-118">Requirements</span></span>



| <span data-ttu-id="08a54-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="08a54-119">Requirement</span></span> | <span data-ttu-id="08a54-120">Value</span><span class="sxs-lookup"><span data-stu-id="08a54-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08a54-121">Versión</span><span class="sxs-lookup"><span data-stu-id="08a54-121">Version</span></span><br/>   | <span data-ttu-id="08a54-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="08a54-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="08a54-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="08a54-123">Namespace</span></span><br/> | <span data-ttu-id="08a54-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="08a54-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="08a54-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="08a54-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="08a54-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="08a54-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08a54-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="08a54-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a54-128">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="08a54-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="08a54-129">**AxWindowsMediaPlayer. reproducción (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="08a54-129">**AxWindowsMediaPlayer.newPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="08a54-130">**AxWindowsMediaPlayer. Settings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="08a54-130">**AxWindowsMediaPlayer.settings (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="08a54-131">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="08a54-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="08a54-132">**IWMPPlaylistArray. Item (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="08a54-132">**IWMPPlaylistArray.Item (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="08a54-133">**IWMPPlaylistCollection. reproducción (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="08a54-133">**IWMPPlaylistCollection.newPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="08a54-134">**IWMPSettings. autoStart (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="08a54-134">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





