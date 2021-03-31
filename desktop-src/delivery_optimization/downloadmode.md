---
title: Enumeración DownloadMode (Deliveryoptimization. h)
description: Define los diferentes modos de descarga que utiliza la optimización de entrega.
ms.assetid: 7E9407C6-A22F-459E-B316-5E7809F0067A
keywords:
- Omite Optimización de distribución y usa BITS en su lugar. Por ejemplo, selecciona este modo para que los clientes puedan usar BranchCache. enumeración
topic_type:
- apiref
api_name:
- DownloadMode
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0cde44a3d211040e2cc1dd62afd54f8284f5493e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079290"
---
# <a name="downloadmode-enumeration"></a><span data-ttu-id="231d5-106">Enumeración DownloadMode</span><span class="sxs-lookup"><span data-stu-id="231d5-106">DownloadMode enumeration</span></span>

<span data-ttu-id="231d5-107">Define los diferentes modos de descarga que utiliza la optimización de entrega.</span><span class="sxs-lookup"><span data-stu-id="231d5-107">Defines the different download modes that Delivery Optimization uses.</span></span>

## <a name="syntax"></a><span data-ttu-id="231d5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="231d5-108">Syntax</span></span>


```C++
typedef enum _DownloadMode { 
  DownloadMode_CdnOnly   = 0,
  DownloadMode_Lan       = 1,
  DownloadMode_Group     = 2,
  DownloadMode_Internet  = 3,
  DownloadMode_Simple    = 99,
  DownloadMode_Bypass    = 100
} DownloadMode;
```



## <a name="constants"></a><span data-ttu-id="231d5-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="231d5-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="231d5-110"><span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**</span><span class="sxs-lookup"><span data-stu-id="231d5-110"><span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**</span></span>
</dt> <dd>

<span data-ttu-id="231d5-111">Esta configuración deshabilita el almacenamiento en caché del mismo nivel, pero permite que la optimización de entrega Descargue contenido de servidores de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="231d5-111">This setting disables peer-to-peer caching but still allows Delivery Optimization to download content from Microsoft servers.</span></span> <span data-ttu-id="231d5-112">Este modo utiliza metadatos adicionales proporcionados por los servicios en la nube de optimización de entrega para una experiencia de descarga eficaz y confiable.</span><span class="sxs-lookup"><span data-stu-id="231d5-112">This mode uses additional metadata provided by the Delivery Optimization cloud services for a peerless reliable and efficient download experience.</span></span>

</dd> <dt>

<span data-ttu-id="231d5-113"><span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**</span><span class="sxs-lookup"><span data-stu-id="231d5-113"><span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**</span></span>
</dt> <dd>

<span data-ttu-id="231d5-114">Este modo de funcionamiento predeterminado de Optimización de distribución permite el uso compartido del mismo nivel en la misma red.</span><span class="sxs-lookup"><span data-stu-id="231d5-114">This default operating mode for Delivery Optimization enables peer sharing on the same network.</span></span>

</dd> <dt>

<span data-ttu-id="231d5-115"><span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**</span><span class="sxs-lookup"><span data-stu-id="231d5-115"><span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**</span></span>
</dt> <dd>

<span data-ttu-id="231d5-116">Cuando se establece el modo de grupo, el grupo se selecciona automáticamente según el sitio de Active Directory Domain Services de dispositivos (AD DS) (Windows 10, versión 1607) o el dominio al que se autentica el dispositivo (Windows 10, versión 1511).</span><span class="sxs-lookup"><span data-stu-id="231d5-116">When group mode is set, the group is automatically selected based on the device s Active Directory Domain Services (AD DS) site (Windows 10, version 1607) or the domain the device is authenticated to (Windows 10, version 1511).</span></span> <span data-ttu-id="231d5-117">En el modo de grupo, el emparejamiento se produce entre subredes internas, entre dispositivos que pertenecen al mismo grupo, incluidos los dispositivos de las oficinas remotas.</span><span class="sxs-lookup"><span data-stu-id="231d5-117">In group mode, peering occurs across internal subnets, between devices that belong to the same group, including devices in remote offices.</span></span> <span data-ttu-id="231d5-118">Puedes usar la opción GroupID para crear tu propio grupo personalizado independientemente de los dominios y sitios de AD DS.</span><span class="sxs-lookup"><span data-stu-id="231d5-118">You can use the GroupID option to create your own custom group independently of domains and AD DS sites.</span></span> <span data-ttu-id="231d5-119">El modo de descarga en grupo es la opción recomendada para la mayoría de las organizaciones que tratan de conseguir la máxima optimización del ancho de banda con la Optimización de distribución.</span><span class="sxs-lookup"><span data-stu-id="231d5-119">Group download mode is the recommended option for most organizations looking to achieve the best bandwidth optimization with Delivery Optimization.</span></span>

</dd> <dt>

<span data-ttu-id="231d5-120"><span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**</span><span class="sxs-lookup"><span data-stu-id="231d5-120"><span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**</span></span>
</dt> <dd>

<span data-ttu-id="231d5-121">Habilita orígenes del mismo nivel de Internet para Optimización de distribución.</span><span class="sxs-lookup"><span data-stu-id="231d5-121">Enable Internet peer sources for Delivery Optimization.</span></span>

</dd> <dt>

<span data-ttu-id="231d5-122"><span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**</span><span class="sxs-lookup"><span data-stu-id="231d5-122"><span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**</span></span>
</dt> <dd>

<span data-ttu-id="231d5-123">El modo simple deshabilita completamente el uso de los servicios en la nube de Optimización de distribución completo (para entornos sin conexión).</span><span class="sxs-lookup"><span data-stu-id="231d5-123">Simple mode disables the use of Delivery Optimization cloud services completely (for offline environments).</span></span> <span data-ttu-id="231d5-124">La optimización de entrega cambia a este modo automáticamente cuando los servicios en la nube de optimización de entrega no están disponibles, no se puede tener acceso a ellos o cuando el tamaño del archivo de contenido es inferior a 10 MB.</span><span class="sxs-lookup"><span data-stu-id="231d5-124">Delivery Optimization switches to this mode automatically when the Delivery Optimization cloud services are unavailable, unreachable or when the content file size is less than 10 MB.</span></span> <span data-ttu-id="231d5-125">En este modo, la optimización de entrega proporciona una experiencia de descarga confiable, sin almacenamiento en caché punto a punto.</span><span class="sxs-lookup"><span data-stu-id="231d5-125">In this mode, Delivery Optimization provides a reliable download experience, with no peer-to-peer caching.</span></span>

</dd> <dt>

<span data-ttu-id="231d5-126"><span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**</span><span class="sxs-lookup"><span data-stu-id="231d5-126"><span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**</span></span>
</dt> <dd>

<span data-ttu-id="231d5-127">Omite Optimización de distribución y usa BITS en su lugar.</span><span class="sxs-lookup"><span data-stu-id="231d5-127">Bypass Delivery Optimization and use BITS, instead.</span></span> <span data-ttu-id="231d5-128">Por ejemplo, selecciona este modo para que los clientes puedan usar BranchCache.</span><span class="sxs-lookup"><span data-stu-id="231d5-128">For example, select this mode so that clients can use BranchCache.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="231d5-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="231d5-129">Requirements</span></span>

| <span data-ttu-id="231d5-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="231d5-130">Requirement</span></span> | <span data-ttu-id="231d5-131">Value</span><span class="sxs-lookup"><span data-stu-id="231d5-131">Value</span></span> |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="231d5-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="231d5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="231d5-133">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="231d5-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="231d5-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="231d5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="231d5-135">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="231d5-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>  |
| <span data-ttu-id="231d5-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="231d5-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="231d5-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="231d5-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>               |
