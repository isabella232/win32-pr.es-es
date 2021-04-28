---
description: 'Método IDelaydC::GetTotalStatistics: el método GetTotalStatistics recupera las estadísticas totales de la captura actual.'
ms.assetid: 904c7496-5603-41b9-8481-06fa31f6f112
title: Método IDelaydC::GetTotalStatistics (Netmon.h)
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
ms.openlocfilehash: b3a0ce4f230236e276fede528a5e778ecafd51fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113533"
---
# <a name="idelaydcgettotalstatistics-method"></a><span data-ttu-id="2ff27-103">IDelaydC::GetTotalStatistics (método)</span><span class="sxs-lookup"><span data-stu-id="2ff27-103">IDelaydC::GetTotalStatistics method</span></span>

<span data-ttu-id="2ff27-104">El **método GetTotalStatistics** recupera las [*estadísticas totales*](t.md) de la captura [*actual.*](c.md)</span><span class="sxs-lookup"><span data-stu-id="2ff27-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2ff27-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ff27-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="2ff27-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ff27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ff27-107">*lpStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2ff27-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff27-108">Puntero a una [estructura STATISTICS](statistics.md)que proporciona las estadísticas totales de la captura.</span><span class="sxs-lookup"><span data-stu-id="2ff27-108">Pointer to a [STATISTICS](statistics.md)structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="2ff27-109">Es responsabilidad del autor de la llamada asignar y liberar la memoria utilizada por la **estructura STATISTICS.**</span><span class="sxs-lookup"><span data-stu-id="2ff27-109">It is the caller's responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="2ff27-110">*fClearAfterReading* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2ff27-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff27-111">Marca que se usa para Monitor de red cómo controlar el almacenamiento interno de las estadísticas totales.</span><span class="sxs-lookup"><span data-stu-id="2ff27-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="2ff27-112">Una configuración **de TRUE** indica Monitor de red borrar el almacenamiento interno de las estadísticas totales después de recuperar la información actual.</span><span class="sxs-lookup"><span data-stu-id="2ff27-112">A setting of **TRUE** tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ff27-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ff27-113">Return value</span></span>

<span data-ttu-id="2ff27-114">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="2ff27-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2ff27-115">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="2ff27-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="2ff27-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2ff27-116">Return code</span></span>                                                                                          | <span data-ttu-id="2ff27-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ff27-117">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2ff27-118"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="2ff27-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="2ff27-119">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="2ff27-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="2ff27-120">Llame [a IDelaydC::Connect](idelaydc-connect.md) para conectarse a la red.</span><span class="sxs-lookup"><span data-stu-id="2ff27-120">Call [IDelaydC::Connect](idelaydc-connect.md) to connect to the network.</span></span><br/> |
| <dl> <span data-ttu-id="2ff27-121"><dt>**NMERR \_ NO \_ RETRASADA**</dt></span><span class="sxs-lookup"><span data-stu-id="2ff27-121"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="2ff27-122">El NPP está conectado a la red, pero no con [el método IDelaydC::Connect.](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="2ff27-122">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>             |
| <dl> <span data-ttu-id="2ff27-123"><dt>**NMERR \_ NO \_ CAPTURA**</dt></span><span class="sxs-lookup"><span data-stu-id="2ff27-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="2ff27-124">El NPP no captura datos.</span><span class="sxs-lookup"><span data-stu-id="2ff27-124">The NPP is not capturing data.</span></span> <span data-ttu-id="2ff27-125">Llame [a IDelaydC::Start para](idelaydc-start.md) empezar a capturar datos.</span><span class="sxs-lookup"><span data-stu-id="2ff27-125">Call [IDelaydC::Start](idelaydc-start.md) to start capturing data.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="2ff27-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2ff27-126">Remarks</span></span>

<span data-ttu-id="2ff27-127">Este método devuelve datos solo mientras hay una captura en curso; cuando la captura está en pausa, las llamadas a este método no se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="2ff27-127">This method returns data only while a capture is in progress; when the capture is paused, calls to this method will not succeed.</span></span>

<span data-ttu-id="2ff27-128">Monitor de red también almacena [*estadísticas*](c.md)de conversación, que se pueden recuperar llamando al método [IDelaydC::GetConversationStatistics.](idelaydc-getconversationstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="2ff27-128">Network Monitor also stores [*conversation statistics*](c.md), which can be retrieved by calling the [IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ff27-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ff27-129">Requirements</span></span>



| <span data-ttu-id="2ff27-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ff27-130">Requirement</span></span> | <span data-ttu-id="2ff27-131">Valor</span><span class="sxs-lookup"><span data-stu-id="2ff27-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ff27-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ff27-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2ff27-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2ff27-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="2ff27-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ff27-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2ff27-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2ff27-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="2ff27-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ff27-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ff27-137"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="2ff27-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="2ff27-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2ff27-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ff27-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ff27-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ff27-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2ff27-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ff27-141">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="2ff27-141">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="2ff27-142">IDelaydC::Connect</span><span class="sxs-lookup"><span data-stu-id="2ff27-142">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="2ff27-143">IDelaydC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="2ff27-143">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="2ff27-144">IDelaydC::Start</span><span class="sxs-lookup"><span data-stu-id="2ff27-144">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="2ff27-145">Estadísticas</span><span class="sxs-lookup"><span data-stu-id="2ff27-145">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




