---
description: Proporciona acceso a la memoria compartida entre los subprocesos de tableta.
ms.assetid: 047ff598-7d20-49d7-bdd3-498fe5c778c6
title: 'ITabletContextP:: UseSharedMemoryCommunications (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: d7880e1d0377d9d0140a0c82509abd31182c724e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717158"
---
# <a name="itabletcontextpusesharedmemorycommunications-method"></a><span data-ttu-id="39284-103">ITabletContextP:: UseSharedMemoryCommunications (método)</span><span class="sxs-lookup"><span data-stu-id="39284-103">ITabletContextP::UseSharedMemoryCommunications method</span></span>

<span data-ttu-id="39284-104">Proporciona acceso a la memoria compartida entre los subprocesos de tableta.</span><span class="sxs-lookup"><span data-stu-id="39284-104">Provides access to memory shared between tablet threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="39284-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39284-105">Syntax</span></span>


```C++
HRESULT UseSharedMemoryCommunications(
  [in]  DWORD pid,
  [out] DWORD *phEventMoreData,
  [out] DWORD *phEventClientReady,
  [out] DWORD *phMutexAccess,
  [out] DWORD *phFileMapping
);
```



## <a name="parameters"></a><span data-ttu-id="39284-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39284-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39284-107">*PID* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="39284-107">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39284-108">Identificador de proceso.</span><span class="sxs-lookup"><span data-stu-id="39284-108">Process id.</span></span>

</dd> <dt>

<span data-ttu-id="39284-109">*phEventMoreData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="39284-109">*phEventMoreData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39284-110">Identificador de evento que indica cuándo están disponibles los nuevos datos para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="39284-110">Event handle that signals when new data is available to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="39284-111">*phEventClientReady* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="39284-111">*phEventClientReady* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39284-112">Identificador de evento devuelto que se usa para indicar que el cliente está listo para recibir datos.</span><span class="sxs-lookup"><span data-stu-id="39284-112">Returned event handle used to signal that the client is ready to receive data.</span></span> <span data-ttu-id="39284-113">Señalado después del procesamiento de datos nuevos.</span><span class="sxs-lookup"><span data-stu-id="39284-113">Signaled after processing new data.</span></span>

</dd> <dt>

<span data-ttu-id="39284-114">*phMutexAccess* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="39284-114">*phMutexAccess* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39284-115">La exclusión mutua que concede acceso a la memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="39284-115">The mutex granting access to shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="39284-116">*phFileMapping* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="39284-116">*phFileMapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39284-117">Puntero al bloque de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="39284-117">Pointer to the shared memory block.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39284-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39284-118">Return value</span></span>

<span data-ttu-id="39284-119">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="39284-119">This method can return one of these values.</span></span>



| <span data-ttu-id="39284-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="39284-120">Return code</span></span>                                                                            | <span data-ttu-id="39284-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="39284-121">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="39284-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="39284-122"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="39284-123">Correcto.</span><span class="sxs-lookup"><span data-stu-id="39284-123">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="39284-124"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="39284-124"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="39284-125">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="39284-125">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="39284-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39284-126">Remarks</span></span>

<span data-ttu-id="39284-127">El método **UseSharedMemoryCommunications** se usa como parte del Protocolo de memoria compartida de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="39284-127">The **UseSharedMemoryCommunications** method is used as part of the Tablet PC shared memory protocol.</span></span> <span data-ttu-id="39284-128">Dado que el servicio Wisptis tiene un nivel de integridad alto (IL), puede almacenar y obtener acceso a los datos almacenados en la memoria compartida sin necesidad de elevar sus privilegios.</span><span class="sxs-lookup"><span data-stu-id="39284-128">Since the Wisptis service has a high integrity level (IL), it can store and access data stored in shared memory without needing to elevate its privileges.</span></span>

<span data-ttu-id="39284-129">La estructura de [**\_ encabezado SHAREDMEMORY**](sharedmemory-header.md) se convierte a partir de los datos a los que hace referencia la asignación de archivos y los datos de paquete sin formato siguen el **\_ encabezado SHAREDMEMORY**.</span><span class="sxs-lookup"><span data-stu-id="39284-129">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure is cast from the data referenced by the file mapping and the raw packet data follows the **SHAREDMEMORY\_HEADER**.</span></span> <span data-ttu-id="39284-130">Los datos de paquetes sin formato se pueden leer en la memoria compartida cuando se genera el evento al que hace referencia *pdwEventClientReady* .</span><span class="sxs-lookup"><span data-stu-id="39284-130">Raw packet data can be read off of the shared memory when the event referenced by *pdwEventClientReady* is raised.</span></span>

<span data-ttu-id="39284-131">En la lista siguiente se describe la secuencia de eventos para obtener acceso y usar la memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="39284-131">The following list describes the sequence of events for accessing and using shared memory.</span></span>

-   <span data-ttu-id="39284-132">El cliente establece el evento clientReady.</span><span class="sxs-lookup"><span data-stu-id="39284-132">The client sets the clientReady event.</span></span>
-   <span data-ttu-id="39284-133">El cliente espera el evento moreData.</span><span class="sxs-lookup"><span data-stu-id="39284-133">The client waits for the moreData event.</span></span>
-   <span data-ttu-id="39284-134">El cliente adquiere la exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="39284-134">The client acquires the mutex.</span></span>
-   <span data-ttu-id="39284-135">El cliente Lee los datos de paquetes de la sección de memoria compartida después del encabezado y los números de serie después de los paquetes.</span><span class="sxs-lookup"><span data-stu-id="39284-135">The client reads packet data from the section of shared memory after the header and serial numbers after the packets.</span></span>
-   <span data-ttu-id="39284-136">El cliente controla los datos en función del valor de **dwEvent**.</span><span class="sxs-lookup"><span data-stu-id="39284-136">The client handles data depending on the value of **dwEvent**.</span></span>
-   <span data-ttu-id="39284-137">El cliente escribe-1 (0xFFFFFFFF) en **dwEvent**.</span><span class="sxs-lookup"><span data-stu-id="39284-137">The client writes -1 (0xFFFFFFFF) into **dwEvent**.</span></span>
-   <span data-ttu-id="39284-138">El cliente libera la exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="39284-138">The client releases the mutex.</span></span>
-   <span data-ttu-id="39284-139">El cliente establece el evento clientReady.</span><span class="sxs-lookup"><span data-stu-id="39284-139">The client sets the clientReady event.</span></span>

## <a name="requirements"></a><span data-ttu-id="39284-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39284-140">Requirements</span></span>



| <span data-ttu-id="39284-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="39284-141">Requirement</span></span> | <span data-ttu-id="39284-142">Value</span><span class="sxs-lookup"><span data-stu-id="39284-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39284-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39284-143">Minimum supported client</span></span><br/> | <span data-ttu-id="39284-144">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="39284-144">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="39284-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39284-145">Minimum supported server</span></span><br/> | <span data-ttu-id="39284-146">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="39284-146">None supported</span></span><br/>                                                              |
| <span data-ttu-id="39284-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39284-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="39284-148"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="39284-148"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39284-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="39284-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39284-150">**Interfaz ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="39284-150">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> <dt>

[<span data-ttu-id="39284-151">**UseNamedSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="39284-151">**UseNamedSharedMemoryCommunications**</span></span>](itabletcontextp-usenamedsharedmemorycommunications.md)
</dt> </dl>

 

 




