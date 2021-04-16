---
title: PlaylistCollection. isDeleted (método)
description: El método isDeleted recupera un valor que indica si la lista de reproducción especificada está en la carpeta elementos eliminados.
ms.assetid: 5023927a-5d1a-4b61-8122-476947d537c4
keywords:
- método isDeleted Windows Media Player
- método isDeleted Windows Media Player, clase PlaylistCollection
- Clase PlaylistCollection Windows Media Player, método isDeleted
topic_type:
- apiref
api_name:
- PlaylistCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fed3e7e8ff41f23d0f9f741ea99f3382d20532e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718815"
---
# <a name="playlistcollectionisdeleted-method"></a><span data-ttu-id="0077b-106">PlaylistCollection. isDeleted (método)</span><span class="sxs-lookup"><span data-stu-id="0077b-106">PlaylistCollection.isDeleted method</span></span>

<span data-ttu-id="0077b-107">El método **IsDeleted** recupera un valor que indica si la lista de reproducción especificada está en la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="0077b-107">The **isDeleted** method retrieves a value indicating whether the specified playlist is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="0077b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0077b-108">Syntax</span></span>


```JScript
bRetVal = PlaylistCollection.isDeleted(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="0077b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0077b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0077b-110">*lista de reproducción* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0077b-110">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0077b-111">Objeto de **lista de reproducción** que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="0077b-111">The **Playlist** object to be searched for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0077b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0077b-112">Return value</span></span>

<span data-ttu-id="0077b-113">Este método devuelve un **valor booleano**.</span><span class="sxs-lookup"><span data-stu-id="0077b-113">This method returns a **Boolean**.</span></span>

<span data-ttu-id="0077b-114">**Windows Media Player 10 Mobile**: este método siempre devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="0077b-114">**Windows Media Player 10 Mobile**: This method always returns **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0077b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0077b-115">Requirements</span></span>



| <span data-ttu-id="0077b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0077b-116">Requirement</span></span> | <span data-ttu-id="0077b-117">Value</span><span class="sxs-lookup"><span data-stu-id="0077b-117">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0077b-118">Versión</span><span class="sxs-lookup"><span data-stu-id="0077b-118">Version</span></span><br/> | <span data-ttu-id="0077b-119">Windows Media Player versión 7,0, Windows Media Player versión 7,1 o Windows Media Player para Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0077b-119">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="0077b-120">Este método no es compatible con Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="0077b-120">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="0077b-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0077b-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="0077b-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0077b-122"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="0077b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="0077b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0077b-124">**Objeto PlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="0077b-124">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> </dl>

 

 





