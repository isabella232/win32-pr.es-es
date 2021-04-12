---
description: El método GetTotalStatistics recupera las estadísticas totales de la captura actual.
ms.assetid: 904c7496-5603-41b9-8481-06fa31f6f112
title: 'IDelaydC:: GetTotalStatistics (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0d194426933532fcf7a1965ed59b099489eefcb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423679"
---
# <a name="idelaydcgettotalstatistics-method"></a><span data-ttu-id="18e30-103">IDelaydC:: GetTotalStatistics (método)</span><span class="sxs-lookup"><span data-stu-id="18e30-103">IDelaydC::GetTotalStatistics method</span></span>

<span data-ttu-id="18e30-104">El método **GetTotalStatistics** recupera las [*Estadísticas totales*](t.md) de la [*captura*](c.md)actual.</span><span class="sxs-lookup"><span data-stu-id="18e30-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="18e30-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18e30-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="18e30-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18e30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18e30-107">*lpStats* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="18e30-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18e30-108">Puntero a una estructura de [estadísticas](statistics.md)que proporciona las estadísticas totales de la captura.</span><span class="sxs-lookup"><span data-stu-id="18e30-108">Pointer to a [STATISTICS](statistics.md)structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="18e30-109">Es responsabilidad del autor de la llamada asignar y liberar la memoria que usa la estructura de **estadísticas** .</span><span class="sxs-lookup"><span data-stu-id="18e30-109">It is the caller's responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="18e30-110">*fClearAfterReading* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="18e30-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18e30-111">Marca usada para indicar a Monitor de red cómo controlar el almacenamiento interno de las estadísticas totales.</span><span class="sxs-lookup"><span data-stu-id="18e30-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="18e30-112">Un valor **true** indica a monitor de red que borre el almacenamiento interno de las estadísticas totales una vez recuperada la información actual.</span><span class="sxs-lookup"><span data-stu-id="18e30-112">A setting of **TRUE** tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18e30-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18e30-113">Return value</span></span>

<span data-ttu-id="18e30-114">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="18e30-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="18e30-115">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="18e30-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="18e30-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="18e30-116">Return code</span></span>                                                                                          | <span data-ttu-id="18e30-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="18e30-117">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="18e30-118"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="18e30-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="18e30-119">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="18e30-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="18e30-120">Llame a [IDelaydC:: Connect](idelaydc-connect.md) para conectarse a la red.</span><span class="sxs-lookup"><span data-stu-id="18e30-120">Call [IDelaydC::Connect](idelaydc-connect.md) to connect to the network.</span></span><br/> |
| <dl> <span data-ttu-id="18e30-121"><dt>**NMERR \_ no \_ retrasado**</dt></span><span class="sxs-lookup"><span data-stu-id="18e30-121"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="18e30-122">NPP está conectado a la red, pero no con el método [IDelaydC:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="18e30-122">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>             |
| <dl> <span data-ttu-id="18e30-123"><dt>**NMERR \_ no se \_ captura**</dt></span><span class="sxs-lookup"><span data-stu-id="18e30-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="18e30-124">NPP no está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="18e30-124">The NPP is not capturing data.</span></span> <span data-ttu-id="18e30-125">Llame a [IDelaydC:: Start](idelaydc-start.md) para empezar a capturar datos.</span><span class="sxs-lookup"><span data-stu-id="18e30-125">Call [IDelaydC::Start](idelaydc-start.md) to start capturing data.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="18e30-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18e30-126">Remarks</span></span>

<span data-ttu-id="18e30-127">Este método devuelve los datos solo mientras una captura está en curso; Cuando se pausa la captura, las llamadas a este método no se realizarán correctamente.</span><span class="sxs-lookup"><span data-stu-id="18e30-127">This method returns data only while a capture is in progress; when the capture is paused, calls to this method will not succeed.</span></span>

<span data-ttu-id="18e30-128">Monitor de red también almacena [*estadísticas de conversación*](c.md), que se pueden recuperar llamando al método [IDelaydC:: GetConversationStatistics](idelaydc-getconversationstatistics.md) .</span><span class="sxs-lookup"><span data-stu-id="18e30-128">Network Monitor also stores [*conversation statistics*](c.md), which can be retrieved by calling the [IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="18e30-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18e30-129">Requirements</span></span>



| <span data-ttu-id="18e30-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="18e30-130">Requirement</span></span> | <span data-ttu-id="18e30-131">Value</span><span class="sxs-lookup"><span data-stu-id="18e30-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18e30-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18e30-132">Minimum supported client</span></span><br/> | <span data-ttu-id="18e30-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="18e30-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="18e30-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18e30-134">Minimum supported server</span></span><br/> | <span data-ttu-id="18e30-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="18e30-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="18e30-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18e30-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="18e30-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="18e30-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="18e30-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="18e30-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18e30-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18e30-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18e30-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="18e30-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18e30-141">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="18e30-141">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="18e30-142">IDelaydC:: Connect</span><span class="sxs-lookup"><span data-stu-id="18e30-142">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="18e30-143">IDelaydC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="18e30-143">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="18e30-144">IDelaydC:: Start</span><span class="sxs-lookup"><span data-stu-id="18e30-144">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="18e30-145">¡</span><span class="sxs-lookup"><span data-stu-id="18e30-145">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




