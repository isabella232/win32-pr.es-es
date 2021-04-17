---
title: Atributo SyncState
description: El atributo SyncState es una representación de cadena de un valor de 32 bits que usa Windows Media Player cuando sincroniza listas de reproducción con dispositivos portátiles.
ms.assetid: affc3d1c-7fe6-4811-acfc-57285cb181ca
keywords:
- SyncState Media Player de Windows
topic_type:
- apiref
api_name:
- SyncState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a948f6c649d548b375ccb676134177b0273c85c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718680"
---
# <a name="syncstate-attribute"></a><span data-ttu-id="4a574-104">Atributo SyncState</span><span class="sxs-lookup"><span data-stu-id="4a574-104">SyncState Attribute</span></span>

<span data-ttu-id="4a574-105">El atributo **SyncState** es una representación de cadena de un valor de 32 bits que usa Windows Media Player cuando sincroniza listas de reproducción con dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="4a574-105">The **SyncState** attribute is a string representation of a 32-bit value that Windows Media Player uses when it synchronizes playlists with portable devices.</span></span>

## <a name="applies-to"></a><span data-ttu-id="4a574-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="4a574-106">Applies To</span></span>

-   [<span data-ttu-id="4a574-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="4a574-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="4a574-108">Otros elementos</span><span class="sxs-lookup"><span data-stu-id="4a574-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="4a574-109">Elementos de fotografía</span><span class="sxs-lookup"><span data-stu-id="4a574-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="4a574-110">Elementos de vídeo</span><span class="sxs-lookup"><span data-stu-id="4a574-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="4a574-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a574-111">Remarks</span></span>

<span data-ttu-id="4a574-112">Este atributo consta de valores de 16 2 bits, cada uno de los cuales especifica el estado de sincronización de un dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="4a574-112">This attribute consists of sixteen 2-bit values, each of which specifies the synchronization state of a portable device.</span></span> <span data-ttu-id="4a574-113">El bit más significativo (MSB) de este valor de 32 bits corresponde al dispositivo 16.</span><span class="sxs-lookup"><span data-stu-id="4a574-113">The most significant bit (MSB) of this 32-bit value corresponds to device 16.</span></span> <span data-ttu-id="4a574-114">El bit menos significativo (LSB) corresponde al dispositivo 1.</span><span class="sxs-lookup"><span data-stu-id="4a574-114">The least significant bit (LSB) corresponds to device 1.</span></span>

<span data-ttu-id="4a574-115">El MSB de cada valor de 2 bits indica si Windows Media Player sincronizar el contenido con el dispositivo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="4a574-115">The MSB of each 2-bit value indicates whether Windows Media Player synchronized the content with the corresponding device.</span></span> <span data-ttu-id="4a574-116">Un valor de 1 indica que lo hizo.</span><span class="sxs-lookup"><span data-stu-id="4a574-116">A value of 1 indicates that it did.</span></span> <span data-ttu-id="4a574-117">Un valor de 0 indica que no lo hizo.</span><span class="sxs-lookup"><span data-stu-id="4a574-117">A value of 0 indicates that it did not.</span></span>

<span data-ttu-id="4a574-118">Si el MSB es 0, LSB especifica por qué se produjo un error en la sincronización.</span><span class="sxs-lookup"><span data-stu-id="4a574-118">If the MSB is 0, the LSB specifies why the synchronization failed.</span></span> <span data-ttu-id="4a574-119">Un valor de 1 en LSB indica que no hay suficiente espacio libre para el contenido.</span><span class="sxs-lookup"><span data-stu-id="4a574-119">A value of 1 in the LSB indicates that there was not enough free space for the content.</span></span> <span data-ttu-id="4a574-120">Un valor de 0 en LSB indica algún otro motivo que impidió la sincronización.</span><span class="sxs-lookup"><span data-stu-id="4a574-120">A value of 0 in the LSB indicates some other reason prevented synchronization.</span></span>

<span data-ttu-id="4a574-121">Para recuperar el estado de sincronización de un dispositivo determinado, debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4a574-121">To retrieve the synchronization state of a given device, you should do the following:</span></span>

1.  <span data-ttu-id="4a574-122">Invocar **IWMPSyncDevice:: get \_ status** para determinar si un dispositivo determinado está sincronizado.</span><span class="sxs-lookup"><span data-stu-id="4a574-122">Invoke **IWMPSyncDevice::get\_status** to determine whether a given device is synchronized.</span></span>
2.  <span data-ttu-id="4a574-123">Si está sincronizado, invoque **IWMPSyncDevice:: get \_ partnershipIndex** para recuperar el índice del par de bits del dispositivo en el atributo **SyncState** .</span><span class="sxs-lookup"><span data-stu-id="4a574-123">If it is synchronized, invoke **IWMPSyncDevice::get\_partnershipIndex** to retrieve the index of the device's bit pair in the **SyncState** attribute.</span></span>
3.  <span data-ttu-id="4a574-124">Con este índice, debe enmascarar el par de bits correspondiente del atributo **SyncState** y examinar el resultado para determinar el estado de sincronización de la lista de reproducción con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4a574-124">Using this index, mask the corresponding bit pair of the **SyncState** attribute and examine the result to determine the synchronization state of the playlist with the device.</span></span>

<span data-ttu-id="4a574-125">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="4a574-125">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a574-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a574-126">Requirements</span></span>



| <span data-ttu-id="4a574-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a574-127">Requirement</span></span> | <span data-ttu-id="4a574-128">Value</span><span class="sxs-lookup"><span data-stu-id="4a574-128">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="4a574-129">Versión</span><span class="sxs-lookup"><span data-stu-id="4a574-129">Version</span></span><br/> | <span data-ttu-id="4a574-130">Windows Media Player 10 o posterior</span><span class="sxs-lookup"><span data-stu-id="4a574-130">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4a574-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a574-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a574-132">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="4a574-132">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="4a574-133">**Determinar el estado de sincronización de la lista de reproducción**</span><span class="sxs-lookup"><span data-stu-id="4a574-133">**Determining Playlist Synchronization State**</span></span>](determining-playlist-synchronization-state.md)
</dt> <dt>

[<span data-ttu-id="4a574-134">**IWMPSyncDevice:: get \_ partnershipIndex**</span><span class="sxs-lookup"><span data-stu-id="4a574-134">**IWMPSyncDevice::get\_partnershipIndex**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)
</dt> <dt>

[<span data-ttu-id="4a574-135">**IWMPSyncDevice:: get \_ status**</span><span class="sxs-lookup"><span data-stu-id="4a574-135">**IWMPSyncDevice::get\_status**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status)
</dt> </dl>

 

 





