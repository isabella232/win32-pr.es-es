---
title: Extensiones de dispositivo de Windows Media Administrador de dispositivos para la transferencia de metadatos
description: Extensiones de dispositivo de Windows Media Administrador de dispositivos para la transferencia de metadatos
ms.assetid: c1d84225-b5b1-4f9e-8694-a229653e53de
keywords:
- Windows Media Player, extensiones de dispositivo
- Windows Media Player, extensiones
- Media Player de Windows, metadatos
- Windows Media Player, transferencia acelerada de metadatos
- Windows Media Player, transferencia acelerada de metadatos
- metadatos, extensiones de dispositivo
- metadatos, extensiones
- extensiones de dispositivo, transferencia de metadatos
- extensiones, transferencia de metadatos
- transferencia acelerada de metadatos
- metadatos, transferencia acelerada
- extensiones de dispositivo, transferencia acelerada de metadatos
- extensiones, transferencia de metadatos acelerada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d85ff7026e3395338fdf048c54b8ff7401c9ee7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486882"
---
# <a name="windows-media-device-manager-device-extensions-for-metadata-transfer"></a><span data-ttu-id="4f262-116">Extensiones de dispositivo de Windows Media Administrador de dispositivos para la transferencia de metadatos</span><span class="sxs-lookup"><span data-stu-id="4f262-116">Windows Media Device Manager Device Extensions for Metadata Transfer</span></span>

<span data-ttu-id="4f262-117">Para habilitar la transferencia de metadatos acelerada, los fabricantes de dispositivos que no admiten MTP deben hacer lo siguiente en el código fuente:</span><span class="sxs-lookup"><span data-stu-id="4f262-117">To enable accelerated metadata transfer, manufacturers of devices that do not support MTP must do the following in source code:</span></span>

-   <span data-ttu-id="4f262-118">Definir **la \_ \_ \_ compatibilidad con dispositivos de WMP WMDM**.</span><span class="sxs-lookup"><span data-stu-id="4f262-118">Define **WMP\_WMDM\_DEVICE\_SUPPORT**.</span></span>
-   <span data-ttu-id="4f262-119">Incluya wmpdevices. h, que se instala como parte del SDK de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4f262-119">Include wmpdevices.h, which is installed as part of the Windows Media Player SDK.</span></span>

<span data-ttu-id="4f262-120">Wmpdevices. h define las siguientes estructuras.</span><span class="sxs-lookup"><span data-stu-id="4f262-120">Wmpdevices.h defines the following structures.</span></span>



| <span data-ttu-id="4f262-121">Estructura</span><span class="sxs-lookup"><span data-stu-id="4f262-121">Structure</span></span>                                                                                 | <span data-ttu-id="4f262-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f262-122">Description</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f262-123">Ciclo de ida y \_ vuelta de metadatos de WMP WMDM \_ \_ \_ \_ PC2DEVICE</span><span class="sxs-lookup"><span data-stu-id="4f262-123">WMP\_WMDM\_METADATA\_ROUND\_TRIP\_PC2DEVICE</span></span>](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_pc2device) | <span data-ttu-id="4f262-124">Estructura utilizada por Windows Media Player para solicitar información de sincronización de metadatos acelerada de dispositivos portátiles que no son compatibles con MTP.</span><span class="sxs-lookup"><span data-stu-id="4f262-124">Structure used by Windows Media Player to request accelerated metadata synchronization information from portable devices that do not support MTP.</span></span> |
| [<span data-ttu-id="4f262-125">Ciclo de ida y \_ vuelta de metadatos de WMP WMDM \_ \_ \_ \_ DEVICE2PC</span><span class="sxs-lookup"><span data-stu-id="4f262-125">WMP\_WMDM\_METADATA\_ROUND\_TRIP\_DEVICE2PC</span></span>](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_device2pc) | <span data-ttu-id="4f262-126">Estructura utilizada por Windows Media Player para recibir información de sincronización de metadatos acelerada de dispositivos portátiles que no son compatibles con MTP.</span><span class="sxs-lookup"><span data-stu-id="4f262-126">Structure used by Windows Media Player to receive accelerated metadata synchronization information from portable devices that do not support MTP.</span></span> |



 

<span data-ttu-id="4f262-127">Para solicitar información del dispositivo sobre los metadatos que han cambiado, Windows Media Player 10 o posterior llama al método de Administrador de dispositivos de Windows Media **IWMDMDevice3::D eviceiocontrol**.</span><span class="sxs-lookup"><span data-stu-id="4f262-127">To request information from the device about metadata that has changed, Windows Media Player 10 or later calls the Windows Media Device Manager method **IWMDMDevice3::DeviceIoControl**.</span></span> <span data-ttu-id="4f262-128">Al realizar esta llamada, el reproductor sigue los pasos específicos, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="4f262-128">When making this call, the Player follows specific steps, as follows:</span></span>

-   <span data-ttu-id="4f262-129">El primer parámetro, *dwIoControlCode*, contiene la constante **ioctl \_ WMP \_ Metadata \_ Round \_ Trip**.</span><span class="sxs-lookup"><span data-stu-id="4f262-129">The first parameter, *dwIoControlCode*, contains the constant **IOCTL\_WMP\_METADATA\_ROUND\_TRIP**.</span></span> <span data-ttu-id="4f262-130">Esta constante se define en wmpdevices. h.</span><span class="sxs-lookup"><span data-stu-id="4f262-130">This constant is defined in wmpdevices.h.</span></span>
-   <span data-ttu-id="4f262-131">El segundo parámetro, *lpInBuffer*, apunta a una estructura de PC2DEVICE de ida y **\_ \_ \_ \_ \_ vuelta de metadatos de WMP WMDM** .</span><span class="sxs-lookup"><span data-stu-id="4f262-131">The second parameter, *lpInBuffer*, points to a **WMP\_WMDM\_METADATA\_ROUND\_TRIP\_PC2DEVICE** structure.</span></span>
-   <span data-ttu-id="4f262-132">El tercer parámetro, *nInBufferSize*, contiene el tamaño del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="4f262-132">The third parameter, *nInBufferSize*, contains the size of the input buffer.</span></span>
-   <span data-ttu-id="4f262-133">El cuarto parámetro, *lpOutBuffer*, apunta a una estructura de DEVICE2PC de ida y **\_ \_ \_ \_ \_ vuelta de metadatos de WMP WMDM** .</span><span class="sxs-lookup"><span data-stu-id="4f262-133">The fourth parameter, *lpOutBuffer*, points to a **WMP\_WMDM\_METADATA\_ROUND\_TRIP\_DEVICE2PC** structure.</span></span> <span data-ttu-id="4f262-134">El dispositivo debe rellenar esta estructura con información sobre los cambios.</span><span class="sxs-lookup"><span data-stu-id="4f262-134">The device must fill in this structure with information about changes.</span></span>
-   <span data-ttu-id="4f262-135">El quinto parámetro, *pnOutBufferSize*, recibe el tamaño del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="4f262-135">The fifth parameter, *pnOutBufferSize*, receives the size of the output buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f262-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4f262-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f262-137">**Extensiones de dispositivo para la transferencia de metadatos acelerada**</span><span class="sxs-lookup"><span data-stu-id="4f262-137">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




