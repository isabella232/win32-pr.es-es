---
description: La \_ propiedad FriendlyName del dispositivo PKEY \_ contiene el nombre descriptivo del dispositivo de extremo (por ejemplo, &\# 0034; Altavoces (adaptador de audio XYZ) &\# 0034;).
ms.assetid: 3ccd6a78-8bc3-4a46-8f11-7c2ae8a23c63
title: PKEY_Device_FriendlyName (Functiondiscoverykeys \_ devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fab8b8f30e04ae66356fb0910e3767d74b7b697a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906934"
---
# <a name="pkey_device_friendlyname"></a><span data-ttu-id="ed73f-103">PKEY el \_ dispositivo \_ FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ed73f-103">PKEY\_Device\_FriendlyName</span></span>

<span data-ttu-id="ed73f-104">La **propiedad \_ \_ FriendlyName del dispositivo PKEY** contiene el nombre descriptivo del dispositivo del punto de conexión (por ejemplo, "altavoces (adaptador de audio XYZ)").</span><span class="sxs-lookup"><span data-stu-id="ed73f-104">The **PKEY\_Device\_FriendlyName** property contains the friendly name of the endpoint device (for example, "Speakers (XYZ Audio Adapter)").</span></span>

<span data-ttu-id="ed73f-105">El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ LPWStr.</span><span class="sxs-lookup"><span data-stu-id="ed73f-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="ed73f-106">El miembro **pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en null que contiene el nombre descriptivo del dispositivo de extremo.</span><span class="sxs-lookup"><span data-stu-id="ed73f-106">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains the friendly name of the endpoint device.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed73f-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed73f-107">Requirements</span></span>



| <span data-ttu-id="ed73f-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed73f-108">Requirement</span></span> | <span data-ttu-id="ed73f-109">Value</span><span class="sxs-lookup"><span data-stu-id="ed73f-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed73f-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed73f-110">Minimum supported client</span></span><br/> | <span data-ttu-id="ed73f-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ed73f-111">Windows Vista \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ed73f-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed73f-112">Minimum supported server</span></span><br/> | <span data-ttu-id="ed73f-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed73f-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="ed73f-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed73f-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed73f-115"><dt>Functiondiscoverykeys \_ devpkey. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed73f-115"><dt>Functiondiscoverykeys\_devpkey.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed73f-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed73f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed73f-117">Propiedades de audio principales</span><span class="sxs-lookup"><span data-stu-id="ed73f-117">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="ed73f-118">Propiedades de dispositivos</span><span class="sxs-lookup"><span data-stu-id="ed73f-118">Device Properties</span></span>](device-properties.md)
</dt> </dl>

 

 




