---
title: Enumeración TransportStatus
description: Define el estado de transporte disponible tal y como se define en las directrices de UPnP.
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
keywords:
- Enumeración de TransportStatus de media streaming API
topic_type:
- apiref
api_name:
- TransportStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4a9de34f358db96b468dbd3329483a8e09b6b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718981"
---
# <a name="transportstatus-enumeration"></a><span data-ttu-id="f86a3-104">Enumeración TransportStatus</span><span class="sxs-lookup"><span data-stu-id="f86a3-104">TransportStatus enumeration</span></span>

<span data-ttu-id="f86a3-105">Define el estado de transporte disponible tal y como se define en las directrices de UPnP.</span><span class="sxs-lookup"><span data-stu-id="f86a3-105">Defines the available transport status as defined by the UPnP Guidelines.</span></span>

## <a name="syntax"></a><span data-ttu-id="f86a3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f86a3-106">Syntax</span></span>


```C++
typedef enum TransportStatus { 
  Unknown        = 0,
  Ok             = 1,
  ErrorOccurred  = 2,
  Last           = 3
} TransportStatus;
```



## <a name="constants"></a><span data-ttu-id="f86a3-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="f86a3-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f86a3-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span><span class="sxs-lookup"><span data-stu-id="f86a3-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="f86a3-109">Estado de dispositivo erróneo.</span><span class="sxs-lookup"><span data-stu-id="f86a3-109">Erroneous device status.</span></span>

</dd> <dt>

<span data-ttu-id="f86a3-110"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Vale**</span><span class="sxs-lookup"><span data-stu-id="f86a3-110"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Ok**</span></span>
</dt> <dd>

<span data-ttu-id="f86a3-111">El dispositivo está en buen estado.</span><span class="sxs-lookup"><span data-stu-id="f86a3-111">The device is in a good status.</span></span>

</dd> <dt>

<span data-ttu-id="f86a3-112"><span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ErrorOccurred**</span><span class="sxs-lookup"><span data-stu-id="f86a3-112"><span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ErrorOccurred**</span></span>
</dt> <dd>

<span data-ttu-id="f86a3-113">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f86a3-113">An error occurred on the device.</span></span>

</dd> <dt>

<span data-ttu-id="f86a3-114"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Guardado**</span><span class="sxs-lookup"><span data-stu-id="f86a3-114"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Last**</span></span>
</dt> <dd>

<span data-ttu-id="f86a3-115">El estado anterior del dispositivo es el estado de transporte actual.</span><span class="sxs-lookup"><span data-stu-id="f86a3-115">The device s previous status to the current transport status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f86a3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f86a3-116">Requirements</span></span>



| <span data-ttu-id="f86a3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f86a3-117">Requirement</span></span> | <span data-ttu-id="f86a3-118">Value</span><span class="sxs-lookup"><span data-stu-id="f86a3-118">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f86a3-119">IDL</span><span class="sxs-lookup"><span data-stu-id="f86a3-119">IDL</span></span><br/> | <dl> <span data-ttu-id="f86a3-120"><dt>Windows. Media. streaming. idl (referencia a Windows. Media. streaming. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="f86a3-120"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





