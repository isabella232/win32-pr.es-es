---
title: IMsTscAxEvents OnNetworkStatusChanged, método
description: Se llama cuando el estado de la red ha cambiado. | IMsTscAxEvents OnNetworkStatusChanged, método
ms.assetid: 177A410E-2449-4FC7-8DE5-21F83A6DD028
ms.tgt_platform: multiple
keywords:
- Método OnNetworkStatusChanged Servicios de Escritorio remoto
- Método OnNetworkStatusChanged Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnNetworkStatusChanged
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b9bdcd7774493fcc54e1390ad199a6a56a7c51
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678675"
---
# <a name="imstscaxeventsonnetworkstatuschanged-method"></a><span data-ttu-id="91405-107">IMsTscAxEvents:: OnNetworkStatusChanged (método)</span><span class="sxs-lookup"><span data-stu-id="91405-107">IMsTscAxEvents::OnNetworkStatusChanged method</span></span>

<span data-ttu-id="91405-108">Se llama cuando el estado de la red ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="91405-108">Called when the network status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="91405-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91405-109">Syntax</span></span>


```C++
void OnNetworkStatusChanged(
  [in] ULONG qualityLevel,
  [in] LONG  bandwidth,
  [in] LONG  rtt
);
```



## <a name="parameters"></a><span data-ttu-id="91405-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91405-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91405-111">*qualityLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91405-111">*qualityLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91405-112">Especifica la nueva velocidad de conexión.</span><span class="sxs-lookup"><span data-stu-id="91405-112">Specifies the new connection speed.</span></span> <span data-ttu-id="91405-113">Será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="91405-113">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="91405-114">1</span><span class="sxs-lookup"><span data-stu-id="91405-114">1</span></span>
</dt> <dd>

<span data-ttu-id="91405-115">Menos de 512 kilobytes por segundo (KBps).</span><span class="sxs-lookup"><span data-stu-id="91405-115">Less than 512 kilobytes per second (KBps).</span></span>

</dd> <dt>

<span data-ttu-id="91405-116">2</span><span class="sxs-lookup"><span data-stu-id="91405-116">2</span></span>
</dt> <dd>

<span data-ttu-id="91405-117">de 512 a 1.999 KBps.</span><span class="sxs-lookup"><span data-stu-id="91405-117">512 to 1,999 KBps.</span></span>

</dd> <dt>

<span data-ttu-id="91405-118">3</span><span class="sxs-lookup"><span data-stu-id="91405-118">3</span></span>
</dt> <dd>

<span data-ttu-id="91405-119">de 2.000 a 9.999 KBps.</span><span class="sxs-lookup"><span data-stu-id="91405-119">2,000 to 9,999 KBps.</span></span>

</dd> <dt>

<span data-ttu-id="91405-120">4</span><span class="sxs-lookup"><span data-stu-id="91405-120">4</span></span>
</dt> <dd>

<span data-ttu-id="91405-121">Mayor o igual que 10.000 KBps.</span><span class="sxs-lookup"><span data-stu-id="91405-121">Greater than or equal to 10,000 KBps.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="91405-122">*ancho de banda* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91405-122">*bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91405-123">Especifica el ancho de banda de conexión.</span><span class="sxs-lookup"><span data-stu-id="91405-123">Specifies the connection bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="91405-124">*RTT* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91405-124">*rtt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91405-125">Especifica la latencia de conexión.</span><span class="sxs-lookup"><span data-stu-id="91405-125">Specifies the connection latency.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91405-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91405-126">Return value</span></span>

<span data-ttu-id="91405-127">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="91405-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="91405-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91405-128">Requirements</span></span>



| <span data-ttu-id="91405-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="91405-129">Requirement</span></span> | <span data-ttu-id="91405-130">Value</span><span class="sxs-lookup"><span data-stu-id="91405-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="91405-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91405-131">Minimum supported client</span></span><br/> | <span data-ttu-id="91405-132">Windows 8</span><span class="sxs-lookup"><span data-stu-id="91405-132">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="91405-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91405-133">Minimum supported server</span></span><br/> | <span data-ttu-id="91405-134">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="91405-134">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="91405-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="91405-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="91405-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91405-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="91405-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="91405-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91405-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91405-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="91405-139">IID</span><span class="sxs-lookup"><span data-stu-id="91405-139">IID</span></span><br/>                      | <span data-ttu-id="91405-140">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="91405-140">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="91405-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="91405-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91405-142">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="91405-142">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





