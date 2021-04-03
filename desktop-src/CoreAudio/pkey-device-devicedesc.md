---
description: La \_ propiedad DeviceDesc del dispositivo PKEY \_ contiene la descripción del dispositivo de extremo (por ejemplo, &\# 0034; Habla&\# 0034;).
ms.assetid: 23715497-a74d-4dab-aade-c7779fe80aa6
title: PKEY_Device_DeviceDesc (Functiondiscoverykeys \_ devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb68f874979e660fec0cd563db9bcaceb7d5b74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906938"
---
# <a name="pkey_device_devicedesc"></a><span data-ttu-id="3730f-103">\_DeviceDesc de dispositivo PKEY \_</span><span class="sxs-lookup"><span data-stu-id="3730f-103">PKEY\_Device\_DeviceDesc</span></span>

<span data-ttu-id="3730f-104">La **propiedad \_ \_ DeviceDesc del dispositivo PKEY** contiene la descripción del dispositivo de extremo (por ejemplo, "altavoces").</span><span class="sxs-lookup"><span data-stu-id="3730f-104">The **PKEY\_Device\_DeviceDesc** property contains the device description of the endpoint device (for example, "Speakers").</span></span>

<span data-ttu-id="3730f-105">El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ LPWStr.</span><span class="sxs-lookup"><span data-stu-id="3730f-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="3730f-106">El miembro **pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en null que contiene la descripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3730f-106">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains the device description.</span></span>

## <a name="requirements"></a><span data-ttu-id="3730f-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3730f-107">Requirements</span></span>



| <span data-ttu-id="3730f-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="3730f-108">Requirement</span></span> | <span data-ttu-id="3730f-109">Value</span><span class="sxs-lookup"><span data-stu-id="3730f-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3730f-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3730f-110">Minimum supported client</span></span><br/> | <span data-ttu-id="3730f-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3730f-111">Windows Vista \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3730f-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3730f-112">Minimum supported server</span></span><br/> | <span data-ttu-id="3730f-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3730f-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="3730f-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3730f-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="3730f-115"><dt>Functiondiscoverykeys \_ devpkey. h</dt></span><span class="sxs-lookup"><span data-stu-id="3730f-115"><dt>Functiondiscoverykeys\_devpkey.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3730f-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="3730f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3730f-117">Propiedades de audio principales</span><span class="sxs-lookup"><span data-stu-id="3730f-117">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="3730f-118">Propiedades de dispositivos</span><span class="sxs-lookup"><span data-stu-id="3730f-118">Device Properties</span></span>](device-properties.md)
</dt> </dl>

 

 




