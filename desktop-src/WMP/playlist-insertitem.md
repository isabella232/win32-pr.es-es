---
title: Playlist. insertItem (método)
description: El método insertItem inserta un elemento multimedia en la lista de reproducción de la ubicación especificada.
ms.assetid: c186abc4-0a15-49d2-bbc4-5660e8cc0a4b
keywords:
- método insertItem Media Player Windows
- método insertItem Windows Media Player, clase playlist
- Clase PlayList Windows Media Player, método insertItem
topic_type:
- apiref
api_name:
- Playlist.insertItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a456b7a359d59958ce7693cc48c16eabba435621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708224"
---
# <a name="playlistinsertitem-method"></a><span data-ttu-id="3b479-106">Playlist. insertItem (método)</span><span class="sxs-lookup"><span data-stu-id="3b479-106">Playlist.insertItem method</span></span>

<span data-ttu-id="3b479-107">El método **insertItem** inserta un elemento multimedia en la lista de reproducción de la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="3b479-107">The **insertItem** method inserts a media item into the playlist at the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b479-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b479-108">Syntax</span></span>


```JScript
Playlist.insertItem(
  index,
  item
)
```



## <a name="parameters"></a><span data-ttu-id="3b479-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b479-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b479-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3b479-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b479-111">**Número** (**largo**) que contiene el índice en el que se va a agregar el elemento.</span><span class="sxs-lookup"><span data-stu-id="3b479-111">**Number** (**long**) containing the index at which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="3b479-112">*elemento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3b479-112">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b479-113">Objeto **multimedia** que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="3b479-113">**Media** object to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b479-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b479-114">Return value</span></span>

<span data-ttu-id="3b479-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3b479-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b479-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b479-116">Remarks</span></span>

<span data-ttu-id="3b479-117">Todos los elementos después del elemento insertado tendrán los números de índice incrementados en uno.</span><span class="sxs-lookup"><span data-stu-id="3b479-117">All items after the inserted item will have their index numbers increased by one.</span></span>

<span data-ttu-id="3b479-118">Para usar este método, se necesita acceso completo a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3b479-118">To use this method, full access to the library is required.</span></span> <span data-ttu-id="3b479-119">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3b479-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b479-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b479-120">Requirements</span></span>



| <span data-ttu-id="3b479-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b479-121">Requirement</span></span> | <span data-ttu-id="3b479-122">Value</span><span class="sxs-lookup"><span data-stu-id="3b479-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3b479-123">Versión</span><span class="sxs-lookup"><span data-stu-id="3b479-123">Version</span></span><br/> | <span data-ttu-id="3b479-124">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="3b479-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3b479-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b479-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="3b479-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b479-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b479-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b479-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b479-128">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="3b479-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="3b479-129">**Playlist. Item**</span><span class="sxs-lookup"><span data-stu-id="3b479-129">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="3b479-130">**Lista de reproducción. removeItem**</span><span class="sxs-lookup"><span data-stu-id="3b479-130">**Playlist.removeItem**</span></span>](playlist-removeitem.md)
</dt> <dt>

[<span data-ttu-id="3b479-131">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3b479-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="3b479-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3b479-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





