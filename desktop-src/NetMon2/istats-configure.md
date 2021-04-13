---
description: El método configure envía información de configuración de la captura.
ms.assetid: 739ed1df-1a84-4c48-a1ac-2dba7a614cdd
title: 'IStas:: Configurate (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 9f2dddea3132ce81a57f16737c0f90c6277d4efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278605"
---
# <a name="istatsconfigure-method"></a><span data-ttu-id="ee4be-103">IStas:: Configure (método)</span><span class="sxs-lookup"><span data-stu-id="ee4be-103">IStats::Configure method</span></span>

<span data-ttu-id="ee4be-104">El método **Configure** envía información de configuración de la captura.</span><span class="sxs-lookup"><span data-stu-id="ee4be-104">The **Configure** method submits capture configuration information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee4be-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee4be-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="ee4be-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee4be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee4be-107">*hConfigurationBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee4be-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee4be-108">Identificador del BLOB que el autor de la llamada configura.</span><span class="sxs-lookup"><span data-stu-id="ee4be-108">Handle to the BLOB that the caller configures.</span></span>

</dd> <dt>

<span data-ttu-id="ee4be-109">*hErrorBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ee4be-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee4be-110">Identificador de un BLOB de error que contiene información de error adicional.</span><span class="sxs-lookup"><span data-stu-id="ee4be-110">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee4be-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee4be-111">Return value</span></span>

<span data-ttu-id="ee4be-112">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ee4be-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ee4be-113">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="ee4be-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="ee4be-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ee4be-114">Return code</span></span>                                                                                                         | <span data-ttu-id="ee4be-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee4be-115">Description</span></span>                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ee4be-116"><dt>**NMERR \_ cadena de blob \_ \_ no válida**</dt></span><span class="sxs-lookup"><span data-stu-id="ee4be-116"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="ee4be-117">La cadena no termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="ee4be-117">The string is not null-terminated.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="ee4be-118"><dt>**\_BLOB NMERR \_ no \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="ee4be-118"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="ee4be-119">No se ha llamado al método **CreateBlob** .</span><span class="sxs-lookup"><span data-stu-id="ee4be-119">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="ee4be-120"><dt>**NMERR \_ BLOB no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ee4be-120"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="ee4be-121">El objeto al que se apunta no es un BLOB.</span><span class="sxs-lookup"><span data-stu-id="ee4be-121">The object that is pointed to is not a BLOB.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="ee4be-122"><dt>**\_BLOB de nivel superior de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ee4be-122"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="ee4be-123">El número de versión del BLOB no es correcto.</span><span class="sxs-lookup"><span data-stu-id="ee4be-123">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="ee4be-124"><dt>**la \_ entrada de BLOB NMERR \_ \_ ya \_ existe**</dt></span><span class="sxs-lookup"><span data-stu-id="ee4be-124"><dt>**NMERR\_BLOB\_ENTRY\_ALREADY\_EXISTS**</dt></span></span> </dl>  | <span data-ttu-id="ee4be-125">Ya existe una entrada de BLOB.</span><span class="sxs-lookup"><span data-stu-id="ee4be-125">A BLOB entry already exists.</span></span><br/>                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="ee4be-126"><dt>**la \_ entrada de BLOB NMERR \_ \_ \_ no \_ existe**</dt></span><span class="sxs-lookup"><span data-stu-id="ee4be-126"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="ee4be-127">Falta una entrada necesaria para realizar esta operación en el BLOB de configuración especificado por el parámetro *hConfigurationBlob* .</span><span class="sxs-lookup"><span data-stu-id="ee4be-127">The configuration BLOB specified by the *hConfigurationBlob* parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="ee4be-128">Examine el BLOB de error devuelto por el parámetro *hErrorBlob* para determinar qué entrada no se encontró.</span><span class="sxs-lookup"><span data-stu-id="ee4be-128">Look at the error BLOB returned by the *hErrorBlob* parameter to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="ee4be-129"><dt>**NMERR \_ ( \_ especificador ambiguo)**</dt></span><span class="sxs-lookup"><span data-stu-id="ee4be-129"><dt>**NMERR\_AMBIGUOUS\_SPECIFIER**</dt></span></span> </dl>          | <span data-ttu-id="ee4be-130">Falta la información del propietario o de la categoría en el BLOB.</span><span class="sxs-lookup"><span data-stu-id="ee4be-130">The BLOB lacks owner or category information.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="ee4be-131"><dt>**\_ \_ \_ no \_ se encontró el propietario del BLOB de NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="ee4be-131"><dt>**NMERR\_BLOB\_OWNER\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="ee4be-132">No se encontró la sección Owner del BLOB.</span><span class="sxs-lookup"><span data-stu-id="ee4be-132">The Owner section of the BLOB was not found.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="ee4be-133"><dt>**\_ \_ \_ no \_ se encontró la categoría de BLOB NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="ee4be-133"><dt>**NMERR\_BLOB\_CATEGORY\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="ee4be-134">No se encontró la sección de categoría del BLOB.</span><span class="sxs-lookup"><span data-stu-id="ee4be-134">The Category section of the BLOB was not found.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="ee4be-135"><dt>**NMERR \_ \_ categoría desconocida**</dt></span><span class="sxs-lookup"><span data-stu-id="ee4be-135"><dt>**NMERR\_UNKNOWN\_CATEGORY**</dt></span></span> </dl>             | <span data-ttu-id="ee4be-136">Se encontró información de categoría, pero no se entendió.</span><span class="sxs-lookup"><span data-stu-id="ee4be-136">Category information was found but not understood.</span></span><br/>                                                                                                                                                                            |
| <dl> <span data-ttu-id="ee4be-137"><dt>**NMERR \_ \_ etiqueta desconocida**</dt></span><span class="sxs-lookup"><span data-stu-id="ee4be-137"><dt>**NMERR\_UNKNOWN\_TAG**</dt></span></span> </dl>                  | <span data-ttu-id="ee4be-138">Se encontró información de etiqueta, pero no se entendió.</span><span class="sxs-lookup"><span data-stu-id="ee4be-138">Tag information was found but not understood.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="ee4be-139"><dt>**\_error de \_ conversión de BLOB NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ee4be-139"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="ee4be-140">El BLOB está dañado.</span><span class="sxs-lookup"><span data-stu-id="ee4be-140">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="ee4be-141"><dt>**\_desencadenador no válido de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ee4be-141"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="ee4be-142">La parte del desencadenador del BLOB está dañada.</span><span class="sxs-lookup"><span data-stu-id="ee4be-142">The trigger portion of the BLOB is corrupt.</span></span><br/>                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="ee4be-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee4be-143">Remarks</span></span>

<span data-ttu-id="ee4be-144">Debe aplicar este método para reiniciar un NPP que se ha iniciado, detenido pero no desconectado.</span><span class="sxs-lookup"><span data-stu-id="ee4be-144">You must apply this method to restart an NPP that has been started, stopped but not disconnected.</span></span>

<span data-ttu-id="ee4be-145">El BLOB de error devuelto por *hErrorBlob* contiene entradas que monitor de red no pudo comprender o encontrar en el BLOB de configuración especificado en el parámetro *hConfigurationBlob* .</span><span class="sxs-lookup"><span data-stu-id="ee4be-145">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in the *hConfigurationBlob* parameter.</span></span> <span data-ttu-id="ee4be-146">El BLOB de error devuelto contiene información de error que la aplicación puede usar para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="ee4be-146">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="ee4be-147">Por ejemplo, si \_ \_ se devuelve la entrada de BLOB NMERR \_ \_ \_ , la entrada monitor de red no encontró se incluye en el BLOB de error devuelto.</span><span class="sxs-lookup"><span data-stu-id="ee4be-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee4be-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee4be-148">Requirements</span></span>



| <span data-ttu-id="ee4be-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee4be-149">Requirement</span></span> | <span data-ttu-id="ee4be-150">Value</span><span class="sxs-lookup"><span data-stu-id="ee4be-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee4be-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee4be-151">Minimum supported client</span></span><br/> | <span data-ttu-id="ee4be-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ee4be-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="ee4be-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee4be-153">Minimum supported server</span></span><br/> | <span data-ttu-id="ee4be-154">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ee4be-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="ee4be-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee4be-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee4be-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee4be-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="ee4be-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ee4be-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee4be-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee4be-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee4be-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee4be-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee4be-160">IStas</span><span class="sxs-lookup"><span data-stu-id="ee4be-160">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="ee4be-161">ISTA:: Connect</span><span class="sxs-lookup"><span data-stu-id="ee4be-161">ISTATS::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="ee4be-162">BLOBs Monitor de red</span><span class="sxs-lookup"><span data-stu-id="ee4be-162">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




