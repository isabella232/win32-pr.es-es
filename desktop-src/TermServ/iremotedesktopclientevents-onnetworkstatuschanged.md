---
title: IRemoteDesktopClientEvents OnNetworkStatusChanged, método
description: Se llama cuando el estado de la red ha cambiado. | IRemoteDesktopClientEvents OnNetworkStatusChanged, método
ms.assetid: B68D1AA0-6403-40CA-95C5-BBBF39CEFFD8
ms.tgt_platform: multiple
keywords:
- Método OnNetworkStatusChanged Servicios de Escritorio remoto
- Método OnNetworkStatusChanged Servicios de Escritorio remoto, interfaz IRemoteDesktopClientEvents
- Interfaz IRemoteDesktopClientEvents Servicios de Escritorio remoto, método OnNetworkStatusChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de64d8b16ea9acf9defc976d4baa91afd64f8fa7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547574"
---
# <a name="iremotedesktopclienteventsonnetworkstatuschanged-method"></a><span data-ttu-id="9aa21-107">IRemoteDesktopClientEvents:: OnNetworkStatusChanged (método)</span><span class="sxs-lookup"><span data-stu-id="9aa21-107">IRemoteDesktopClientEvents::OnNetworkStatusChanged method</span></span>

<span data-ttu-id="9aa21-108">Se llama cuando el estado de la red ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="9aa21-108">Called when the network status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa21-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9aa21-109">Syntax</span></span>


```C++
void OnNetworkStatusChanged(
  [in] unsigned long qualityLevel,
  [in] long          bandwidth,
  [in] long          rtt
);
```



## <a name="parameters"></a><span data-ttu-id="9aa21-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9aa21-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aa21-111">*qualityLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9aa21-111">*qualityLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa21-112">Nuevo nivel de calidad de la conexión.</span><span class="sxs-lookup"><span data-stu-id="9aa21-112">The new quality level of the connection.</span></span> <span data-ttu-id="9aa21-113">El nivel de calidad se determina a partir de los valores de ancho de banda y de tiempo de ida y vuelta (RTT).</span><span class="sxs-lookup"><span data-stu-id="9aa21-113">The quality level is determined from the bandwidth and round-trip time (rtt) values.</span></span>

<span data-ttu-id="9aa21-114">Uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="9aa21-114">One of the following values.</span></span>



| <span data-ttu-id="9aa21-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9aa21-115">Value</span></span>                                                                        | <span data-ttu-id="9aa21-116">Significado</span><span class="sxs-lookup"><span data-stu-id="9aa21-116">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="9aa21-117"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9aa21-117"><dt>0</dt></span></span> </dl> | <span data-ttu-id="9aa21-118">No se pudo determinar el nivel de calidad.</span><span class="sxs-lookup"><span data-stu-id="9aa21-118">The quality level could not be determined.</span></span><br/>       |
| <dl> <span data-ttu-id="9aa21-119"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9aa21-119"><dt>1</dt></span></span> </dl> | <span data-ttu-id="9aa21-120">La calidad de la conexión es deficiente (una barra).</span><span class="sxs-lookup"><span data-stu-id="9aa21-120">The connection quality is poor (one bar).</span></span><br/>        |
| <dl> <span data-ttu-id="9aa21-121"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9aa21-121"><dt>2</dt></span></span> </dl> | <span data-ttu-id="9aa21-122">La calidad de la conexión es justa (dos barras).</span><span class="sxs-lookup"><span data-stu-id="9aa21-122">The connection quality is fair (two bars).</span></span><br/>       |
| <dl> <span data-ttu-id="9aa21-123"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9aa21-123"><dt>3</dt></span></span> </dl> | <span data-ttu-id="9aa21-124">La calidad de la conexión es buena (tres barras).</span><span class="sxs-lookup"><span data-stu-id="9aa21-124">The connection quality is good (three bars).</span></span><br/>     |
| <dl> <span data-ttu-id="9aa21-125"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9aa21-125"><dt>4</dt></span></span> </dl> | <span data-ttu-id="9aa21-126">La calidad de la conexión es excelente (cuatro barras).</span><span class="sxs-lookup"><span data-stu-id="9aa21-126">The connection quality is excellent (four bars).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9aa21-127">*ancho de banda* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9aa21-127">*bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa21-128">Especifica el nuevo ancho de banda de conexión, en kilobits por segundo (kbps).</span><span class="sxs-lookup"><span data-stu-id="9aa21-128">Specifies the new connection bandwidth, in kilobits per second (Kbps).</span></span>

</dd> <dt>

<span data-ttu-id="9aa21-129">*RTT* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9aa21-129">*rtt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa21-130">Especifica el nuevo tiempo de ida y vuelta (latencia) de la conexión, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="9aa21-130">Specifies the new connection roundtrip time (latency), in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aa21-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9aa21-131">Return value</span></span>

<span data-ttu-id="9aa21-132">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9aa21-132">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aa21-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aa21-133">Requirements</span></span>



| <span data-ttu-id="9aa21-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aa21-134">Requirement</span></span> | <span data-ttu-id="9aa21-135">Value</span><span class="sxs-lookup"><span data-stu-id="9aa21-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aa21-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9aa21-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9aa21-137">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9aa21-137">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="9aa21-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9aa21-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9aa21-139">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9aa21-139">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="9aa21-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9aa21-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="9aa21-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aa21-141"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="9aa21-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9aa21-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9aa21-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aa21-143"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="9aa21-144">IID</span><span class="sxs-lookup"><span data-stu-id="9aa21-144">IID</span></span><br/>                      | <span data-ttu-id="9aa21-145">DIID \_ IRemoteDesktopClientEvents se define como 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="9aa21-145">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9aa21-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="9aa21-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aa21-147">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="9aa21-147">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





