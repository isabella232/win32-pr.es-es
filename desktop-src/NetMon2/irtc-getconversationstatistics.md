---
description: 'Método IRTC::GetConversationStatistics: el método GetConversationStatistics recupera información de sesión y estación sobre la captura actual.'
ms.assetid: 27f364cd-fee9-4262-b181-c5f15fb12e51
title: Método IRTC::GetConversationStatistics (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 4d2476f4eb33d7e74d0de8363fa88d5e688a2e73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110703"
---
# <a name="irtcgetconversationstatistics-method"></a><span data-ttu-id="69279-103">IrTC::GetConversationStatistics (método)</span><span class="sxs-lookup"><span data-stu-id="69279-103">IRTC::GetConversationStatistics method</span></span>

<span data-ttu-id="69279-104">El **método GetConversationStatistics** recupera información [*de*](s.md) sesión y [*estación*](s.md) sobre la captura actual.</span><span class="sxs-lookup"><span data-stu-id="69279-104">The **GetConversationStatistics** method retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="69279-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69279-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="69279-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69279-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69279-107">*nSessions* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="69279-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69279-108">Puntero a un DWORD que contiene el número de [*sesiones*](s.md) registradas para la captura actual.</span><span class="sxs-lookup"><span data-stu-id="69279-108">Pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="69279-109">*lpSessionStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="69279-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69279-110">Puntero a una [estructura SESSIONSTATS.](sessionstats.md)</span><span class="sxs-lookup"><span data-stu-id="69279-110">Pointer to a [SESSIONSTATS](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="69279-111">*nStations* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="69279-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69279-112">Puntero a un DWORD que contiene el número de [*estaciones*](s.md) registradas para la captura actual.</span><span class="sxs-lookup"><span data-stu-id="69279-112">Pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="69279-113">*lpStationStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="69279-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69279-114">Puntero a una [estructura STATIONSTATS.](stationstats.md)</span><span class="sxs-lookup"><span data-stu-id="69279-114">Pointer to a [STATIONSTATS](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="69279-115">*fClearAfterReading* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="69279-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69279-116">Marca que se usa para Monitor de red borrar el almacenamiento interno de las estructuras [SESSIONSTATS](sessionstats.md) y [STATIONSTATS](stationstats.md) después de recuperar la información actual.</span><span class="sxs-lookup"><span data-stu-id="69279-116">Flag used to tell Network Monitor to clear out the internal storage of the [SESSIONSTATS](sessionstats.md) and [STATIONSTATS](stationstats.md) structures after it retrieves the current information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69279-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69279-117">Return value</span></span>

<span data-ttu-id="69279-118">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="69279-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="69279-119">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="69279-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="69279-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="69279-120">Return code</span></span>                                                                                                   | <span data-ttu-id="69279-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="69279-121">Description</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="69279-122"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="69279-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="69279-123">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="69279-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="69279-124">Llame [a IRTC::Connect](irtc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="69279-124">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="69279-125"><dt>**NMERR \_ NO \_ CAPTURA**</dt></span><span class="sxs-lookup"><span data-stu-id="69279-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="69279-126">El NPP no captura datos.</span><span class="sxs-lookup"><span data-stu-id="69279-126">The NPP is not capturing data.</span></span> <span data-ttu-id="69279-127">Llame [a IRTC::Start](irtc-start.md) para iniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="69279-127">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="69279-128"><dt>**NMERR \_ NOT \_ REALTIME**</dt></span><span class="sxs-lookup"><span data-stu-id="69279-128"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>           | <span data-ttu-id="69279-129">El NPP está conectado a la red, pero no con el [método IRTC::Connect.](irtc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="69279-129">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                                                                                                                          |
| <dl> <span data-ttu-id="69279-130"><dt>**NMERR \_ NO \_ CONVERSATION \_ STATS**</dt></span><span class="sxs-lookup"><span data-stu-id="69279-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="69279-131">La configuración de esta conexión se establece para no guardar las estadísticas de conversación.</span><span class="sxs-lookup"><span data-stu-id="69279-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="69279-132">Para guardar las estadísticas de conversación, detenga la captura, establezca NoConversationStats = YES en el BLOB de configuración y reinicie la captura.</span><span class="sxs-lookup"><span data-stu-id="69279-132">To save conversation statistics, stop the capture, set NoConversationStats = YES in the configuration BLOB, then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="69279-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="69279-133">Remarks</span></span>

<span data-ttu-id="69279-134">Solo se puede llamar a este método mientras se capturan datos; Si llama a este método mientras la captura actual está en pausa, el método no se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="69279-134">This method can only be called while you are capturing data; if you call this method while the current capture is paused, the method will not succeed.</span></span> <span data-ttu-id="69279-135">Para iniciar una captura, llame al [método IRTC::Start.](irtc-start.md)</span><span class="sxs-lookup"><span data-stu-id="69279-135">To start a capture, call the [IRTC::Start](irtc-start.md) method.</span></span>

<span data-ttu-id="69279-136">Para recuperar otros tipos de estadísticas, llame al [método IRTC::GetTotalStatistics.](irtc-gettotalstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="69279-136">To retrieve other types of statistics, call the [IRTC::GetTotalStatistics](irtc-gettotalstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="69279-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69279-137">Requirements</span></span>



| <span data-ttu-id="69279-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="69279-138">Requirement</span></span> | <span data-ttu-id="69279-139">Valor</span><span class="sxs-lookup"><span data-stu-id="69279-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69279-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69279-140">Minimum supported client</span></span><br/> | <span data-ttu-id="69279-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="69279-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="69279-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69279-142">Minimum supported server</span></span><br/> | <span data-ttu-id="69279-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="69279-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="69279-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69279-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="69279-145"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="69279-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="69279-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="69279-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69279-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69279-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69279-148">Consulte también</span><span class="sxs-lookup"><span data-stu-id="69279-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69279-149">IRTC</span><span class="sxs-lookup"><span data-stu-id="69279-149">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="69279-150">IRTC::Connect</span><span class="sxs-lookup"><span data-stu-id="69279-150">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="69279-151">IRTC::GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="69279-151">IRTC::GetTotalStatistics</span></span>](irtc-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="69279-152">IRTC::Start</span><span class="sxs-lookup"><span data-stu-id="69279-152">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="69279-153">SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="69279-153">SESSIONSTATS</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="69279-154">STATIONSTATS</span><span class="sxs-lookup"><span data-stu-id="69279-154">STATIONSTATS</span></span>](stationstats.md)
</dt> </dl>

 

 




