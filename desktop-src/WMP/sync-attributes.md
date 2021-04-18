---
title: Atributos de sincronización
description: Los atributos Sync01 a Sync16 son representaciones de cadena de valores de 32 bits que Windows Media Player usa al sincronizar listas de reproducción con uno de hasta 16 dispositivos portátiles.
ms.assetid: b9ae3420-aa09-4969-8637-f16d438942f3
keywords:
- Atributos de sincronización de Windows Media Player
topic_type:
- apiref
api_name:
- Sync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5af26ae563a38efcc40b0bcd319c5fc62b4776dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718682"
---
# <a name="sync-attributes"></a><span data-ttu-id="fd2f7-104">Atributos de sincronización</span><span class="sxs-lookup"><span data-stu-id="fd2f7-104">Sync Attributes</span></span>

<span data-ttu-id="fd2f7-105">Los atributos **Sync01** a **Sync16** son representaciones de cadena de valores de 32 bits que Windows Media Player usa al sincronizar listas de reproducción con uno de hasta 16 dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="fd2f7-105">The **Sync01** through **Sync16** attributes are string representations of 32-bit values that Windows Media Player uses when it synchronizes playlists with one of up to 16 portable devices.</span></span>

## <a name="applies-to"></a><span data-ttu-id="fd2f7-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="fd2f7-106">Applies To</span></span>

-   [<span data-ttu-id="fd2f7-107">Reproducción</span><span class="sxs-lookup"><span data-stu-id="fd2f7-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="fd2f7-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd2f7-108">Remarks</span></span>

<span data-ttu-id="fd2f7-109">Son atributos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="fd2f7-109">These are read/write attributes.</span></span> <span data-ttu-id="fd2f7-110">Un valor de cero indica que Windows Media Player no debe sincronizar la lista de reproducción con el dispositivo asociado.</span><span class="sxs-lookup"><span data-stu-id="fd2f7-110">A value of zero indicates that Windows Media Player should not synchronize the playlist with the associated device.</span></span> <span data-ttu-id="fd2f7-111">Un valor mayor que cero indica una prioridad de sincronización para la lista de reproducción determinada.</span><span class="sxs-lookup"><span data-stu-id="fd2f7-111">A value greater than zero indicates a synchronization priority for the given playlist.</span></span>

<span data-ttu-id="fd2f7-112">En función de la entrada del usuario, Windows Media Player establece este atributo para cada una de las listas de reproducción de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="fd2f7-112">Based on user input, Windows Media Player sets this attribute for each of the playlists in the library.</span></span> <span data-ttu-id="fd2f7-113">Cuando Windows Media Player intenta sincronizar una lista de reproducción con un dispositivo portátil, examina cada lista de reproducción para comparar los valores de los atributos de **Sync**_XX_ que representan la Asociación de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="fd2f7-113">When Windows Media Player attempts to synchronize a playlist with a portable device, it examines each playlist to compare the values for the **Sync**_XX_ attributes that represent the device partnership.</span></span> <span data-ttu-id="fd2f7-114">Las listas de reproducción con valores inferiores de la **sincronización**_XX_ reciben mayor prioridad de sincronización.</span><span class="sxs-lookup"><span data-stu-id="fd2f7-114">Playlists that have lower **Sync**_XX_ values receive higher synchronization priority.</span></span>

<span data-ttu-id="fd2f7-115">Por ejemplo, la biblioteca puede contener las cuatro listas de reproducción siguientes y los valores de la **sincronización**_XX_ correspondientes:</span><span class="sxs-lookup"><span data-stu-id="fd2f7-115">For example, the library might contain the following four playlists and respective **Sync**_XX_ values:</span></span>



| <span data-ttu-id="fd2f7-116">Nombre de lista de reproducción</span><span class="sxs-lookup"><span data-stu-id="fd2f7-116">Playlist Name</span></span> | <span data-ttu-id="fd2f7-117">Valor Sync01</span><span class="sxs-lookup"><span data-stu-id="fd2f7-117">Sync01 Value</span></span> |
|---------------|--------------|
| <span data-ttu-id="fd2f7-118">GymMusic. WPL</span><span class="sxs-lookup"><span data-stu-id="fd2f7-118">GymMusic.WPL</span></span>  | <span data-ttu-id="fd2f7-119">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="fd2f7-119">0x0000000D</span></span>   |
| <span data-ttu-id="fd2f7-120">Relajarse. WPL</span><span class="sxs-lookup"><span data-stu-id="fd2f7-120">Relax.WPL</span></span>     | <span data-ttu-id="fd2f7-121">0x00000020</span><span class="sxs-lookup"><span data-stu-id="fd2f7-121">0x00000020</span></span>   |
| <span data-ttu-id="fd2f7-122">DriveHome. WPL</span><span class="sxs-lookup"><span data-stu-id="fd2f7-122">DriveHome.WPL</span></span> | <span data-ttu-id="fd2f7-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fd2f7-123">0x00000001</span></span>   |
| <span data-ttu-id="fd2f7-124">NoGo. WPL</span><span class="sxs-lookup"><span data-stu-id="fd2f7-124">NoGo.WPL</span></span>      | <span data-ttu-id="fd2f7-125">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fd2f7-125">0x00000000</span></span>   |



 

<span data-ttu-id="fd2f7-126">Cuando Windows Media Player sincroniza el dispositivo asociado con el atributo, sincronizará las listas de reproducción en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="fd2f7-126">When Windows Media Player synchronizes the device associated with the attribute, it will synchronize the playlists in the following order:</span></span>

1.  <span data-ttu-id="fd2f7-127">DriveHome. WPL</span><span class="sxs-lookup"><span data-stu-id="fd2f7-127">DriveHome.WPL</span></span>
2.  <span data-ttu-id="fd2f7-128">GymMusic. WPL</span><span class="sxs-lookup"><span data-stu-id="fd2f7-128">GymMusic.WPL</span></span>
3.  <span data-ttu-id="fd2f7-129">Relajarse. WPL</span><span class="sxs-lookup"><span data-stu-id="fd2f7-129">Relax.WPL</span></span>

<span data-ttu-id="fd2f7-130">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="fd2f7-130">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd2f7-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd2f7-131">Requirements</span></span>



| <span data-ttu-id="fd2f7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd2f7-132">Requirement</span></span> | <span data-ttu-id="fd2f7-133">Value</span><span class="sxs-lookup"><span data-stu-id="fd2f7-133">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="fd2f7-134">Versión</span><span class="sxs-lookup"><span data-stu-id="fd2f7-134">Version</span></span><br/> | <span data-ttu-id="fd2f7-135">Windows Media Player 10 o posterior</span><span class="sxs-lookup"><span data-stu-id="fd2f7-135">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd2f7-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd2f7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd2f7-137">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="fd2f7-137">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="fd2f7-138">**Enumerar listas de reproducción de sincronización**</span><span class="sxs-lookup"><span data-stu-id="fd2f7-138">**Enumerating Synchronization Playlists**</span></span>](enumerating-synchronization-playlists.md)
</dt> </dl>

 

 





