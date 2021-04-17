---
description: Configura la comunicación de la memoria compartida para el contexto de la tableta.
ms.assetid: 63e6b271-d89a-4c91-9a15-9e41dcdfa363
title: 'ITabletContextP:: UseNamedSharedMemoryCommunications (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseNamedSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 81e8c653dd12600ae02fe7e6038de6e6a38786e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716301"
---
# <a name="itabletcontextpusenamedsharedmemorycommunications-method"></a><span data-ttu-id="23deb-103">ITabletContextP:: UseNamedSharedMemoryCommunications (método)</span><span class="sxs-lookup"><span data-stu-id="23deb-103">ITabletContextP::UseNamedSharedMemoryCommunications method</span></span>

<span data-ttu-id="23deb-104">Configura la comunicación de la memoria compartida para el contexto de la tableta.</span><span class="sxs-lookup"><span data-stu-id="23deb-104">Sets up shared memory communication for the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="23deb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23deb-105">Syntax</span></span>


```C++
HRESULT UseNamedSharedMemoryCommunications(
  [in]  DWORD  pid,
  [in]  LPCSTR pszCallerSid,
  [in]  LPCSTR pszCallerIntegritySid,
  [out] DWORD  *pdwEventMoreDataId,
  [out] DWORD  *pdwEventClientReadyId,
  [out] DWORD  *pdwMutexAccessId,
  [out] DWORD  *pdwFileMappingId
);
```



## <a name="parameters"></a><span data-ttu-id="23deb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23deb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23deb-107">*PID* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="23deb-107">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23deb-108">El ID. de proceso del cliente que tiene acceso a la memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="23deb-108">The process ID of the client that accesses shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="23deb-109">*pszCallerSid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="23deb-109">*pszCallerSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23deb-110">El identificador de seguridad del autor de la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="23deb-110">The security identifier of the function caller.</span></span>

</dd> <dt>

<span data-ttu-id="23deb-111">*pszCallerIntegritySid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="23deb-111">*pszCallerIntegritySid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23deb-112">El identificador de seguridad que puede comprobar la integridad de la función de llamada.</span><span class="sxs-lookup"><span data-stu-id="23deb-112">The security identifier that can verify the integrity of the calling function.</span></span>

</dd> <dt>

<span data-ttu-id="23deb-113">*pdwEventMoreDataId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="23deb-113">*pdwEventMoreDataId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23deb-114">Entero que se usa para construir el nombre de un evento.</span><span class="sxs-lookup"><span data-stu-id="23deb-114">An integer used to construct the name of an event.</span></span> <span data-ttu-id="23deb-115">El evento indica si hay más datos.</span><span class="sxs-lookup"><span data-stu-id="23deb-115">The event indicates whether there is more data.</span></span>

</dd> <dt>

<span data-ttu-id="23deb-116">*pdwEventClientReadyId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="23deb-116">*pdwEventClientReadyId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23deb-117">Entero que se usa para construir el nombre de un evento.</span><span class="sxs-lookup"><span data-stu-id="23deb-117">An integer used to construct the name of an event.</span></span> <span data-ttu-id="23deb-118">El evento indica que el cliente está listo para recibir datos.</span><span class="sxs-lookup"><span data-stu-id="23deb-118">The event signals that the client is ready to receive data.</span></span> <span data-ttu-id="23deb-119">El evento se señala después de procesar los datos nuevos.</span><span class="sxs-lookup"><span data-stu-id="23deb-119">The event is signaled after processing new data.</span></span>

</dd> <dt>

<span data-ttu-id="23deb-120">*pdwMutexAccessId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="23deb-120">*pdwMutexAccessId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23deb-121">Puntero al identificador de acceso de la memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="23deb-121">A pointer to the access identifier of the shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="23deb-122">*pdwFileMappingId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="23deb-122">*pdwFileMappingId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23deb-123">Un entero que identifica la memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="23deb-123">An integer that identifies the shared memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23deb-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23deb-124">Return value</span></span>

<span data-ttu-id="23deb-125">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="23deb-125">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="23deb-126">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="23deb-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="23deb-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23deb-127">Remarks</span></span>

<span data-ttu-id="23deb-128">El método **UseNamedSharedMemoryCommunications** forma parte del Protocolo de memoria compartida de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="23deb-128">The **UseNamedSharedMemoryCommunications** method is part of the Tablet PC shared memory protocol.</span></span> <span data-ttu-id="23deb-129">Un cliente sin privilegios elevados pasa en un identificador de seguridad (SID) y un identificador de seguridad de nivel de integridad (IL-SID) para que el servicio de tableta pueda utilizar listas de control de acceso (ACL) para tener acceso a los objetos de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="23deb-129">A client without elevated privileges passes in a security identifier (SID) and an integrity level security identifier (IL-SID) so that the Tablet service can use access control lists (ACL) to access the shared memory objects.</span></span> <span data-ttu-id="23deb-130">Si el cliente tiene privilegios elevados, debe usar UseSharedMemoryCommunications, que es la API a la que se llama si el servicio ya tiene privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="23deb-130">If the client has elevated privileges, it should use UseSharedMemoryCommunications, which is the API that is called if the service already has an elevated privilege.</span></span>

<span data-ttu-id="23deb-131">La estructura del [**\_ encabezado SHAREDMEMORY**](sharedmemory-header.md) almacena el encabezado de la memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="23deb-131">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure stores the shared memory header.</span></span>

<span data-ttu-id="23deb-132">La estructura del [**\_ encabezado SHAREDMEMORY**](sharedmemory-header.md) se convierte a partir de los datos a los que hace referencia la asignación de archivos.</span><span class="sxs-lookup"><span data-stu-id="23deb-132">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure is cast from the data referenced by the file mapping.</span></span> <span data-ttu-id="23deb-133">Los datos de paquete sin formato siguen el **\_ encabezado SHAREDMEMORY**.</span><span class="sxs-lookup"><span data-stu-id="23deb-133">The raw packet data follows the **SHAREDMEMORY\_HEADER**.</span></span> <span data-ttu-id="23deb-134">Los datos de paquetes sin formato se pueden leer en la memoria compartida cuando se genera el evento al que hace referencia *pdwEventClientReadyId* .</span><span class="sxs-lookup"><span data-stu-id="23deb-134">Raw packet data can be read off of the shared memory when the event referenced by *pdwEventClientReadyId* is raised.</span></span>

<span data-ttu-id="23deb-135">En la lista siguiente se describe la secuencia de eventos para obtener acceso y usar la memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="23deb-135">The following list describes the sequence of events for accessing and using shared memory.</span></span>

1.  <span data-ttu-id="23deb-136">El cliente genera el evento clientReady.</span><span class="sxs-lookup"><span data-stu-id="23deb-136">The client raises the clientReady event.</span></span>
2.  <span data-ttu-id="23deb-137">El cliente espera el evento moreData.</span><span class="sxs-lookup"><span data-stu-id="23deb-137">The client waits for the moreData event.</span></span>
3.  <span data-ttu-id="23deb-138">El cliente adquiere la exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="23deb-138">The client acquires the mutex.</span></span>
4.  <span data-ttu-id="23deb-139">El cliente Lee los datos de paquete de la sección de memoria compartida que sigue al encabezado.</span><span class="sxs-lookup"><span data-stu-id="23deb-139">The client reads packet data from the section of shared memory that follows the header.</span></span> <span data-ttu-id="23deb-140">Los números de serie aparecen en la memoria compartida después de los datos del paquete.</span><span class="sxs-lookup"><span data-stu-id="23deb-140">Serial numbers appear in the shared memory after the packet data.</span></span>
5.  <span data-ttu-id="23deb-141">El cliente controla los datos en función del valor de **dwEvent**.</span><span class="sxs-lookup"><span data-stu-id="23deb-141">The client handles data depending on the value of **dwEvent**.</span></span>
6.  <span data-ttu-id="23deb-142">El cliente escribe-1 (0xFFFFFFFF) en **dwEvent**.</span><span class="sxs-lookup"><span data-stu-id="23deb-142">The client writes -1 (0xFFFFFFFF) into **dwEvent**.</span></span>
7.  <span data-ttu-id="23deb-143">El cliente libera la exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="23deb-143">The client releases the mutex.</span></span>
8.  <span data-ttu-id="23deb-144">El cliente genera el evento clientReady.</span><span class="sxs-lookup"><span data-stu-id="23deb-144">The client raises the clientReady event.</span></span>

<span data-ttu-id="23deb-145">Los nombres de evento se crean dando formato al resultado de este método.</span><span class="sxs-lookup"><span data-stu-id="23deb-145">The event names are created by formatting the output of this method.</span></span> <span data-ttu-id="23deb-146">Las siguientes definiciones se pueden usar junto con sprintf o su equivalente para crear los nombres de evento.</span><span class="sxs-lookup"><span data-stu-id="23deb-146">The following definitions can be used in conjunction with sprintf or its equivalent to create the event names.</span></span>


```C++
#define WISPTIS_SM_MORE_DATA_EVENT_NAME     _T("wisptis-1-%d-%u")
#define WISPTIS_SM_CLIENT_DONE_EVENT_NAME   _T("wisptis-2-%d-%u")
#define WISPTIS_SM_SECTION_NAME             _T("wisptis-3-%d-%u")
#define WISPTIS_SM_THREAD_EVENT_NAME        _T("wisptis-4-%u")
```



<span data-ttu-id="23deb-147">En cada definición, la sección% d se reemplaza por el identificador de proceso y la sección% u se reemplaza por el entero devuelto en *pdwEventMoreDataId* o *pdwEventClientReadyId*.</span><span class="sxs-lookup"><span data-stu-id="23deb-147">In each definition, the %d section is replaced with the process ID, and the %u section is replaced with the integer returned in *pdwEventMoreDataId* or *pdwEventClientReadyId*.</span></span>

## <a name="requirements"></a><span data-ttu-id="23deb-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23deb-148">Requirements</span></span>



| <span data-ttu-id="23deb-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="23deb-149">Requirement</span></span> | <span data-ttu-id="23deb-150">Value</span><span class="sxs-lookup"><span data-stu-id="23deb-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23deb-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23deb-151">Minimum supported client</span></span><br/> | <span data-ttu-id="23deb-152">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="23deb-152">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="23deb-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23deb-153">Minimum supported server</span></span><br/> | <span data-ttu-id="23deb-154">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="23deb-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="23deb-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23deb-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="23deb-156"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="23deb-156"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23deb-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="23deb-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23deb-158">**UseSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="23deb-158">**UseSharedMemoryCommunications**</span></span>](itabletcontextp-usesharedmemorycommunications.md)
</dt> <dt>

[<span data-ttu-id="23deb-159">**ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="23deb-159">**ITabletContextP**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




