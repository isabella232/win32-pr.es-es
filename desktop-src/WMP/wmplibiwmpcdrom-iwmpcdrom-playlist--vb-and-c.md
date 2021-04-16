---
title: Propiedad de lista de reproducción IWMPCdrom
description: La propiedad playlist obtiene una interfaz IWMPPlaylist que representa las pistas del CD que se encuentran actualmente en la unidad de CD o en las entradas de título de nivel de raíz de un DVD.
ms.assetid: 09c3db45-6586-4a5b-b72c-77c64473bdd0
keywords:
- Propiedades de la lista de reproducción Windows Media Player
- Propiedad de lista de reproducción Windows Media Player, interfaz IWMPCdrom
- Interfaz IWMPCdrom Windows Media Player, propiedad playlist
topic_type:
- apiref
api_name:
- IWMPCdrom.Playlist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a386881c8416f4ea1881f3ccd68ee4291aa3fa84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718845"
---
# <a name="iwmpcdromplaylist-property"></a><span data-ttu-id="3f04a-106">IWMPCdrom::P propiedad laylist</span><span class="sxs-lookup"><span data-stu-id="3f04a-106">IWMPCdrom::Playlist property</span></span>

<span data-ttu-id="3f04a-107">La propiedad **playlist** obtiene una interfaz **IWMPPlaylist** que representa las pistas del CD que se encuentran actualmente en la unidad de CD o en las entradas de título de nivel de raíz de un DVD.</span><span class="sxs-lookup"><span data-stu-id="3f04a-107">The **Playlist** property gets an **IWMPPlaylist** interface representing the tracks on the CD currently in the CD drive or the root-level title entries for a DVD.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f04a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f04a-108">Syntax</span></span>


```CSharp
public IWMPPlaylist Playlist {get; set;}
```


```VB

Public ReadOnly Property Playlist As IWMPPlaylist
```





## <a name="property-value"></a><span data-ttu-id="3f04a-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3f04a-109">Property value</span></span>

<span data-ttu-id="3f04a-110">Una interfaz **WMPLib. IWMPPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="3f04a-110">A **WMPLib.IWMPPlaylist** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f04a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f04a-111">Remarks</span></span>

<span data-ttu-id="3f04a-112">Normalmente, el contenido basado en DVD se organiza en títulos.</span><span class="sxs-lookup"><span data-stu-id="3f04a-112">Typically, DVD-based content organized into titles.</span></span> <span data-ttu-id="3f04a-113">Cada título contiene uno o varios capítulos.</span><span class="sxs-lookup"><span data-stu-id="3f04a-113">Each title contains one or more chapters.</span></span> <span data-ttu-id="3f04a-114">Cada DVD se crea de forma diferente, por lo que la forma de usar títulos y capítulos depende del autor del contenido.</span><span class="sxs-lookup"><span data-stu-id="3f04a-114">Each DVD is authored differently, so how titles and chapters are used is up to the content author.</span></span>

<span data-ttu-id="3f04a-115">En un DVD, esta propiedad obtiene una lista de reproducción que contiene como primer elemento una interfaz **IWMPMedia** denominada "DVD".</span><span class="sxs-lookup"><span data-stu-id="3f04a-115">For a DVD, this property gets a playlist that contains as the first item an **IWMPMedia** interface named "DVD".</span></span> <span data-ttu-id="3f04a-116">Esta interfaz representa el medio DVD.</span><span class="sxs-lookup"><span data-stu-id="3f04a-116">This interface represents the DVD media.</span></span> <span data-ttu-id="3f04a-117">Reproducir el elemento hace que el DVD se reproduzca desde el principio si es el primer juego después de insertar un DVD nuevo o reanudar la reproducción si el DVD es el mismo que el último DVD visualizado.</span><span class="sxs-lookup"><span data-stu-id="3f04a-117">Playing the item results in the DVD playing from the beginning if it is the first play after inserting a new DVD, or resuming playback if the DVD is the same as the last DVD viewed.</span></span> <span data-ttu-id="3f04a-118">Al establecer este elemento como el elemento actual durante la reproducción, el DVD se reproduce desde el principio.</span><span class="sxs-lookup"><span data-stu-id="3f04a-118">Setting this item as the current item during playback results in the DVD playing from the beginning.</span></span>

<span data-ttu-id="3f04a-119">Los elementos adicionales (representados por las interfaces **IWMPMedia** ) de la lista de reproducción son títulos de DVD que se representan mediante listas de reproducción anidadas.</span><span class="sxs-lookup"><span data-stu-id="3f04a-119">Additional items (represented by **IWMPMedia** interfaces) in the playlist are DVD titles that are represented by nested playlists.</span></span> <span data-ttu-id="3f04a-120">Al establecer **IWMPControls. CurrentItem** en uno de estos elementos de lista de reproducción anidados, Windows Media Player establece automáticamente la lista de reproducción anidada como la lista de reproducción actual después de que comience la reproducción del capítulo.</span><span class="sxs-lookup"><span data-stu-id="3f04a-120">When you set **IWMPControls.currentItem** to equal one of these nested playlist items, Windows Media Player automatically sets the nested playlist as the current playlist after chapter playback begins.</span></span> <span data-ttu-id="3f04a-121">A continuación, puede usar las propiedades, los métodos y los eventos asociados de la interfaz **IWMPPlaylist** para trabajar con capítulos de DVD, que también son elementos de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="3f04a-121">You can then use the **IWMPPlaylist** interface properties, methods and associated events to work with DVD chapters, which are also playlist items.</span></span>

<span data-ttu-id="3f04a-122">Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3f04a-122">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="3f04a-123">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3f04a-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3f04a-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3f04a-124">Examples</span></span>

<span data-ttu-id="3f04a-125">En el ejemplo siguiente se usa la lista de **reproducción** para rellenar un cuadro de texto de varias líneas, denominado mi texto, con la lista de seguimiento del CD de audio que se encuentra en la primera unidad de CD.</span><span class="sxs-lookup"><span data-stu-id="3f04a-125">The following example uses **Playlist** to fill a multi-line text box, named myText, with the track list of the audio CD currently in the first CD drive.</span></span> <span data-ttu-id="3f04a-126">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="3f04a-126">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface that provides access to the CD playlist.
WMPLib.IWMPPlaylist playlist = player.cdromCollection.Item(0).Playlist;

// Create a string array to hold the track list.
String[] trackList = new String[playlist.count];

// Iterate through the CD playlist.
for (int i = 0; i < playlist.count; i++)
{
    trackList[i]= playlist.get_Item(i).name;
}

// Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList;
```


```VB

'  Get an interface that provides access to the CD playlist.
Dim playlist As WMPLib.IWMPPlaylist = player.cdromCollection.Item(0).Playlist

&#39;  Create a string array to hold the track list.
Dim trackList(playlist.count) As String

&#39;  Iterate through the CD playlist.
For i As Integer = 0 To (playlist.count - 1)

    trackList(i) = playlist.Item(i).name

Next i

&#39;  Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList
```





## <a name="requirements"></a><span data-ttu-id="3f04a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f04a-127">Requirements</span></span>



| <span data-ttu-id="3f04a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f04a-128">Requirement</span></span> | <span data-ttu-id="3f04a-129">Value</span><span class="sxs-lookup"><span data-stu-id="3f04a-129">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f04a-130">Versión</span><span class="sxs-lookup"><span data-stu-id="3f04a-130">Version</span></span><br/>   | <span data-ttu-id="3f04a-131">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="3f04a-131">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3f04a-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3f04a-132">Namespace</span></span><br/> | <span data-ttu-id="3f04a-133">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3f04a-133">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3f04a-134">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="3f04a-134">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3f04a-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3f04a-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f04a-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f04a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f04a-137">**Interfaz IWMPCdrom (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3f04a-137">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3f04a-138">**IWMPControls. currentItem (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3f04a-138">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3f04a-139">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3f04a-139">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3f04a-140">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3f04a-140">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3f04a-141">**IWMPSettings2. mediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3f04a-141">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3f04a-142">**IWMPSettings2. requestMediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3f04a-142">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





