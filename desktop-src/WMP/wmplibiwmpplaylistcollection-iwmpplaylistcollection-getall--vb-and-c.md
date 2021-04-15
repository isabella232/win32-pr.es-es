---
title: IWMPPlaylistCollection getAll (método)
description: El método getAll devuelve una interfaz IWMPPlaylistArray que proporciona acceso a todas las listas de reproducción de la biblioteca.
ms.assetid: d36dbc5c-ccb0-400a-ab5b-918598c218f1
keywords:
- getAll (método) de Windows Media Player
- getAll (método) Windows Media Player, interfaz IWMPPlaylistCollection
- Interfaz IWMPPlaylistCollection Windows Media Player, método getAll
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4260f5c960650cf6c04a1dd8b39d887f711fb8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708998"
---
# <a name="iwmpplaylistcollectiongetall-method"></a><span data-ttu-id="e9758-106">IWMPPlaylistCollection:: getAll (método)</span><span class="sxs-lookup"><span data-stu-id="e9758-106">IWMPPlaylistCollection::getAll method</span></span>

<span data-ttu-id="e9758-107">El método **getAll** devuelve una interfaz **IWMPPlaylistArray** que proporciona acceso a todas las listas de reproducción de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e9758-107">The **getAll** method returns an **IWMPPlaylistArray** interface that provides access to all of the playlists in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9758-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9758-108">Syntax</span></span>


```CSharp
public IWMPPlaylistArray getAll();
```


```VB

Public Function getAll() As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getAll
```





## <a name="parameters"></a><span data-ttu-id="e9758-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9758-109">Parameters</span></span>

<span data-ttu-id="e9758-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e9758-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e9758-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9758-111">Return value</span></span>

<span data-ttu-id="e9758-112">Una interfaz **WMPLib. IWMPPlaylistArray** para la matriz de listas de reproducción recuperada.</span><span class="sxs-lookup"><span data-stu-id="e9758-112">A **WMPLib.IWMPPlaylistArray** interface for the retrieved array of playlists.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9758-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9758-113">Remarks</span></span>

<span data-ttu-id="e9758-114">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e9758-114">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="e9758-115">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e9758-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9758-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9758-116">Requirements</span></span>



| <span data-ttu-id="e9758-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9758-117">Requirement</span></span> | <span data-ttu-id="e9758-118">Value</span><span class="sxs-lookup"><span data-stu-id="e9758-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9758-119">Versión</span><span class="sxs-lookup"><span data-stu-id="e9758-119">Version</span></span><br/>   | <span data-ttu-id="e9758-120">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="e9758-120">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="e9758-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e9758-121">Namespace</span></span><br/> | <span data-ttu-id="e9758-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e9758-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e9758-123">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="e9758-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e9758-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e9758-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9758-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9758-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9758-126">**Interfaz IWMPPlaylistArray (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="e9758-126">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e9758-127">**Interfaz IWMPPlaylistCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="e9758-127">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





