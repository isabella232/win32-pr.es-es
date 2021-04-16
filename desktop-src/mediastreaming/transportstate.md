---
title: Enumeración TransportState
description: Define los Estados de transporte disponibles tal y como se define en las directrices de UPnP.
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
keywords:
- Enumeración de TransportState de media streaming API
topic_type:
- apiref
api_name:
- TransportState
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 865d7e0f6a96727915833bb402860cde661162f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718982"
---
# <a name="transportstate-enumeration"></a><span data-ttu-id="19bd0-104">Enumeración TransportState</span><span class="sxs-lookup"><span data-stu-id="19bd0-104">TransportState enumeration</span></span>

<span data-ttu-id="19bd0-105">Define los Estados de transporte disponibles tal y como se define en las directrices de UPnP.</span><span class="sxs-lookup"><span data-stu-id="19bd0-105">Defines the available transport states as defined by the UPnP Guidelines.</span></span>

## <a name="syntax"></a><span data-ttu-id="19bd0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19bd0-106">Syntax</span></span>


```C++
typedef enum _TransportState { 
  Unknown         = 0,
  Stopped         = 1,
  Playing         = 2,
  Transitioning   = 3,
  Paused          = 4,
  Recording       = 5,
  NoMediaPresent  = 6,
  Last            = 7
} TransportState;
```



## <a name="constants"></a><span data-ttu-id="19bd0-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="19bd0-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="19bd0-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span><span class="sxs-lookup"><span data-stu-id="19bd0-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="19bd0-109">Estado de dispositivo erróneo.</span><span class="sxs-lookup"><span data-stu-id="19bd0-109">Erroneous device state.</span></span>

</dd> <dt>

<span data-ttu-id="19bd0-110"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Ha**</span><span class="sxs-lookup"><span data-stu-id="19bd0-110"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped**</span></span>
</dt> <dd>

<span data-ttu-id="19bd0-111">El transporte del dispositivo s está detenido.</span><span class="sxs-lookup"><span data-stu-id="19bd0-111">The device s transport is in a stopped state.</span></span>

</dd> <dt>

<span data-ttu-id="19bd0-112"><span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Tarjetas**</span><span class="sxs-lookup"><span data-stu-id="19bd0-112"><span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Playing**</span></span>
</dt> <dd>

<span data-ttu-id="19bd0-113">El transporte del dispositivo s está en estado de reproducción.</span><span class="sxs-lookup"><span data-stu-id="19bd0-113">The device s transport is in a playing state.</span></span>

</dd> <dt>

<span data-ttu-id="19bd0-114"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición**</span><span class="sxs-lookup"><span data-stu-id="19bd0-114"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning**</span></span>
</dt> <dd>

<span data-ttu-id="19bd0-115">El transporte del dispositivo s está en un estado de transición que dará como resultado otro valor de estado.</span><span class="sxs-lookup"><span data-stu-id="19bd0-115">The device s transport is in a transitioning state which will result in another state value.</span></span>

</dd> <dt>

<span data-ttu-id="19bd0-116"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**En pausa**</span><span class="sxs-lookup"><span data-stu-id="19bd0-116"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused**</span></span>
</dt> <dd>

<span data-ttu-id="19bd0-117">El transporte del dispositivo s está en estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="19bd0-117">The device s transport is in a paused state.</span></span>

</dd> <dt>

<span data-ttu-id="19bd0-118"><span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Musicales**</span><span class="sxs-lookup"><span data-stu-id="19bd0-118"><span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Recording**</span></span>
</dt> <dd>

<span data-ttu-id="19bd0-119">El transporte del dispositivo s está en un estado de grabación.</span><span class="sxs-lookup"><span data-stu-id="19bd0-119">The device s transport is in a recording state.</span></span>

</dd> <dt>

<span data-ttu-id="19bd0-120"><span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**</span><span class="sxs-lookup"><span data-stu-id="19bd0-120"><span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**</span></span>
</dt> <dd>

<span data-ttu-id="19bd0-121">El transporte del dispositivo s no tiene un URI establecido para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="19bd0-121">The device s transport does not have an URI set for playback.</span></span>

</dd> <dt>

<span data-ttu-id="19bd0-122"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Guardado**</span><span class="sxs-lookup"><span data-stu-id="19bd0-122"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Last**</span></span>
</dt> <dd>

<span data-ttu-id="19bd0-123">El estado anterior del dispositivo es el estado de transporte actual.</span><span class="sxs-lookup"><span data-stu-id="19bd0-123">The device s previous state to the current transport state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19bd0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19bd0-124">Requirements</span></span>



| <span data-ttu-id="19bd0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="19bd0-125">Requirement</span></span> | <span data-ttu-id="19bd0-126">Value</span><span class="sxs-lookup"><span data-stu-id="19bd0-126">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19bd0-127">IDL</span><span class="sxs-lookup"><span data-stu-id="19bd0-127">IDL</span></span><br/> | <dl> <span data-ttu-id="19bd0-128"><dt>Windows. Media. streaming. idl (referencia a Windows. Media. streaming. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="19bd0-128"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





