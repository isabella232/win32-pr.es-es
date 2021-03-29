---
description: El método configure envía información de configuración para una captura.
ms.assetid: b8cbbae1-3c07-489f-8e8f-77c95ec03209
title: 'IESP:: Configure (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 53efbe7eb2887165dacc4cb904822de953b84017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666269"
---
# <a name="iespconfigure-method"></a><span data-ttu-id="6c755-103">IESP:: Configure (método)</span><span class="sxs-lookup"><span data-stu-id="6c755-103">IESP::Configure method</span></span>

<span data-ttu-id="6c755-104">El método **Configure** envía información de configuración para una captura.</span><span class="sxs-lookup"><span data-stu-id="6c755-104">The **Configure** method submits configuration information for a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c755-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c755-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="6c755-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c755-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c755-107">*hConfigurationBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c755-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c755-108">Identificador del BLOB que el autor de la llamada configura.</span><span class="sxs-lookup"><span data-stu-id="6c755-108">Handle to the BLOB that the caller configures.</span></span>

</dd> <dt>

<span data-ttu-id="6c755-109">*hErrorBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6c755-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c755-110">Identificador de un BLOB de error que contiene información de error adicional.</span><span class="sxs-lookup"><span data-stu-id="6c755-110">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="6c755-111">Para obtener información sobre el contenido de un BLOB de error, consulte la sección Comentarios de este tema.</span><span class="sxs-lookup"><span data-stu-id="6c755-111">For information about the contents of an error BLOB, see the Remarks section in this topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c755-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c755-112">Return value</span></span>

<span data-ttu-id="6c755-113">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6c755-113">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6c755-114">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="6c755-114">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="6c755-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6c755-115">Return code</span></span>                                                                                                         | <span data-ttu-id="6c755-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c755-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c755-117"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="6c755-117"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>                | <span data-ttu-id="6c755-118">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="6c755-118">The NPP is not connected to the network.</span></span><br/>                                                                                                                                                               |
| <dl> <span data-ttu-id="6c755-119"><dt>**NMERR \_ no \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="6c755-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>                      | <span data-ttu-id="6c755-120">NPP está conectado a la red, pero no con el método [iesp:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="6c755-120">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="6c755-121"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c755-121"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>                     | <span data-ttu-id="6c755-122">El NPP informa de que se ha iniciado la sesión de captura.</span><span class="sxs-lookup"><span data-stu-id="6c755-122">The NPP reports that the capture session has started.</span></span><br/>                                                                                                                                                  |
| <dl> <span data-ttu-id="6c755-123"><dt>**\_desencadenador no válido de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c755-123"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="6c755-124">La parte del desencadenador del BLOB de configuración está dañada.</span><span class="sxs-lookup"><span data-stu-id="6c755-124">The trigger portion of the configuration BLOB is corrupt.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="6c755-125"><dt>**la \_ entrada de BLOB NMERR \_ \_ \_ no \_ existe**</dt></span><span class="sxs-lookup"><span data-stu-id="6c755-125"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="6c755-126">Falta una entrada necesaria para realizar esta operación en el BLOB de configuración especificado por *hConfigurationBlob* .</span><span class="sxs-lookup"><span data-stu-id="6c755-126">The configuration BLOB specified by *hConfigurationBlob* is missing an entry needed to perform this operation.</span></span> <span data-ttu-id="6c755-127">Observe el BLOB de error devuelto por *hErrorBlob* para determinar qué entrada no se encontró.</span><span class="sxs-lookup"><span data-stu-id="6c755-127">Look at the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="6c755-128"><dt>**\_error de \_ conversión de BLOB NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c755-128"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="6c755-129">El BLOB está dañado.</span><span class="sxs-lookup"><span data-stu-id="6c755-129">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="6c755-130"><dt>**\_BLOB NMERR \_ no \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="6c755-130"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="6c755-131">No se ha llamado al método **CreateBlob** .</span><span class="sxs-lookup"><span data-stu-id="6c755-131">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="6c755-132"><dt>**NMERR \_ BLOB no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c755-132"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="6c755-133">El objeto al que se apunta no es un BLOB.</span><span class="sxs-lookup"><span data-stu-id="6c755-133">The object that is pointed to is not a BLOB.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="6c755-134"><dt>**NMERR \_ cadena de blob \_ \_ no válida**</dt></span><span class="sxs-lookup"><span data-stu-id="6c755-134"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="6c755-135">La cadena no termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="6c755-135">The string is not null-terminated.</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="6c755-136"><dt>**\_BLOB de nivel superior de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c755-136"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="6c755-137">El número de versión del BLOB no es correcto.</span><span class="sxs-lookup"><span data-stu-id="6c755-137">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="6c755-138"><dt>**NMERR \_ \_ de \_ memoria insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="6c755-138"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>               | <span data-ttu-id="6c755-139">No había memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="6c755-139">No memory was available.</span></span> <span data-ttu-id="6c755-140">Cierre Windows para liberar recursos.</span><span class="sxs-lookup"><span data-stu-id="6c755-140">Shut down windows to free up resources.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="6c755-141"><dt>**tiempo de espera de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c755-141"><dt>**NMERR\_TIMEOUT**</dt></span></span> </dl>                       | <span data-ttu-id="6c755-142">La solicitud ha agotado el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="6c755-142">The request has timed out.</span></span><br/>                                                                                                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="6c755-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c755-143">Remarks</span></span>

<span data-ttu-id="6c755-144">Debe aplicar este método para reiniciar un NPP que se ha iniciado y detenido, pero no está desconectado.</span><span class="sxs-lookup"><span data-stu-id="6c755-144">You must apply this method to restart an NPP that has been started and stopped, but not disconnected.</span></span>

<span data-ttu-id="6c755-145">El BLOB de error devuelto por el parámetro *hErrorBlob* contiene entradas que monitor de red no pudieron comprender o encontrar en el BLOB de configuración especificado en *hConfigurationBlob*.</span><span class="sxs-lookup"><span data-stu-id="6c755-145">The error BLOB returned by the *hErrorBlob* parameter contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="6c755-146">El BLOB de error devuelto contiene información de error que la aplicación puede usar para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="6c755-146">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="6c755-147">Por ejemplo, si \_ \_ se devuelve la entrada de BLOB NMERR \_ \_ \_ , la entrada monitor de red no encontró se incluye en el BLOB de error devuelto.</span><span class="sxs-lookup"><span data-stu-id="6c755-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c755-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c755-148">Requirements</span></span>



| <span data-ttu-id="6c755-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c755-149">Requirement</span></span> | <span data-ttu-id="6c755-150">Value</span><span class="sxs-lookup"><span data-stu-id="6c755-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c755-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c755-151">Minimum supported client</span></span><br/> | <span data-ttu-id="6c755-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6c755-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="6c755-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c755-153">Minimum supported server</span></span><br/> | <span data-ttu-id="6c755-154">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6c755-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="6c755-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c755-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c755-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c755-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="6c755-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6c755-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c755-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c755-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

 




