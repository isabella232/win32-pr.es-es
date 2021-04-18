---
title: IWMPPlaylistCollection isDeleted (método)
description: El método isDeleted devuelve un valor que indica si la lista de reproducción especificada está en la carpeta elementos eliminados.
ms.assetid: 02bc4b9f-6149-4fe2-8417-6484b22f2d74
keywords:
- método isDeleted Windows Media Player
- método isDeleted Windows Media Player, interfaz IWMPPlaylistCollection
- Interfaz IWMPPlaylistCollection Windows Media Player, método isDeleted
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.isDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ce4a314378c5a4a211a52b99ea1b36ae1fda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708146"
---
# <a name="iwmpplaylistcollectionisdeleted-method"></a><span data-ttu-id="6f1ad-106">IWMPPlaylistCollection:: isDeleted (método)</span><span class="sxs-lookup"><span data-stu-id="6f1ad-106">IWMPPlaylistCollection::isDeleted method</span></span>

<span data-ttu-id="6f1ad-107">El método **IsDeleted** devuelve un valor que indica si la lista de reproducción especificada está en la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="6f1ad-107">The **isDeleted** method returns a value indicating whether the specified playlist is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f1ad-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f1ad-108">Syntax</span></span>


```CSharp
public System.Boolean isDeleted(
  IWMPPlaylist pItem
);
```


```VB

Public Function isDeleted( _
  ByVal pItem As IWMPPlaylist _
) As System.Boolean
Implements IWMPPlaylistCollection.isDeleted
```





## <a name="parameters"></a><span data-ttu-id="6f1ad-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f1ad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f1ad-110">*pItem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f1ad-110">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f1ad-111">Una interfaz **WMPLib. IWMPPlaylist** para la lista de reproducción consultada.</span><span class="sxs-lookup"><span data-stu-id="6f1ad-111">A **WMPLib.IWMPPlaylist** interface for the queried playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f1ad-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f1ad-112">Return value</span></span>

<span data-ttu-id="6f1ad-113">**System. Boolean** que especifica si se eliminó la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="6f1ad-113">A **System.Boolean** that specifies whether the playlist was deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f1ad-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f1ad-114">Requirements</span></span>



| <span data-ttu-id="6f1ad-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f1ad-115">Requirement</span></span> | <span data-ttu-id="6f1ad-116">Value</span><span class="sxs-lookup"><span data-stu-id="6f1ad-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f1ad-117">Versión</span><span class="sxs-lookup"><span data-stu-id="6f1ad-117">Version</span></span><br/>   | <span data-ttu-id="6f1ad-118">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="6f1ad-118">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="6f1ad-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6f1ad-119">Namespace</span></span><br/> | <span data-ttu-id="6f1ad-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6f1ad-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6f1ad-121">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="6f1ad-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6f1ad-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6f1ad-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f1ad-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f1ad-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f1ad-124">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="6f1ad-124">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6f1ad-125">**Interfaz IWMPPlaylistCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="6f1ad-125">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





