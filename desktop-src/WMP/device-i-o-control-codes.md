---
title: Códigos de control de e/s de dispositivo
description: Códigos de control de e/s de dispositivo
ms.assetid: 46a5d166-ca8d-42df-9455-145332437153
keywords:
- Media Player de Windows, códigos de control de e/s de dispositivo
- Media Player de Windows, códigos de control
- Administrador de dispositivos de Windows Media
- códigos de control de e/s de dispositivo
- códigos de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c00e235ce0f0e68e98f4f0e37221eac0903682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695399"
---
# <a name="device-io-control-codes"></a><span data-ttu-id="23c4a-108">Códigos de control de e/s de dispositivo</span><span class="sxs-lookup"><span data-stu-id="23c4a-108">Device I/O Control Codes</span></span>

<span data-ttu-id="23c4a-109">Windows Media Player 10 o posterior define los códigos de control de e/s de dispositivo de Windows Media Administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="23c4a-109">Windows Media Player 10 or later defines Windows Media Device Manager device I/O control codes.</span></span> <span data-ttu-id="23c4a-110">La tabla siguiente contiene los códigos de control y sus descripciones.</span><span class="sxs-lookup"><span data-stu-id="23c4a-110">The following table contains the control codes and their descriptions.</span></span>



| <span data-ttu-id="23c4a-111">Código de control de e/s</span><span class="sxs-lookup"><span data-stu-id="23c4a-111">I/O control code</span></span>                      | <span data-ttu-id="23c4a-112">Value</span><span class="sxs-lookup"><span data-stu-id="23c4a-112">Value</span></span>      | <span data-ttu-id="23c4a-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="23c4a-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23c4a-114">**\_viaje de \_ ida y \_ vuelta de metadatos de ioctl WMP \_**</span><span class="sxs-lookup"><span data-stu-id="23c4a-114">**IOCTL\_WMP\_METADATA\_ROUND\_TRIP**</span></span> | <span data-ttu-id="23c4a-115">0x31504d57</span><span class="sxs-lookup"><span data-stu-id="23c4a-115">0x31504d57</span></span> | <span data-ttu-id="23c4a-116">Administra la transferencia de información sobre los cambios que se produjeron en los valores de metadatos.</span><span class="sxs-lookup"><span data-stu-id="23c4a-116">Manages transfer of information about changes that occurred to metadata values.</span></span> <span data-ttu-id="23c4a-117">Consulte [extensiones de dispositivo para la transferencia de metadatos acelerada](device-extensions-for-accelerated-metadata-transfer.md).</span><span class="sxs-lookup"><span data-stu-id="23c4a-117">See [Device Extensions for Accelerated Metadata Transfer](device-extensions-for-accelerated-metadata-transfer.md).</span></span>                                                                                                                                                                          |
| <span data-ttu-id="23c4a-118">**se \_ \_ \_ puede \_ sincronizar el dispositivo WMP de ioctl**</span><span class="sxs-lookup"><span data-stu-id="23c4a-118">**IOCTL\_WMP\_DEVICE\_CAN\_SYNC**</span></span>     | <span data-ttu-id="23c4a-119">0x32504d57</span><span class="sxs-lookup"><span data-stu-id="23c4a-119">0x32504d57</span></span> | <span data-ttu-id="23c4a-120">Indica si un dispositivo portátil admite la sincronización automática.</span><span class="sxs-lookup"><span data-stu-id="23c4a-120">Indicates whether a portable device supports automatic synchronization.</span></span> <span data-ttu-id="23c4a-121">Windows Media Player 10 o posterior no proporciona ningún búfer de entrada. El búfer de salida debe devolver un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="23c4a-121">Windows Media Player 10 or later provides no input buffer.The output buffer must return a **DWORD** value.</span></span> <span data-ttu-id="23c4a-122">Un valor de 1 significa que el dispositivo admite la sincronización.</span><span class="sxs-lookup"><span data-stu-id="23c4a-122">A value of 1 means the device supports synchronization.</span></span> <span data-ttu-id="23c4a-123">Un valor de 0 significa que el dispositivo no admite la sincronización automática.</span><span class="sxs-lookup"><span data-stu-id="23c4a-123">A value of 0 means the device does not support automatic synchronization.</span></span><br/> <span data-ttu-id="23c4a-124">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="23c4a-124">See Remarks for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="23c4a-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23c4a-125">Remarks</span></span>

<span data-ttu-id="23c4a-126">Estos códigos de control se definen en wmpdevices. h.</span><span class="sxs-lookup"><span data-stu-id="23c4a-126">These control codes are defined in wmpdevices.h.</span></span>

<span data-ttu-id="23c4a-127">Si el dispositivo no es compatible con el dispositivo WMP de IOCTL que se **\_ \_ \_ puede \_ sincronizar**, Windows Media Player 10 o posterior supone que el dispositivo admite la sincronización automática.</span><span class="sxs-lookup"><span data-stu-id="23c4a-127">If the device does not support **IOCTL\_WMP\_DEVICE\_CAN\_SYNC**, Windows Media Player 10 or later assumes the device supports automatic synchronization.</span></span> <span data-ttu-id="23c4a-128">Tenga en cuenta que, aunque este valor puede impedir la sincronización automática, se usan criterios adicionales para determinar si el dispositivo admite la sincronización automática.</span><span class="sxs-lookup"><span data-stu-id="23c4a-128">Note that while this value can disallow automatic synchronization, there are additional criteria used to determine whether the device supports automatic synchronization.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23c4a-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="23c4a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23c4a-130">**Extensiones de dispositivo para la transferencia de metadatos acelerada**</span><span class="sxs-lookup"><span data-stu-id="23c4a-130">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> <dt>

[<span data-ttu-id="23c4a-131">**Reproductor de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="23c4a-131">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 





