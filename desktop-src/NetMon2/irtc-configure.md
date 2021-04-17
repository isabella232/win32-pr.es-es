---
description: Envía datos de configuración para una captura de datos.
ms.assetid: fb8c8ac8-cef4-45e0-bb06-3cf09c8ad9ac
title: 'IRTC:: Configure (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 702a3883acdbb7509d79e76d8fcc73af1e167e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652403"
---
# <a name="irtcconfigure-method"></a><span data-ttu-id="b370b-103">IRTC:: Configure (método)</span><span class="sxs-lookup"><span data-stu-id="b370b-103">IRTC::Configure method</span></span>

<span data-ttu-id="b370b-104">El método [**Configure**](configure.md) envía datos de configuración para una captura de datos.</span><span class="sxs-lookup"><span data-stu-id="b370b-104">The [**Configure**](configure.md) method submits configuration data for a data capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="b370b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b370b-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="b370b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b370b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b370b-107">*hConfigurationBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b370b-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b370b-108">Identificador del BLOB que el autor de la llamada configura.</span><span class="sxs-lookup"><span data-stu-id="b370b-108">A handle to the BLOB that is configured by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="b370b-109">*hErrorBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b370b-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b370b-110">Identificador de un BLOB de error que contiene datos de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="b370b-110">A handle to an error BLOB that contains additional error data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b370b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b370b-111">Return value</span></span>

<span data-ttu-id="b370b-112">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b370b-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b370b-113">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="b370b-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="b370b-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b370b-114">Return code</span></span>                                                                                                         | <span data-ttu-id="b370b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="b370b-115">Description</span></span>                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b370b-116"><dt>**\_BLOB NMERR \_ no \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="b370b-116"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="b370b-117">No se ha llamado al método **CreateBlob** .</span><span class="sxs-lookup"><span data-stu-id="b370b-117">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                 |
| <dl> <span data-ttu-id="b370b-118"><dt>**NMERR \_ BLOB no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b370b-118"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="b370b-119">El objeto al que apunta no es un BLOB.</span><span class="sxs-lookup"><span data-stu-id="b370b-119">The object pointed to is not a BLOB.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="b370b-120"><dt>**\_BLOB de nivel superior de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b370b-120"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="b370b-121">El número de versión del BLOB no es correcto.</span><span class="sxs-lookup"><span data-stu-id="b370b-121">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="b370b-122"><dt>**la \_ entrada de BLOB NMERR \_ \_ ya \_ existe**</dt></span><span class="sxs-lookup"><span data-stu-id="b370b-122"><dt>**NMERR\_BLOB\_ENTRY\_ALREADY\_EXISTS**</dt></span></span> </dl>  | <span data-ttu-id="b370b-123">BLOB duplicado.</span><span class="sxs-lookup"><span data-stu-id="b370b-123">Duplicate BLOB.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="b370b-124"><dt>**la \_ entrada de BLOB NMERR \_ \_ \_ no \_ existe**</dt></span><span class="sxs-lookup"><span data-stu-id="b370b-124"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="b370b-125">El BLOB de configuración especificado por *hConfigurationBlob* no tiene una entrada necesaria para realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="b370b-125">The configuration BLOB specified by *hConfigurationBlob* lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="b370b-126">Vea el BLOB de error devuelto por *hErrorBlob* para determinar qué entrada no se encontró.</span><span class="sxs-lookup"><span data-stu-id="b370b-126">View the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="b370b-127"><dt>**NMERR \_ ( \_ especificador ambiguo)**</dt></span><span class="sxs-lookup"><span data-stu-id="b370b-127"><dt>**NMERR\_AMBIGUOUS\_SPECIFIER**</dt></span></span> </dl>          | <span data-ttu-id="b370b-128">Faltan los datos de la categoría o del propietario del BLOB.</span><span class="sxs-lookup"><span data-stu-id="b370b-128">The BLOB Owner or Category data is missing.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="b370b-129"><dt>**\_ \_ \_ no \_ se encontró el propietario del BLOB de NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="b370b-129"><dt>**NMERR\_BLOB\_OWNER\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="b370b-130">No se encontró la sección del propietario del BLOB.</span><span class="sxs-lookup"><span data-stu-id="b370b-130">The BLOB Owner section was not found.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="b370b-131"><dt>**\_ \_ \_ no \_ se encontró la categoría de BLOB NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="b370b-131"><dt>**NMERR\_BLOB\_CATEGORY\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="b370b-132">No se encontró la sección de categoría de BLOB.</span><span class="sxs-lookup"><span data-stu-id="b370b-132">The BLOB Category section was not found.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="b370b-133"><dt>**NMERR \_ \_ categoría desconocida**</dt></span><span class="sxs-lookup"><span data-stu-id="b370b-133"><dt>**NMERR\_UNKNOWN\_CATEGORY**</dt></span></span> </dl>             | <span data-ttu-id="b370b-134">Se encontró la sección de la categoría BLOB, pero no se entendió.</span><span class="sxs-lookup"><span data-stu-id="b370b-134">The BLOB Category section was found, but not understood.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="b370b-135"><dt>**NMERR \_ \_ etiqueta desconocida**</dt></span><span class="sxs-lookup"><span data-stu-id="b370b-135"><dt>**NMERR\_UNKNOWN\_TAG**</dt></span></span> </dl>                  | <span data-ttu-id="b370b-136">La sección de etiqueta de BLOB se encontró, pero no se entendió.</span><span class="sxs-lookup"><span data-stu-id="b370b-136">The BLOB Tag section was found, but not understood.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="b370b-137"><dt>**\_error de \_ conversión de BLOB NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b370b-137"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="b370b-138">El BLOB está dañado.</span><span class="sxs-lookup"><span data-stu-id="b370b-138">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                           |
| <dl> <span data-ttu-id="b370b-139"><dt>**\_desencadenador no válido de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b370b-139"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="b370b-140">La parte del desencadenador del BLOB está dañada.</span><span class="sxs-lookup"><span data-stu-id="b370b-140">The trigger portion of the BLOB is corrupt.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="b370b-141"><dt>**NMERR \_ cadena de blob \_ \_ no válida**</dt></span><span class="sxs-lookup"><span data-stu-id="b370b-141"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="b370b-142">La cadena no termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="b370b-142">The string is not null-terminated.</span></span><br/>                                                                                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="b370b-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b370b-143">Remarks</span></span>

<span data-ttu-id="b370b-144">Debe aplicar este método para reiniciar un NPP que se ha iniciado, detenido, pero no está desconectado.</span><span class="sxs-lookup"><span data-stu-id="b370b-144">You must apply this method to restart an NPP that has been started, stopped, but not disconnected.</span></span>

<span data-ttu-id="b370b-145">El BLOB de error devuelto por *hErrorBlob* contiene entradas que monitor de red no pudo comprender o encontrar en el BLOB de configuración especificado en *hConfigurationBlob*.</span><span class="sxs-lookup"><span data-stu-id="b370b-145">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="b370b-146">El BLOB de error devuelto contiene datos de error que la aplicación puede usar para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="b370b-146">The returned error BLOB contains error data that the application can use for troubleshooting.</span></span> <span data-ttu-id="b370b-147">Por ejemplo, si \_ \_ se devuelve la entrada de BLOB NMERR \_ \_ \_ , la entrada monitor de red no se puede encontrar se incluye en el BLOB de error devuelto.</span><span class="sxs-lookup"><span data-stu-id="b370b-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor cannot find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="b370b-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b370b-148">Requirements</span></span>



| <span data-ttu-id="b370b-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="b370b-149">Requirement</span></span> | <span data-ttu-id="b370b-150">Value</span><span class="sxs-lookup"><span data-stu-id="b370b-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b370b-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b370b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="b370b-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b370b-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="b370b-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b370b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="b370b-154">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b370b-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="b370b-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b370b-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="b370b-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b370b-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="b370b-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b370b-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b370b-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b370b-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b370b-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="b370b-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b370b-160">IRTC</span><span class="sxs-lookup"><span data-stu-id="b370b-160">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="b370b-161">IRTC:: Connect</span><span class="sxs-lookup"><span data-stu-id="b370b-161">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="b370b-162">BLOBs Monitor de red</span><span class="sxs-lookup"><span data-stu-id="b370b-162">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




