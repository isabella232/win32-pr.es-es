---
description: El método GetTotalStatistics recupera las estadísticas totales de la captura actual.
ms.assetid: 494634f6-a9b3-4a50-8920-2387be9ba30f
title: 'IStas:: GetTotalStatistics (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 51cdbfdcc796aa7d8091e8da5837809efaa63379
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678182"
---
# <a name="istatsgettotalstatistics-method"></a><span data-ttu-id="0c8a7-103">IStas:: GetTotalStatistics (método)</span><span class="sxs-lookup"><span data-stu-id="0c8a7-103">IStats::GetTotalStatistics method</span></span>

<span data-ttu-id="0c8a7-104">El método **GetTotalStatistics** recupera las [*Estadísticas totales*](t.md) de la [*captura*](c.md)actual.</span><span class="sxs-lookup"><span data-stu-id="0c8a7-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0c8a7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c8a7-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="0c8a7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c8a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c8a7-107">*lpStats* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0c8a7-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c8a7-108">Puntero a una estructura de [estadísticas](statistics.md)que proporciona las estadísticas totales de la captura.</span><span class="sxs-lookup"><span data-stu-id="0c8a7-108">Pointer to a [STATISTICS](statistics.md)structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="0c8a7-109">Es responsabilidad del autor de la llamada asignar y liberar la memoria que usa la estructura de **estadísticas** .</span><span class="sxs-lookup"><span data-stu-id="0c8a7-109">It is the caller's responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="0c8a7-110">*fClearAfterReading* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c8a7-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c8a7-111">Marca usada para indicar a Monitor de red cómo controlar el almacenamiento interno de las estadísticas totales.</span><span class="sxs-lookup"><span data-stu-id="0c8a7-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="0c8a7-112">Un valor TRUE indica a Monitor de red que borre el almacenamiento interno de las estadísticas totales una vez recuperada la información actual.</span><span class="sxs-lookup"><span data-stu-id="0c8a7-112">A setting of TRUE tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c8a7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c8a7-113">Return value</span></span>

<span data-ttu-id="0c8a7-114">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0c8a7-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0c8a7-115">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="0c8a7-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="0c8a7-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0c8a7-116">Return code</span></span>                                                                                            | <span data-ttu-id="0c8a7-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c8a7-117">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0c8a7-118"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="0c8a7-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="0c8a7-119">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="0c8a7-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="0c8a7-120">Llame al método [istas:: Connect](istats-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="0c8a7-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="0c8a7-121"><dt>**NMERR \_ no \_ solo estadísticas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c8a7-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="0c8a7-122">NPP está conectado a la red, pero no con el método [istas:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="0c8a7-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |
| <dl> <span data-ttu-id="0c8a7-123"><dt>**NMERR \_ no se \_ captura**</dt></span><span class="sxs-lookup"><span data-stu-id="0c8a7-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="0c8a7-124">NPP no está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="0c8a7-124">The NPP is not capturing data.</span></span> <span data-ttu-id="0c8a7-125">Llame al método [istas:: Start](istats-start.md) para empezar a capturar datos.</span><span class="sxs-lookup"><span data-stu-id="0c8a7-125">Call the [IStats::Start](istats-start.md) method to start capturing data.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="0c8a7-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c8a7-126">Remarks</span></span>

<span data-ttu-id="0c8a7-127">Este método devuelve los datos solo mientras una captura está en curso, incluso mientras la captura está en pausa.</span><span class="sxs-lookup"><span data-stu-id="0c8a7-127">This method returns data only while a capture is in progress, including while the capture is paused.</span></span>

<span data-ttu-id="0c8a7-128">Monitor de red también almacena [*estadísticas de conversación*](c.md), que se pueden recuperar llamando al método [istas:: GetConversationStatistics](istats-getconversationstatistics.md) .</span><span class="sxs-lookup"><span data-stu-id="0c8a7-128">Network Monitor also stores [*conversation statistics*](c.md), which can be retrieved by calling the [IStats::GetConversationStatistics](istats-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c8a7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c8a7-129">Requirements</span></span>



| <span data-ttu-id="0c8a7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c8a7-130">Requirement</span></span> | <span data-ttu-id="0c8a7-131">Value</span><span class="sxs-lookup"><span data-stu-id="0c8a7-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c8a7-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c8a7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0c8a7-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0c8a7-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0c8a7-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c8a7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0c8a7-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c8a7-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0c8a7-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c8a7-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c8a7-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c8a7-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0c8a7-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0c8a7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c8a7-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c8a7-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c8a7-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c8a7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c8a7-141">IStas</span><span class="sxs-lookup"><span data-stu-id="0c8a7-141">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="0c8a7-142">ISta:: Connect</span><span class="sxs-lookup"><span data-stu-id="0c8a7-142">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="0c8a7-143">IStas:: GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="0c8a7-143">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="0c8a7-144">IStas:: Start,</span><span class="sxs-lookup"><span data-stu-id="0c8a7-144">IStats::Start,</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="0c8a7-145">¡</span><span class="sxs-lookup"><span data-stu-id="0c8a7-145">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




