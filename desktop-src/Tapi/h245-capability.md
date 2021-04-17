---
description: La \_ enumeración de la funcionalidad H245 describe la compatibilidad con el formato de audio y vídeo.
ms.assetid: 76aeb3a1-3233-4425-b9db-efacbedc309e
title: Enumeración H245_CAPABILITY (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7a6f81f87480f221f87680d9cf086120deb2de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690954"
---
# <a name="h245_capability-enumeration"></a><span data-ttu-id="b4246-103">\_Enumeración de la funcionalidad H245</span><span class="sxs-lookup"><span data-stu-id="b4246-103">H245\_CAPABILITY enumeration</span></span>

<span data-ttu-id="b4246-104">\[**H245 \_ La funcionalidad** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b4246-104">\[**H245\_CAPABILITY** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b4246-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="b4246-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b4246-106">La enumeración de la **\_ funcionalidad H245** describe la compatibilidad con el formato de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="b4246-106">The **H245\_CAPABILITY** enum describes audio and video format support.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4246-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4246-107">Syntax</span></span>


```C++
} H245_CAPABILITY;
```



## <a name="constants"></a><span data-ttu-id="b4246-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="b4246-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b4246-109"><span id="HC_G711"></span><span id="hc_g711"></span>**HC \_ G711**</span><span class="sxs-lookup"><span data-stu-id="b4246-109"><span id="HC_G711"></span><span id="hc_g711"></span>**HC\_G711**</span></span>
</dt> <dd>

<span data-ttu-id="b4246-110">Se admite el protocolo de audio G. 711.</span><span class="sxs-lookup"><span data-stu-id="b4246-110">The G.711 audio protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="b4246-111"><span id="HC_G723"></span><span id="hc_g723"></span>**HC \_ G723**</span><span class="sxs-lookup"><span data-stu-id="b4246-111"><span id="HC_G723"></span><span id="hc_g723"></span>**HC\_G723**</span></span>
</dt> <dd>

<span data-ttu-id="b4246-112">Se admite el protocolo de audio G. 723.</span><span class="sxs-lookup"><span data-stu-id="b4246-112">The G.723 audio protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="b4246-113"><span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**HC \_ H263QCIF**</span><span class="sxs-lookup"><span data-stu-id="b4246-113"><span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**HC\_H263QCIF**</span></span>
</dt> <dd>

<span data-ttu-id="b4246-114">Se admite el protocolo de vídeo H. 263.</span><span class="sxs-lookup"><span data-stu-id="b4246-114">The H.263 video protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="b4246-115"><span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**HC \_ H261QCIF**</span><span class="sxs-lookup"><span data-stu-id="b4246-115"><span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**HC\_H261QCIF**</span></span>
</dt> <dd>

<span data-ttu-id="b4246-116">Se admite el protocolo de vídeo H. 263.</span><span class="sxs-lookup"><span data-stu-id="b4246-116">The H.263 video protocol is supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4246-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4246-117">Requirements</span></span>



| <span data-ttu-id="b4246-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4246-118">Requirement</span></span> | <span data-ttu-id="b4246-119">Value</span><span class="sxs-lookup"><span data-stu-id="b4246-119">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4246-120">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="b4246-120">TAPI version</span></span><br/> | <span data-ttu-id="b4246-121">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="b4246-121">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b4246-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4246-122">Header</span></span><br/>       | <dl> <span data-ttu-id="b4246-123"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4246-123"><dt>H323priv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4246-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4246-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4246-125">**IH323LineEx::SetDefaultCapabilityPreferrence**</span><span class="sxs-lookup"><span data-stu-id="b4246-125">**IH323LineEx::SetDefaultCapabilityPreferrence**</span></span>](ih323lineex-setdefaultcapabilitypreferrence.md)
</dt> </dl>

 

 




