---
title: IWMPPlaylistCollection getByName, método
description: El método getByName devuelve una interfaz IWMPPlaylistArray que proporciona acceso a las listas de reproducción con el nombre especificado, si existe alguna.
ms.assetid: d41afab1-4103-4f59-a432-21a502499444
keywords:
- método getByName de Windows Media Player
- método getByName Windows Media Player, interfaz IWMPPlaylistCollection
- Interfaz IWMPPlaylistCollection Windows Media Player, método getByName
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e51f83b4db019286c04762a081e649fec282135e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709080"
---
# <a name="iwmpplaylistcollectiongetbyname-method"></a><span data-ttu-id="38410-106">IWMPPlaylistCollection:: getByName (método)</span><span class="sxs-lookup"><span data-stu-id="38410-106">IWMPPlaylistCollection::getByName method</span></span>

<span data-ttu-id="38410-107">El método **getByName** devuelve una interfaz **IWMPPlaylistArray** que proporciona acceso a las listas de reproducción con el nombre especificado, si existe alguna.</span><span class="sxs-lookup"><span data-stu-id="38410-107">The **getByName** method returns a **IWMPPlaylistArray** interface that provides access to playlists with the specified name, if any exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="38410-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38410-108">Syntax</span></span>


```CSharp
public IWMPPlaylistArray getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getByName
```





## <a name="parameters"></a><span data-ttu-id="38410-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38410-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38410-110">*bstrName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="38410-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38410-111">**System. String** que es el nombre de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="38410-111">A **System.String** that is the name of the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38410-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38410-112">Return value</span></span>

<span data-ttu-id="38410-113">Una interfaz **WMPLib. IWMPPlaylistArray** para la matriz de listas de reproducción recuperada.</span><span class="sxs-lookup"><span data-stu-id="38410-113">A **WMPLib.IWMPPlaylistArray** interface for the retrieved array of playlists.</span></span>

## <a name="remarks"></a><span data-ttu-id="38410-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38410-114">Remarks</span></span>

<span data-ttu-id="38410-115">Use **IWMPPlaylistArray. Count** para determinar si existe una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="38410-115">Use **IWMPPlaylistArray.count** to determine whether a playlist exists.</span></span> <span data-ttu-id="38410-116">Si **Count** es cero, la matriz está vacía.</span><span class="sxs-lookup"><span data-stu-id="38410-116">If **count** is zero, the array is empty.</span></span>

<span data-ttu-id="38410-117">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="38410-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="38410-118">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="38410-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="38410-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="38410-119">Examples</span></span>

<span data-ttu-id="38410-120">En el ejemplo siguiente se usa **getByName** para comprobar en la colección de listas de reproducción una lista de reproducción denominada "Favorites--4 and 5 Star clasificód".</span><span class="sxs-lookup"><span data-stu-id="38410-120">The following example uses **getByName** to check the playlist collection for a playlist named "Favorites -- 4 and 5 star rated".</span></span> <span data-ttu-id="38410-121">Si existe una lista de reproducción con ese nombre, **getByName** la establece como la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="38410-121">If a playlist by that name exists, **getByName** sets it as the current playlist.</span></span> <span data-ttu-id="38410-122">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="38410-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the count of the playlists named "Favorites -- 4 and 5 star rated".
int checkit = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").count;

// Since duplicate playlist names are allowed, the count returned
// will be either zero (no playlist) or greater than zero (playlist exists).
if (checkit > 0)
{
    // Retrieve a playlist array containing "Favorites -- 4 and 5 star rated".
    // Assume that there is only one playlist with that name, and assign it to the 
    // current playlist.
    player.currentPlaylist = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").Item(0);
}
```


```VB

'  Get the count of the playlists named &quot;Favorites -- 4 and 5 star rated&quot;.
Dim checkit As Integer = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).count

&#39;  Since duplicate playlist names are allowed, the count returned
&#39;  will be either zero (no playlist) or greater than zero (playlist exists).
If (checkit > 0) Then

    &#39;  Retrieve a playlist array object containing &quot;Favorites -- 4 and 5 star rated&quot;.
    &#39;  Assume that there is only one playlist with that name, and assign it to the 
    &#39;  current playlist.
    player.currentPlaylist = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).Item(0)

End If
```





## <a name="requirements"></a><span data-ttu-id="38410-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38410-123">Requirements</span></span>



| <span data-ttu-id="38410-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="38410-124">Requirement</span></span> | <span data-ttu-id="38410-125">Value</span><span class="sxs-lookup"><span data-stu-id="38410-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38410-126">Versión</span><span class="sxs-lookup"><span data-stu-id="38410-126">Version</span></span><br/>   | <span data-ttu-id="38410-127">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="38410-127">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="38410-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="38410-128">Namespace</span></span><br/> | <span data-ttu-id="38410-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="38410-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="38410-130">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="38410-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="38410-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="38410-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38410-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="38410-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38410-133">**Interfaz IWMPPlaylistArray (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="38410-133">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="38410-134">**IWMPPlaylistArray. Count (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="38410-134">**IWMPPlaylistArray.count (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="38410-135">**Interfaz IWMPPlaylistCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="38410-135">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





