---
title: Atributo SyncOnly
description: El atributo SyncOnly es una representación de cadena de un valor booleano que Windows Media Player usa para determinar si una lista de reproducción solo está disponible para la sincronización.
ms.assetid: 36149bb9-3a0b-4f6d-8be3-97d2a87faa83
keywords:
- SyncOnly Media Player de Windows
topic_type:
- apiref
api_name:
- SyncOnly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0245ffac2c4c64717adf669fcc6ff8fd0768382
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718681"
---
# <a name="synconly-attribute"></a><span data-ttu-id="f63ae-104">Atributo SyncOnly</span><span class="sxs-lookup"><span data-stu-id="f63ae-104">SyncOnly Attribute</span></span>

<span data-ttu-id="f63ae-105">El atributo **SyncOnly** es una representación de cadena de un valor **booleano** que Windows Media Player usa para determinar si una lista de reproducción solo está disponible para la sincronización.</span><span class="sxs-lookup"><span data-stu-id="f63ae-105">The **SyncOnly** attribute is a string representation of a **Boolean** value that Windows Media Player uses to determine whether a playlist is available only for synchronization.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f63ae-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="f63ae-106">Applies To</span></span>

-   [<span data-ttu-id="f63ae-107">Reproducción</span><span class="sxs-lookup"><span data-stu-id="f63ae-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="f63ae-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f63ae-108">Remarks</span></span>

<span data-ttu-id="f63ae-109">Un valor de 1 indica que la lista de reproducción solo está disponible para la sincronización y no puede aparecer en el nodo de **lista de reproducción automática** .</span><span class="sxs-lookup"><span data-stu-id="f63ae-109">A value of 1 indicates that the playlist is available only for synchronization and cannot appear in the **Auto Playlist** node.</span></span> <span data-ttu-id="f63ae-110">Un valor de cero indica que la lista de reproducción puede aparecer en el nodo de **lista de reproducción automática** .</span><span class="sxs-lookup"><span data-stu-id="f63ae-110">A value of zero indicates that the playlist can appear in the **Auto Playlist** node.</span></span>

<span data-ttu-id="f63ae-111">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="f63ae-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f63ae-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f63ae-112">Requirements</span></span>



| <span data-ttu-id="f63ae-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f63ae-113">Requirement</span></span> | <span data-ttu-id="f63ae-114">Value</span><span class="sxs-lookup"><span data-stu-id="f63ae-114">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="f63ae-115">Versión</span><span class="sxs-lookup"><span data-stu-id="f63ae-115">Version</span></span><br/> | <span data-ttu-id="f63ae-116">Windows Media Player 10 o posterior</span><span class="sxs-lookup"><span data-stu-id="f63ae-116">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f63ae-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="f63ae-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f63ae-118">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="f63ae-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





