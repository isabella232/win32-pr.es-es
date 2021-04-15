---
title: Playlist. moveItem (método)
description: El método moveItem cambia la ubicación de un elemento en la lista de reproducción.
ms.assetid: 82a8de86-4419-48a7-89f8-f7b9084b51d4
keywords:
- método moveItem Windows Media Player
- método moveItem Windows Media Player, clase playlist
- Clase PlayList Windows Media Player, método moveItem
topic_type:
- apiref
api_name:
- Playlist.moveItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e2e48b2987af4becd8c07357ff2eecf137f31d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709204"
---
# <a name="playlistmoveitem-method"></a><span data-ttu-id="e20d9-106">Playlist. moveItem (método)</span><span class="sxs-lookup"><span data-stu-id="e20d9-106">Playlist.moveItem method</span></span>

<span data-ttu-id="e20d9-107">El método **moveItem** cambia la ubicación de un elemento en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="e20d9-107">The **moveItem** method changes the location of an item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="e20d9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e20d9-108">Syntax</span></span>


```JScript
Playlist.moveItem(
  oldIndex,
  newIndex
)
```



## <a name="parameters"></a><span data-ttu-id="e20d9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e20d9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e20d9-110">*oldIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e20d9-110">*oldIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e20d9-111">**Número** (**largo**) que contiene el índice anterior.</span><span class="sxs-lookup"><span data-stu-id="e20d9-111">**Number** (**long**) containing the old index.</span></span>

</dd> <dt>

<span data-ttu-id="e20d9-112">*NewIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e20d9-112">*newIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e20d9-113">**Número** (**largo**) que contiene el nuevo índice.</span><span class="sxs-lookup"><span data-stu-id="e20d9-113">**Number** (**long**) containing the new index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e20d9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e20d9-114">Return value</span></span>

<span data-ttu-id="e20d9-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e20d9-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e20d9-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e20d9-116">Remarks</span></span>

<span data-ttu-id="e20d9-117">Las listas de reproducción almacenadas en la biblioteca pueden cambiar fuera del control.</span><span class="sxs-lookup"><span data-stu-id="e20d9-117">Playlists stored in the library can change outside your control.</span></span> <span data-ttu-id="e20d9-118">Asegúrese de supervisar y controlar todos los eventos relacionados con la lista de reproducción adecuados para que el orden de los elementos de la lista de reproducción no cambie de forma inesperada.</span><span class="sxs-lookup"><span data-stu-id="e20d9-118">Be sure to monitor and handle all appropriate playlist-related events so that the order of items in the playlist does not change unexpectedly.</span></span>

<span data-ttu-id="e20d9-119">Para usar este método, se necesita acceso completo a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e20d9-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="e20d9-120">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e20d9-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e20d9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e20d9-121">Requirements</span></span>



| <span data-ttu-id="e20d9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e20d9-122">Requirement</span></span> | <span data-ttu-id="e20d9-123">Value</span><span class="sxs-lookup"><span data-stu-id="e20d9-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e20d9-124">Versión</span><span class="sxs-lookup"><span data-stu-id="e20d9-124">Version</span></span><br/> | <span data-ttu-id="e20d9-125">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="e20d9-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e20d9-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e20d9-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="e20d9-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e20d9-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e20d9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e20d9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e20d9-129">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="e20d9-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="e20d9-130">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="e20d9-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="e20d9-131">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="e20d9-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





