---
title: IWMPPlaylistCollection importPlaylist, método
description: El método importPlaylist agrega una lista de reproducción estática a la biblioteca. | IWMPPlaylistCollection importPlaylist, método
ms.assetid: 7a64e618-920d-419d-8769-612ab5dff49b
keywords:
- método importPlaylist de Windows Media Player
- método importPlaylist Windows Media Player, interfaz IWMPPlaylistCollection
- Interfaz IWMPPlaylistCollection Windows Media Player, método importPlaylist
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.importPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3ca727155d6ae859123d427812d93ebaa0b05c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708220"
---
# <a name="iwmpplaylistcollectionimportplaylist-method"></a><span data-ttu-id="bb23f-107">IWMPPlaylistCollection:: importPlaylist (método)</span><span class="sxs-lookup"><span data-stu-id="bb23f-107">IWMPPlaylistCollection::importPlaylist method</span></span>

<span data-ttu-id="bb23f-108">El método **importPlaylist** agrega una lista de reproducción estática a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="bb23f-108">The **importPlaylist** method adds a static playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb23f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb23f-109">Syntax</span></span>


```CSharp
public IWMPPlaylist importPlaylist(
  IWMPPlaylist pItem
);
```


```VB

Public Function importPlaylist( _
  ByVal pItem As IWMPPlaylist _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.importPlaylist
```





## <a name="parameters"></a><span data-ttu-id="bb23f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb23f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb23f-111">*pItem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb23f-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb23f-112">Una interfaz **WMPLib. IWMPPlaylist** para la lista de reproducción que este método va a agregar.</span><span class="sxs-lookup"><span data-stu-id="bb23f-112">A **WMPLib.IWMPPlaylist** interface for the playlist that this method will add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb23f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb23f-113">Return value</span></span>

<span data-ttu-id="bb23f-114">Una interfaz **WMPLib. IWMPPlaylist** para la lista de reproducción agregada.</span><span class="sxs-lookup"><span data-stu-id="bb23f-114">A **WMPLib.IWMPPlaylist** interface for the added playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb23f-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb23f-115">Remarks</span></span>

<span data-ttu-id="bb23f-116">Las listas de reproducción que no contienen elementos multimedia no se pueden agregar a la biblioteca mediante este método.</span><span class="sxs-lookup"><span data-stu-id="bb23f-116">Playlists that do not contain any media items cannot be added to the library by using this method.</span></span> <span data-ttu-id="bb23f-117">Para crear una lista de reproducción vacía en la biblioteca, use el método **reproducción** .</span><span class="sxs-lookup"><span data-stu-id="bb23f-117">To create an empty playlist in the library, use the **newPlaylist** method.</span></span> <span data-ttu-id="bb23f-118">Después, puede rellenar la lista de reproducción resultante con elementos multimedia mediante **IWMPPlaylist. appendItem** o **IWMPPlaylist. insertItem**.</span><span class="sxs-lookup"><span data-stu-id="bb23f-118">You can then fill the resulting playlist with media items by using **IWMPPlaylist.appendItem** or **IWMPPlaylist.insertItem**.</span></span>

<span data-ttu-id="bb23f-119">Si pasa este método a una lista de reproducción automática, la consulta se ejecuta una vez y el resultado se agrega a la biblioteca como una lista de reproducción estática.</span><span class="sxs-lookup"><span data-stu-id="bb23f-119">If you pass this method an auto playlist, the query is executed once and the result is added to the library as a static playlist.</span></span> <span data-ttu-id="bb23f-120">Para agregar una lista de reproducción automática a la biblioteca y conservar su comportamiento automático, use **IWMPMediaCollection. Add**.</span><span class="sxs-lookup"><span data-stu-id="bb23f-120">To add an auto playlist to the library and preserve its automatic behavior, use **IWMPMediaCollection.add**.</span></span> <span data-ttu-id="bb23f-121">Para obtener más información, vea [listas de reproducción estáticas y automáticas](static-and-auto-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="bb23f-121">For more information, see [Static and Auto Playlists](static-and-auto-playlists.md).</span></span>

<span data-ttu-id="bb23f-122">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="bb23f-122">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="bb23f-123">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="bb23f-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb23f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb23f-124">Requirements</span></span>



| <span data-ttu-id="bb23f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb23f-125">Requirement</span></span> | <span data-ttu-id="bb23f-126">Value</span><span class="sxs-lookup"><span data-stu-id="bb23f-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb23f-127">Versión</span><span class="sxs-lookup"><span data-stu-id="bb23f-127">Version</span></span><br/>   | <span data-ttu-id="bb23f-128">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="bb23f-128">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="bb23f-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bb23f-129">Namespace</span></span><br/> | <span data-ttu-id="bb23f-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="bb23f-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="bb23f-131">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="bb23f-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bb23f-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="bb23f-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb23f-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb23f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb23f-134">**IWMPMediaCollection. Add (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="bb23f-134">**IWMPMediaCollection.add (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bb23f-135">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="bb23f-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bb23f-136">**IWMPPlaylist. appendItem (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="bb23f-136">**IWMPPlaylist.appendItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bb23f-137">**IWMPPlaylist. insertItem (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="bb23f-137">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bb23f-138">**Interfaz IWMPPlaylistCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="bb23f-138">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bb23f-139">**IWMPPlaylistCollection. reproducción (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="bb23f-139">**IWMPPlaylistCollection.newPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





