---
title: Enumeración DeviceTypes
description: Describe los tipos de dispositivo DLNA que admite la API de streaming de multimedia.
ms.assetid: ec6bbc1f-653a-414c-b458-1a5e1b101781
keywords:
- Enumeración de DeviceTypes de media streaming API
topic_type:
- apiref
api_name:
- DeviceTypes
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9caf60fa5736f9db442da5787746a49f71c61c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718599"
---
# <a name="devicetypes-enumeration"></a><span data-ttu-id="4d5a3-104">Enumeración DeviceTypes</span><span class="sxs-lookup"><span data-stu-id="4d5a3-104">DeviceTypes enumeration</span></span>

<span data-ttu-id="4d5a3-105">Describe los tipos de dispositivo DLNA que admite la API de streaming de multimedia.</span><span class="sxs-lookup"><span data-stu-id="4d5a3-105">Describes the DLNA device types that are supported by the Media Streaming API.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d5a3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d5a3-106">Syntax</span></span>


```C++
typedef enum DeviceTypes { 
  Unknown               = 0x0,
  DigitalMediaRenderer  = 0x1,
  DigitalMediaServer    = 0x2,
  DigitalMediaPlayer    = 0x4
} DeviceTypes;
```



## <a name="constants"></a><span data-ttu-id="4d5a3-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="4d5a3-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4d5a3-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span><span class="sxs-lookup"><span data-stu-id="4d5a3-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="4d5a3-109">Tipo de dispositivo desconocido.</span><span class="sxs-lookup"><span data-stu-id="4d5a3-109">Unknown device type.</span></span>

</dd> <dt>

<span data-ttu-id="4d5a3-110"><span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**DigitalMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="4d5a3-110"><span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**DigitalMediaRenderer**</span></span>
</dt> <dd>

<span data-ttu-id="4d5a3-111">Representador de medios digitales DLNA (DMR).</span><span class="sxs-lookup"><span data-stu-id="4d5a3-111">DLNA Digital Media Renderer (DMR).</span></span> <span data-ttu-id="4d5a3-112">El valor es equivalente al tipo de dispositivo **urn: schemas-UPnP-org: Device: MediaRenderer: 1**.</span><span class="sxs-lookup"><span data-stu-id="4d5a3-112">The value is equivalent to the device type **urn:schemas-upnp-org:device:MediaRenderer:1**.</span></span>

</dd> <dt>

<span data-ttu-id="4d5a3-113"><span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**DigitalMediaServer**</span><span class="sxs-lookup"><span data-stu-id="4d5a3-113"><span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**DigitalMediaServer**</span></span>
</dt> <dd>

<span data-ttu-id="4d5a3-114">Servidor de medios digitales DLNA (DMS).</span><span class="sxs-lookup"><span data-stu-id="4d5a3-114">DLNA Digital Media Server (DMS).</span></span> <span data-ttu-id="4d5a3-115">El valor es equivalente al tipo de dispositivo **urn: schemas-UPnP-org: Device: MediaServer: 1**.</span><span class="sxs-lookup"><span data-stu-id="4d5a3-115">The value is equivalent to the device type **urn:schemas-upnp-org:device:MediaServer:1**.</span></span>

</dd> <dt>

<span data-ttu-id="4d5a3-116"><span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**DigitalMediaPlayer**</span><span class="sxs-lookup"><span data-stu-id="4d5a3-116"><span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**DigitalMediaPlayer**</span></span>
</dt> <dd>

<span data-ttu-id="4d5a3-117">Media Player digitales DLNA</span><span class="sxs-lookup"><span data-stu-id="4d5a3-117">DLNA Digital Media Player</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d5a3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d5a3-118">Requirements</span></span>



| <span data-ttu-id="4d5a3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d5a3-119">Requirement</span></span> | <span data-ttu-id="4d5a3-120">Value</span><span class="sxs-lookup"><span data-stu-id="4d5a3-120">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d5a3-121">IDL</span><span class="sxs-lookup"><span data-stu-id="4d5a3-121">IDL</span></span><br/> | <dl> <span data-ttu-id="4d5a3-122"><dt>Windows. Media. streaming. idl (referencia a Windows. Media. streaming. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="4d5a3-122"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





