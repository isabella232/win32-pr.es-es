---
title: IWMPPlaylistCollection reproducción, método
description: El método reproducción devuelve una interfaz IWMPPlaylist para una nueva lista de reproducción vacía en la biblioteca.
ms.assetid: cc0cb356-9a90-421c-8d1a-b79585f71124
keywords:
- método reproducción de Windows Media Player
- método reproducción Windows Media Player, interfaz IWMPPlaylistCollection
- Interfaz IWMPPlaylistCollection Windows Media Player, método reproducción
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.newPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbc455c5815cee1aaac139886bca1d847ddc62b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708219"
---
# <a name="iwmpplaylistcollectionnewplaylist-method"></a><span data-ttu-id="c1e7b-106">IWMPPlaylistCollection:: reproducción (método)</span><span class="sxs-lookup"><span data-stu-id="c1e7b-106">IWMPPlaylistCollection::newPlaylist method</span></span>

<span data-ttu-id="c1e7b-107">El método **reproducción** devuelve una interfaz **IWMPPlaylist** para una nueva lista de reproducción vacía en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c1e7b-107">The **newPlaylist** method returns an **IWMPPlaylist** interface for a new, empty playlist in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1e7b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1e7b-108">Syntax</span></span>


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.newPlaylist
```





## <a name="parameters"></a><span data-ttu-id="c1e7b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1e7b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1e7b-110">*bstrName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1e7b-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e7b-111">**System. String** que es el nombre de la nueva lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="c1e7b-111">A **System.String** that is the name of the new playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1e7b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1e7b-112">Return value</span></span>

<span data-ttu-id="c1e7b-113">Una interfaz **WMPLib. IWMPPlaylist** para la nueva lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="c1e7b-113">A **WMPLib.IWMPPlaylist** interface for the new playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1e7b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1e7b-114">Remarks</span></span>

<span data-ttu-id="c1e7b-115">Este método crea una lista de reproducción vacía en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c1e7b-115">This method creates an empty playlist in the library.</span></span> <span data-ttu-id="c1e7b-116">Para rellenar la lista de reproducción con elementos multimedia, use **IWMPPlaylist. appendItem** o **IWMPPlaylist. insertItem**.</span><span class="sxs-lookup"><span data-stu-id="c1e7b-116">To fill the playlist with media items, use **IWMPPlaylist.appendItem** or **IWMPPlaylist.insertItem**.</span></span>

<span data-ttu-id="c1e7b-117">En la biblioteca se permiten varias listas de reproducción con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="c1e7b-117">Multiple playlists having the same name are permitted in the library.</span></span> <span data-ttu-id="c1e7b-118">Para evitar la creación de un nombre de lista de reproducción duplicado con este método, use el método **getByName** y **IWMPPlaylistArray. Count** para detectar si ya existe una lista de reproducción con un nombre determinado.</span><span class="sxs-lookup"><span data-stu-id="c1e7b-118">To avoid creating a duplicate playlist name with this method, use the **getByName** method and **IWMPPlaylistArray.count** to discover whether a playlist with a particular name already exists.</span></span>

<span data-ttu-id="c1e7b-119">Los espacios iniciales y finales no se permiten en los nombres de las listas de reproducción y se quitan automáticamente del valor especificado para el parámetro *bstrName* .</span><span class="sxs-lookup"><span data-stu-id="c1e7b-119">Leading and trailing spaces are not permitted in playlist names, and are automatically removed from the value specified for the *bstrName* parameter.</span></span>

<span data-ttu-id="c1e7b-120">Antes de llamar a este método, debe tener acceso total a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c1e7b-120">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="c1e7b-121">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c1e7b-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c1e7b-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c1e7b-122">Examples</span></span>

<span data-ttu-id="c1e7b-123">En el ejemplo siguiente se crea una nueva lista de reproducción vacía denominada "ThreeList", se agrega a la colección de listas de reproducción y se le devuelve una interfaz.</span><span class="sxs-lookup"><span data-stu-id="c1e7b-123">The following example creates a new empty playlist called "ThreeList", adds it to the playlist collection, and returns an interface to it.</span></span> <span data-ttu-id="c1e7b-124">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="c1e7b-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a new empty playlist, named ThreeList, to the playlist collection.
WMPLib.IWMPPlaylist newList = player.playlistCollection.newPlaylist("ThreeList");
```


```VB

'  Add a new empty playlist, named ThreeList, to the playlist collection.
Dim newList As WMPLib.IWMPPlaylist = player.playlistCollection.newPlaylist(&quot;ThreeList&quot;)
```





## <a name="requirements"></a><span data-ttu-id="c1e7b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1e7b-125">Requirements</span></span>



| <span data-ttu-id="c1e7b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1e7b-126">Requirement</span></span> | <span data-ttu-id="c1e7b-127">Value</span><span class="sxs-lookup"><span data-stu-id="c1e7b-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e7b-128">Versión</span><span class="sxs-lookup"><span data-stu-id="c1e7b-128">Version</span></span><br/>   | <span data-ttu-id="c1e7b-129">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="c1e7b-129">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="c1e7b-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c1e7b-130">Namespace</span></span><br/> | <span data-ttu-id="c1e7b-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c1e7b-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c1e7b-132">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="c1e7b-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c1e7b-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c1e7b-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1e7b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1e7b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1e7b-135">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c1e7b-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c1e7b-136">**IWMPPlaylist. appendItem (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c1e7b-136">**IWMPPlaylist.appendItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c1e7b-137">**IWMPPlaylist. insertItem (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c1e7b-137">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c1e7b-138">**IWMPPlaylistArray. Count (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c1e7b-138">**IWMPPlaylistArray.count (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c1e7b-139">**Interfaz IWMPPlaylistCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c1e7b-139">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c1e7b-140">**IWMPPlaylistCollection. getByName (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c1e7b-140">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





