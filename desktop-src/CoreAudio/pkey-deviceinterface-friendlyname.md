---
description: La \_ propiedad FriendlyName de PKEY DeviceInterface \_ .
ms.assetid: beef2153-489f-4ff5-a161-b4e2cd4ac1fa
title: PKEY_DeviceInterface_FriendlyName (Functiondiscoverykeys \_ devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7590e9254e336bf9dbfe0fdeb3349bf19c0b8c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152748"
---
# <a name="pkey_deviceinterface_friendlyname"></a><span data-ttu-id="663a6-103">PKEY \_ DeviceInterface \_ FriendlyName</span><span class="sxs-lookup"><span data-stu-id="663a6-103">PKEY\_DeviceInterface\_FriendlyName</span></span>

<span data-ttu-id="663a6-104">La **propiedad \_ \_ FriendlyName de PKEY de DeviceInterface** contiene el nombre descriptivo del adaptador de audio al que está conectado el dispositivo de extremo (por ejemplo, "adaptador de audio XYZ").</span><span class="sxs-lookup"><span data-stu-id="663a6-104">The **PKEY\_DeviceInterface\_FriendlyName** property contains the friendly name of the audio adapter to which the endpoint device is attached (for example, "XYZ Audio Adapter").</span></span>

<span data-ttu-id="663a6-105">El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ LPWStr.</span><span class="sxs-lookup"><span data-stu-id="663a6-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="663a6-106">El miembro **pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en null que contiene el nombre descriptivo.</span><span class="sxs-lookup"><span data-stu-id="663a6-106">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains the friendly name.</span></span>

## <a name="requirements"></a><span data-ttu-id="663a6-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="663a6-107">Requirements</span></span>



| <span data-ttu-id="663a6-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="663a6-108">Requirement</span></span> | <span data-ttu-id="663a6-109">Value</span><span class="sxs-lookup"><span data-stu-id="663a6-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="663a6-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="663a6-110">Minimum supported client</span></span><br/> | <span data-ttu-id="663a6-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="663a6-111">Windows Vista \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="663a6-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="663a6-112">Minimum supported server</span></span><br/> | <span data-ttu-id="663a6-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="663a6-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="663a6-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="663a6-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="663a6-115"><dt>Functiondiscoverykeys \_ devpkey. h</dt></span><span class="sxs-lookup"><span data-stu-id="663a6-115"><dt>Functiondiscoverykeys\_devpkey.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="663a6-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="663a6-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="663a6-117">Propiedades de audio principales</span><span class="sxs-lookup"><span data-stu-id="663a6-117">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="663a6-118">Propiedades de dispositivos</span><span class="sxs-lookup"><span data-stu-id="663a6-118">Device Properties</span></span>](device-properties.md)
</dt> </dl>

 

 




