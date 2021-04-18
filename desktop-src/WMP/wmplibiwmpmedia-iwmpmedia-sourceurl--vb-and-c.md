---
title: Propiedad sourceURL de IWMPMedia
description: La propiedad sourceURL obtiene la dirección URL del elemento multimedia.
ms.assetid: adaef82c-eeed-4cce-859b-c54b9c8fa085
keywords:
- propiedades de sourceURL Media Player de Windows
- propiedad sourceURL de Windows Media Player, interfaz IWMPMedia
- Interfaz IWMPMedia Windows Media Player, propiedad sourceURL
topic_type:
- apiref
api_name:
- IWMPMedia.sourceURL
- IWMPMedia.get_sourceURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ad2cdb2c0a67f65f7b0cf722d1b613307806d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670915"
---
# <a name="iwmpmediasourceurl-property"></a><span data-ttu-id="3f419-106">IWMPMedia:: sourceURL (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3f419-106">IWMPMedia::sourceURL property</span></span>

<span data-ttu-id="3f419-107">La propiedad **sourceURL** obtiene la dirección URL del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="3f419-107">The **sourceURL** property gets the URL of the media item.</span></span>

<span data-ttu-id="3f419-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3f419-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f419-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f419-109">Syntax</span></span>


```CSharp
public System.String sourceURL {get;}
```


```VB

Public ReadOnly Property sourceURL As System.String
```





## <a name="property-value"></a><span data-ttu-id="3f419-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3f419-110">Property value</span></span>

<span data-ttu-id="3f419-111">**System. String** que es la dirección URL de origen.</span><span class="sxs-lookup"><span data-stu-id="3f419-111">A **System.String** that is the source URL.</span></span>

## <a name="examples"></a><span data-ttu-id="3f419-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3f419-112">Examples</span></span>

<span data-ttu-id="3f419-113">En el ejemplo siguiente se usa **sourceURL** para recuperar la dirección URL del primer elemento multimedia de la lista de reproducción "todo el música"; la dirección URL del elemento multimedia se asigna entonces a la propiedad dirección URL del objeto de reproductor.</span><span class="sxs-lookup"><span data-stu-id="3f419-113">The following example uses **sourceURL** to retrieve the URL of the first media item in the "All Music" playlist; the URL of the media item is then assigned to the player object URL property.</span></span> <span data-ttu-id="3f419-114">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="3f419-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the All Music Playlist. 
WMPLib.IWMPPlaylist pl = player.playlistCollection.getByName("All Music").Item(0);

// Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)pl.get_Item(0);

// Change the URL property of the player to the URL of the media item.
player.URL = media.sourceURL;

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Get an interface to the All Music Playlist. 
Dim pl As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
Dim media As WMPLib.IWMPMedia3 = pl.Item(0)

&#39; Change the URL property of the player to the URL of the media item.
player.URL = Media.sourceURL

&#39; Play the media item.
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="3f419-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f419-115">Requirements</span></span>



| <span data-ttu-id="3f419-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f419-116">Requirement</span></span> | <span data-ttu-id="3f419-117">Value</span><span class="sxs-lookup"><span data-stu-id="3f419-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f419-118">Versión</span><span class="sxs-lookup"><span data-stu-id="3f419-118">Version</span></span><br/>   | <span data-ttu-id="3f419-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="3f419-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3f419-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3f419-120">Namespace</span></span><br/> | <span data-ttu-id="3f419-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3f419-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3f419-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="3f419-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3f419-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3f419-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f419-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f419-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f419-125">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3f419-125">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





