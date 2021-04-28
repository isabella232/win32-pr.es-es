---
description: 'Método IDelaydC::GetConversationStatistics: el método GetConversationStatistics recupera información de sesión y estación sobre la captura actual.'
ms.assetid: 0164fa0e-90f2-4b97-be9d-55d172f8112d
title: Método IDelaydC::GetConversationStatistics (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d4d4c1bb1ad7ecb45b640c16322e297f9f640ef1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103813"
---
# <a name="idelaydcgetconversationstatistics-method"></a><span data-ttu-id="0c380-103">Método IDelaydC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="0c380-103">IDelaydC::GetConversationStatistics method</span></span>

<span data-ttu-id="0c380-104">El **método GetConversationStatistics** recupera información [*de*](s.md) sesión y [*estación*](s.md) sobre la captura actual.</span><span class="sxs-lookup"><span data-stu-id="0c380-104">The **GetConversationStatistics** method retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c380-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c380-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="0c380-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c380-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c380-107">*nSessions* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0c380-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c380-108">Puntero a un DWORD que contiene el número de [*sesiones*](s.md) registradas para la captura actual.</span><span class="sxs-lookup"><span data-stu-id="0c380-108">Pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="0c380-109">*lpSessionStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0c380-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c380-110">Puntero a una [estructura SESSIONSTATS.](sessionstats.md)</span><span class="sxs-lookup"><span data-stu-id="0c380-110">Pointer to a [SESSIONSTATS](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0c380-111">*nStations* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0c380-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c380-112">Puntero a un DWORD que contiene el número de [*estaciones*](s.md) registradas para la captura actual.</span><span class="sxs-lookup"><span data-stu-id="0c380-112">Pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="0c380-113">*lpStationStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0c380-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c380-114">Puntero a una [estructura STATIONSTATS.](stationstats.md)</span><span class="sxs-lookup"><span data-stu-id="0c380-114">Pointer to a [STATIONSTATS](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0c380-115">*fClearAfterReading* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0c380-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c380-116">Marca que se usa para Monitor de red borrar el almacenamiento interno de las estructuras [SESSIONSTATS](sessionstats.md) y [STATIONSTATS](stationstats.md) después de recuperar la información actual.</span><span class="sxs-lookup"><span data-stu-id="0c380-116">Flag used to tell Network Monitor to clear out the internal storage of the [SESSIONSTATS](sessionstats.md) and [STATIONSTATS](stationstats.md) structures after it retrieves the current information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c380-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c380-117">Return value</span></span>

<span data-ttu-id="0c380-118">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="0c380-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0c380-119">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="0c380-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="0c380-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0c380-120">Return code</span></span>                                                                                                   | <span data-ttu-id="0c380-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c380-121">Description</span></span>                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0c380-122"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="0c380-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="0c380-123">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="0c380-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="0c380-124">Llame [a IDelaydC::Connect](idelaydc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="0c380-124">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="0c380-125"><dt>**NMERR \_ NO \_ CAPTURA**</dt></span><span class="sxs-lookup"><span data-stu-id="0c380-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="0c380-126">El NPP no captura datos.</span><span class="sxs-lookup"><span data-stu-id="0c380-126">The NPP is not capturing data.</span></span> <span data-ttu-id="0c380-127">Llame [a IDelaydC::Start para](idelaydc-start.md) iniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="0c380-127">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="0c380-128"><dt>**NMERR \_ NO \_ RETRASADO**</dt></span><span class="sxs-lookup"><span data-stu-id="0c380-128"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>            | <span data-ttu-id="0c380-129">El NPP está conectado a la red, pero no con el [método IDelaydC::Connect.](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="0c380-129">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="0c380-130"><dt>**NMERR \_ NO \_ CONVERSATION \_ STATS**</dt></span><span class="sxs-lookup"><span data-stu-id="0c380-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="0c380-131">La configuración de esta conexión se establece para no guardar las estadísticas de conversación.</span><span class="sxs-lookup"><span data-stu-id="0c380-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="0c380-132">Para guardar las estadísticas de conversación, detenga la captura, establezca NoConversationStats = YES en el BLOB de configuración y reinicie la captura.</span><span class="sxs-lookup"><span data-stu-id="0c380-132">To save conversation statistics, stop the capture, set NoConversationStats = YES in the configuration BLOB, and then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0c380-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0c380-133">Remarks</span></span>

<span data-ttu-id="0c380-134">Solo se puede llamar a este método mientras la captura de datos está en curso; cuando la captura actual está en pausa, las llamadas a este método no se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="0c380-134">This method can only be called only while data capture is in progress; when the current capture is paused, calls to this method will not succeed.</span></span> <span data-ttu-id="0c380-135">Para iniciar una captura, llame al [método IDelaydC::Start.](idelaydc-start.md)</span><span class="sxs-lookup"><span data-stu-id="0c380-135">To start a capture, call the [IDelaydC::Start](idelaydc-start.md) method.</span></span>

<span data-ttu-id="0c380-136">Para recuperar otros tipos de estadísticas, llame a [IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="0c380-136">To retrieve other types of statistics, call [IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c380-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c380-137">Requirements</span></span>



| <span data-ttu-id="0c380-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c380-138">Requirement</span></span> | <span data-ttu-id="0c380-139">Valor</span><span class="sxs-lookup"><span data-stu-id="0c380-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c380-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c380-140">Minimum supported client</span></span><br/> | <span data-ttu-id="0c380-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0c380-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0c380-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c380-142">Minimum supported server</span></span><br/> | <span data-ttu-id="0c380-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c380-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0c380-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c380-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c380-145"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="0c380-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0c380-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0c380-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c380-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c380-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c380-148">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0c380-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c380-149">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="0c380-149">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="0c380-150">IDelaydC::Connect</span><span class="sxs-lookup"><span data-stu-id="0c380-150">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="0c380-151">IDelaydC::GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="0c380-151">IDelaydC::GetTotalStatistics</span></span>](idelaydc-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="0c380-152">IDelaydC::Start</span><span class="sxs-lookup"><span data-stu-id="0c380-152">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="0c380-153">SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="0c380-153">SESSIONSTATS</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="0c380-154">STATIONSTATS</span><span class="sxs-lookup"><span data-stu-id="0c380-154">STATIONSTATS</span></span>](stationstats.md)
</dt> </dl>

 

 




