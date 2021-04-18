---
title: Enumeración ControlReconnectStatus
description: Especifica el resultado del método de reconexión IMsRdpClient8.
ms.assetid: FB0AC4CF-18F5-4CDD-A75C-59A7CF716688
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto enumeración ControlReconnectStatus
topic_type:
- apiref
api_name:
- ControlReconnectStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5638cbdda268dd453881ee1d88085728479aada6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676613"
---
# <a name="controlreconnectstatus-enumeration"></a><span data-ttu-id="017b3-104">Enumeración ControlReconnectStatus</span><span class="sxs-lookup"><span data-stu-id="017b3-104">ControlReconnectStatus enumeration</span></span>

<span data-ttu-id="017b3-105">Especifica el resultado del método [**IMsRdpClient8:: reconnect**](imsrdpclient8-reconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="017b3-105">Specifies the result of the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="017b3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="017b3-106">Syntax</span></span>


```C++
typedef enum  { 
  controlReconnectStarted  = 0x0000,
  controlReconnectBlocked  = 0x0001
} ControlReconnectStatus;
```



## <a name="constants"></a><span data-ttu-id="017b3-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="017b3-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="017b3-108"><span id="controlReconnectStarted"></span><span id="controlreconnectstarted"></span><span id="CONTROLRECONNECTSTARTED"></span>**controlReconnectStarted**</span><span class="sxs-lookup"><span data-stu-id="017b3-108"><span id="controlReconnectStarted"></span><span id="controlreconnectstarted"></span><span id="CONTROLRECONNECTSTARTED"></span>**controlReconnectStarted**</span></span>
</dt> <dd>

<span data-ttu-id="017b3-109">Se inició la operación de reconexión.</span><span class="sxs-lookup"><span data-stu-id="017b3-109">The reconnect operation was started.</span></span>

</dd> <dt>

<span data-ttu-id="017b3-110"><span id="controlReconnectBlocked"></span><span id="controlreconnectblocked"></span><span id="CONTROLRECONNECTBLOCKED"></span>**controlReconnectBlocked**</span><span class="sxs-lookup"><span data-stu-id="017b3-110"><span id="controlReconnectBlocked"></span><span id="controlreconnectblocked"></span><span id="CONTROLRECONNECTBLOCKED"></span>**controlReconnectBlocked**</span></span>
</dt> <dd>

<span data-ttu-id="017b3-111">No se pudo iniciar la operación de reconexión.</span><span class="sxs-lookup"><span data-stu-id="017b3-111">The reconnect operation could not be started.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="017b3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="017b3-112">Requirements</span></span>



| <span data-ttu-id="017b3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="017b3-113">Requirement</span></span> | <span data-ttu-id="017b3-114">Value</span><span class="sxs-lookup"><span data-stu-id="017b3-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="017b3-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="017b3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="017b3-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="017b3-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="017b3-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="017b3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="017b3-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="017b3-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="017b3-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="017b3-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="017b3-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="017b3-120"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="017b3-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="017b3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="017b3-122">**IMsRdpClient8:: reconnect**</span><span class="sxs-lookup"><span data-stu-id="017b3-122">**IMsRdpClient8::Reconnect**</span></span>](imsrdpclient8-reconnect.md)
</dt> </dl>

 

 





