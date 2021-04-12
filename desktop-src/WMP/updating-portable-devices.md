---
title: Actualización de dispositivos portátiles
description: Actualización de dispositivos portátiles
ms.assetid: 2827e71b-f5e9-4403-9763-043239c4a216
keywords:
- Windows Media Player tiendas en línea, actualizar dispositivos portátiles
- tiendas en línea, actualizar dispositivos portátiles
- tipo 1 almacenes en línea, actualizar dispositivos portátiles
- Windows Media Player tiendas en línea, dispositivos portátiles
- tiendas en línea, dispositivos portátiles
- tipo 1 tiendas en línea, dispositivos portátiles
- actualización de dispositivos portátiles
- dispositivos portátiles, actualizar
- dispositivos portátiles, tiendas Windows Media Player en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b29f5314f4eba1af43b3858304f02f8a7e0107df
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358670"
---
# <a name="updating-portable-devices"></a><span data-ttu-id="207a5-112">Actualización de dispositivos portátiles</span><span class="sxs-lookup"><span data-stu-id="207a5-112">Updating Portable Devices</span></span>

<span data-ttu-id="207a5-113">Windows Media Player permite a los usuarios sincronizar contenido multimedia digital con dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="207a5-113">Windows Media Player enables users to synchronize digital media content with portable devices.</span></span> <span data-ttu-id="207a5-114">Esto puede incluir el contenido de música adquirido o alquilado desde una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="207a5-114">This can include music content purchased or rented from an online store.</span></span> <span data-ttu-id="207a5-115">En algunas circunstancias, los proveedores de tiendas en línea pueden querer escribir código para trabajar en un dispositivo portátil conectado como parte de la administración del contenido proporcionado por el almacén.</span><span class="sxs-lookup"><span data-stu-id="207a5-115">Under some circumstances, online store providers might want to write code to work on a connected portable device as part of managing content provided by the store.</span></span> <span data-ttu-id="207a5-116">Para que el complemento de la tienda en línea tenga la oportunidad de trabajar con un dispositivo conectado, Windows Media Player llama a [IWMPContentPartner:: UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) y proporciona el nombre canónico del dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="207a5-116">To give the online store plug-in the opportunity to work with a connected device, Windows Media Player calls [IWMPContentPartner::UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) and provides the canonical name of the portable device.</span></span> <span data-ttu-id="207a5-117">Si el código del complemento determina que se debe realizar algún trabajo con el dispositivo conectado, debe devolver de inmediato los elementos \_ correctos de la llamada a **UpdateDevice** antes de continuar con el trabajo.</span><span class="sxs-lookup"><span data-stu-id="207a5-117">If the plug-in code determines that some work must be done with the connected device, it must immediately return S\_OK from the call to **UpdateDevice** before proceeding to do the work.</span></span> <span data-ttu-id="207a5-118">Si no hay ningún trabajo que hacer, el complemento debe devolver un código de error.</span><span class="sxs-lookup"><span data-stu-id="207a5-118">If there is no work to do, the plug-in should return an error code.</span></span>

<span data-ttu-id="207a5-119">Cuando el complemento ha terminado de usar el dispositivo, debe llamar a [IWMPContentPartnerCallback:: UpdateDeviceComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) para notificar a Windows Media Player que el dispositivo está disponible.</span><span class="sxs-lookup"><span data-stu-id="207a5-119">When the plug-in has finished using the device, it must call [IWMPContentPartnerCallback::UpdateDeviceComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) to notify Windows Media Player that the device is available.</span></span>

## <a name="related-topics"></a><span data-ttu-id="207a5-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="207a5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="207a5-121">**Guía de programación para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="207a5-121">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




