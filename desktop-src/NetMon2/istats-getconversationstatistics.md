---
description: Recupera información de la sesión y de la estación sobre la captura actual.
ms.assetid: 7fc436fc-b569-402d-a1ea-c1bb65de8a9e
title: 'IStas:: GetConversationStatistics (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 030fafb4ccf041c2804179f8adf0088ca3fba845
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678577"
---
# <a name="istatsgetconversationstatistics-method"></a><span data-ttu-id="e82ef-103">IStas:: GetConversationStatistics (método)</span><span class="sxs-lookup"><span data-stu-id="e82ef-103">IStats::GetConversationStatistics method</span></span>

<span data-ttu-id="e82ef-104">El método **GetConversationStatistics** recupera información de la sesión y de la estación sobre la captura actual.</span><span class="sxs-lookup"><span data-stu-id="e82ef-104">The **GetConversationStatistics** method retrieves session and station information about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="e82ef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e82ef-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="e82ef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e82ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e82ef-107">*nSessions* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e82ef-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e82ef-108">Un puntero a un valor DWORD que contiene el número de [*sesiones*](s.md) registradas para la captura actual.</span><span class="sxs-lookup"><span data-stu-id="e82ef-108">A pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="e82ef-109">*lpSessionStats* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e82ef-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e82ef-110">Puntero a una estructura [**SESSIONSTATS**](sessionstats.md) .</span><span class="sxs-lookup"><span data-stu-id="e82ef-110">A pointer to a [**SESSIONSTATS**](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e82ef-111">*nStations* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e82ef-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e82ef-112">Un puntero a un valor DWORD que contiene el número de [*estaciones*](s.md) registradas para la captura actual.</span><span class="sxs-lookup"><span data-stu-id="e82ef-112">A pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="e82ef-113">*lpStationStats* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e82ef-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e82ef-114">Puntero a una estructura [**STATIONSTATS**](stationstats.md) .</span><span class="sxs-lookup"><span data-stu-id="e82ef-114">A pointer to a [**STATIONSTATS**](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e82ef-115">*fClearAfterReading* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e82ef-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e82ef-116">Marca usada para indicar a Monitor de red que borre el almacenamiento interno de las estructuras [**SESSIONSTATS**](sessionstats.md) y [**STATIONSTATS**](stationstats.md) después de que se recuperen los datos actuales.</span><span class="sxs-lookup"><span data-stu-id="e82ef-116">Flag used to instruct Network Monitor to clear the internal storage of the [**SESSIONSTATS**](sessionstats.md) and [**STATIONSTATS**](stationstats.md) structures after the current data is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e82ef-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e82ef-117">Return value</span></span>

<span data-ttu-id="e82ef-118">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e82ef-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e82ef-119">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="e82ef-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="e82ef-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e82ef-120">Return code</span></span>                                                                                                   | <span data-ttu-id="e82ef-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="e82ef-121">Description</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e82ef-122"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="e82ef-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="e82ef-123">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="e82ef-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="e82ef-124">Llame a los [**istas:: Connect**](istats-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="e82ef-124">Call [**IStats::Connect**](istats-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="e82ef-125"><dt>**NMERR \_ no se \_ captura**</dt></span><span class="sxs-lookup"><span data-stu-id="e82ef-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="e82ef-126">NPP no está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="e82ef-126">The NPP is not capturing data.</span></span> <span data-ttu-id="e82ef-127">Llame a los [**ISTA:: Start**](istats-start.md) para iniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="e82ef-127">Call [**IStats::Start**](istats-start.md) to start the capture.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="e82ef-128"><dt>**NMERR \_ no \_ solo estadísticas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e82ef-128"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl>        | <span data-ttu-id="e82ef-129">NPP está conectado a la red, pero no con el método [**istas:: Connect**](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="e82ef-129">The NPP is connected to the network, but not with the [**IStats::Connect**](istats-connect.md) method.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="e82ef-130"><dt>**NMERR \_ no \_ hay \_ estadísticas de conversación**</dt></span><span class="sxs-lookup"><span data-stu-id="e82ef-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="e82ef-131">La configuración de esta conexión está establecida en no guardar estadísticas de conversación.</span><span class="sxs-lookup"><span data-stu-id="e82ef-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="e82ef-132">Para guardar las estadísticas de conversación, detenga la captura, establezca **NoConversationStats = Yes** en el BLOB de configuración y, a continuación, reinicie la captura.</span><span class="sxs-lookup"><span data-stu-id="e82ef-132">To save conversation statistics, stop the capture, set **NoConversationStats = YES** in the configuration BLOB, and then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e82ef-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e82ef-133">Remarks</span></span>

<span data-ttu-id="e82ef-134">Solo se puede llamar a este método cuando la captura de datos está en curso; Cuando la captura actual está en pausa, una llamada a este método no se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="e82ef-134">This method can be called only while data capture is in progress; when the current capture is paused, a call to this method will not succeed.</span></span>

<span data-ttu-id="e82ef-135">Para iniciar una captura, llame al método [**istas:: Start**](istats-start.md) .</span><span class="sxs-lookup"><span data-stu-id="e82ef-135">To start a capture, call the [**IStats::Start**](istats-start.md) method.</span></span> <span data-ttu-id="e82ef-136">Para recuperar otros tipos de estadísticas, llame a [**istas:: GetTotalStatistics**](istats-gettotalstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="e82ef-136">To retrieve other types of statistics, call [**IStats::GetTotalStatistics**](istats-gettotalstatistics.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e82ef-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e82ef-137">Requirements</span></span>



| <span data-ttu-id="e82ef-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e82ef-138">Requirement</span></span> | <span data-ttu-id="e82ef-139">Value</span><span class="sxs-lookup"><span data-stu-id="e82ef-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e82ef-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e82ef-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e82ef-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e82ef-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="e82ef-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e82ef-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e82ef-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e82ef-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="e82ef-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e82ef-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="e82ef-145"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e82ef-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="e82ef-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e82ef-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e82ef-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e82ef-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e82ef-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="e82ef-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e82ef-149">**IStas**</span><span class="sxs-lookup"><span data-stu-id="e82ef-149">**IStats**</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="e82ef-150">**IStas:: GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="e82ef-150">**IStats::GetTotalStatistics**</span></span>](istats-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="e82ef-151">**ISta:: Start**</span><span class="sxs-lookup"><span data-stu-id="e82ef-151">**IStats::Start**</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="e82ef-152">**ISta:: Connect**</span><span class="sxs-lookup"><span data-stu-id="e82ef-152">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="e82ef-153">**SESSIONSTATS**</span><span class="sxs-lookup"><span data-stu-id="e82ef-153">**SESSIONSTATS**</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="e82ef-154">**STATIONSTATS**</span><span class="sxs-lookup"><span data-stu-id="e82ef-154">**STATIONSTATS**</span></span>](stationstats.md)
</dt> </dl>

 

 




