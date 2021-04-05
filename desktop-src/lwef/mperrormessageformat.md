---
title: Función MpErrorMessageFormat (MpClient. h)
description: Devuelve un mensaje de error con formato basado en un código de error.
ms.assetid: C125FCE4-3BB0-4608-BBF3-E7FEF17D0807
keywords:
- Función MpErrorMessageFormat características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MpErrorMessageFormat
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a3499b3be885b29135d22b470da4143cfb23ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996969"
---
# <a name="mperrormessageformat-function"></a><span data-ttu-id="acf66-104">MpErrorMessageFormat función)</span><span class="sxs-lookup"><span data-stu-id="acf66-104">MpErrorMessageFormat function</span></span>

<span data-ttu-id="acf66-105">Devuelve un mensaje de error con formato basado en un código de error.</span><span class="sxs-lookup"><span data-stu-id="acf66-105">Returns a formatted error message based on an error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="acf66-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="acf66-106">Syntax</span></span>


```C++
HRESULT WINAPI MpErrorMessageFormat(
  _In_  MPHANDLE hMpHandle,
  _In_  HRESULT  hrError,
  _Out_ LPWSTR   *pwszErrorDesc
);
```



## <a name="parameters"></a><span data-ttu-id="acf66-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="acf66-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acf66-108">*hMpHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="acf66-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acf66-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="acf66-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="acf66-110">Identificador de la interfaz del administrador de protección contra malware.</span><span class="sxs-lookup"><span data-stu-id="acf66-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="acf66-111">La función [**MpManagerOpen**](mpmanageropen.md) devuelve este identificador.</span><span class="sxs-lookup"><span data-stu-id="acf66-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="acf66-112">*hrError* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="acf66-112">*hrError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acf66-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="acf66-113">Type: **HRESULT**</span></span>

<span data-ttu-id="acf66-114">Un código de error basado en **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="acf66-114">An **HRESULT**-based error code.</span></span>

</dd> <dt>

<span data-ttu-id="acf66-115">*pwszErrorDesc* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="acf66-115">*pwszErrorDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acf66-116">Tipo: \**LPWStr \** _</span><span class="sxs-lookup"><span data-stu-id="acf66-116">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="acf66-117">Devuelve un mensaje de error con formato basado en _hrError \*.</span><span class="sxs-lookup"><span data-stu-id="acf66-117">Returns a formatted error message based on _hrError\*.</span></span> <span data-ttu-id="acf66-118">Esta cadena se debe liberar mediante [**MpFreeMemory**](mpfreememory.md).</span><span class="sxs-lookup"><span data-stu-id="acf66-118">This string must be freed using [**MpFreeMemory**](mpfreememory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acf66-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="acf66-119">Return value</span></span>

<span data-ttu-id="acf66-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="acf66-120">Type: **HRESULT**</span></span>

<span data-ttu-id="acf66-121">Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="acf66-121">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="acf66-122">Si se produce un error en la función, el valor devuelto es un código **HRESULT** erróneo.</span><span class="sxs-lookup"><span data-stu-id="acf66-122">If the function fails then the return value is a failed **HRESULT** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="acf66-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="acf66-123">Remarks</span></span>

<span data-ttu-id="acf66-124">Esta función es capaz de dar formato a los códigos de error del sistema, además de códigos de error específicos devueltos por las funciones de protección contra malware.</span><span class="sxs-lookup"><span data-stu-id="acf66-124">This function is capable of formatting system error codes in addition to specific error codes returned by malware protection functions.</span></span> <span data-ttu-id="acf66-125">Los códigos de error **HRESULT** específicos de las funciones de protección contra malware tienen una instalación de 0x50.</span><span class="sxs-lookup"><span data-stu-id="acf66-125">The **HRESULT** error codes specific to malware protection functions have a facility of 0x50.</span></span> <span data-ttu-id="acf66-126">A continuación se muestra una lista de un subconjunto de códigos de error específicos de protección contra malware que pueden ser devueltos por diversas funciones de protección contra malware.</span><span class="sxs-lookup"><span data-stu-id="acf66-126">Below is a list of a subset of the malware protection-specific error codes that can be returned by various malware protection functions.</span></span> <span data-ttu-id="acf66-127">Con la macro **HRESULT \_ del \_ \_ Estado de MP**, los siguientes códigos de error se pueden convertir en **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="acf66-127">Using the macro **HRESULT\_FROM\_MP\_STATUS**, the following error codes can be converted to **HRESULT**.</span></span> <span data-ttu-id="acf66-128">Vea también [códigos de error del motor de antimalware de Forefront Client Security](https://support.microsoft.com/kb/939359) para obtener una lista de otros códigos de error posibles.</span><span class="sxs-lookup"><span data-stu-id="acf66-128">See also [Forefront Client Security anti-malware engine error codes](https://support.microsoft.com/kb/939359) for a list of other possible error codes.</span></span>



| <span data-ttu-id="acf66-129">Código de error</span><span class="sxs-lookup"><span data-stu-id="acf66-129">Error Code</span></span>                              | <span data-ttu-id="acf66-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="acf66-130">Description</span></span>                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acf66-131">ERROR de procesador \_ MP \_</span><span class="sxs-lookup"><span data-stu-id="acf66-131">ERROR\_MP\_NOENGINE</span></span>                     | <span data-ttu-id="acf66-132">No se ha cargado ningún motor en el servicio antimalware para realizar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="acf66-132">No engine is loaded in antimalware service to perform the requested operation.</span></span>                                              |
| <span data-ttu-id="acf66-133">ERROR de \_ MP \_ sin \_ memoria</span><span class="sxs-lookup"><span data-stu-id="acf66-133">ERROR\_MP\_NO\_MEMORY</span></span>                   | <span data-ttu-id="acf66-134">El motor de antimalware ha encontrado una situación de falta de memoria.</span><span class="sxs-lookup"><span data-stu-id="acf66-134">The antimalware engine has encountered a no memory situation.</span></span>                                                               |
| <span data-ttu-id="acf66-135">ERROR de \_ eliminación del módulo de administración \_ \_</span><span class="sxs-lookup"><span data-stu-id="acf66-135">ERROR\_MP\_REMOVE\_FAILED</span></span>               | <span data-ttu-id="acf66-136">No se pudo realizar la operación de eliminación de una amenaza concreta.</span><span class="sxs-lookup"><span data-stu-id="acf66-136">Remove operation failed for a specific threat.</span></span>                                                                              |
| <span data-ttu-id="acf66-137">ERROR de \_ cuarentena del módulo de administración \_ \_</span><span class="sxs-lookup"><span data-stu-id="acf66-137">ERROR\_MP\_QUARANTINE\_FAILED</span></span>           | <span data-ttu-id="acf66-138">No se pudo realizar la operación de cuarentena para una amenaza concreta.</span><span class="sxs-lookup"><span data-stu-id="acf66-138">Quarantine operation failed for a specific threat.</span></span>                                                                          |
| <span data-ttu-id="acf66-139">\_ \_ \_ no \_ se encontró la amenaza del módulo de administración</span><span class="sxs-lookup"><span data-stu-id="acf66-139">ERROR\_MP\_THREAT\_NOT\_FOUND</span></span>           | <span data-ttu-id="acf66-140">La amenaza específica ya no existe en el sistema.</span><span class="sxs-lookup"><span data-stu-id="acf66-140">The specific threat no longer exists in the system.</span></span>                                                                         |
| <span data-ttu-id="acf66-141">ERROR \_ al \_ quitar MP \_ no \_ compatible</span><span class="sxs-lookup"><span data-stu-id="acf66-141">ERROR\_MP\_REMOVE\_NOT\_SUPPORTED</span></span>       | <span data-ttu-id="acf66-142">No se admite la operación de eliminación de una amenaza concreta dentro del tipo de contenedor.</span><span class="sxs-lookup"><span data-stu-id="acf66-142">Remove operation for a specific threat inside the container type is not supported.</span></span>                                          |
| <span data-ttu-id="acf66-143">ERROR de \_ MP \_ quitar \_ contenedor inmutable \_</span><span class="sxs-lookup"><span data-stu-id="acf66-143">ERROR\_MP\_REMOVE\_IMMUTABLE\_CONTAINER</span></span> | <span data-ttu-id="acf66-144">Debido a la Directiva del motor, no se admite una operación de eliminación de una amenaza específica dentro de un contenedor bloqueado.</span><span class="sxs-lookup"><span data-stu-id="acf66-144">Due to engine policy, a remove operation of a specific threat inside a blocked container is not supported.</span></span> <span data-ttu-id="acf66-145">(Archivos de correo electrónico).</span><span class="sxs-lookup"><span data-stu-id="acf66-145">(Mail archives.)</span></span> |
| <span data-ttu-id="acf66-146">ERROR \_ MP \_ BADDB \_ OLDENGINE</span><span class="sxs-lookup"><span data-stu-id="acf66-146">ERROR\_MP\_BADDB\_OLDENGINE</span></span>             | <span data-ttu-id="acf66-147">La solicitud de actualización de firma proporcionó un motor o archivos de firma antiguos.</span><span class="sxs-lookup"><span data-stu-id="acf66-147">Signature update request provided an older engine or signature files(s).</span></span>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="acf66-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acf66-148">Requirements</span></span>



| <span data-ttu-id="acf66-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="acf66-149">Requirement</span></span> | <span data-ttu-id="acf66-150">Value</span><span class="sxs-lookup"><span data-stu-id="acf66-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acf66-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="acf66-151">Minimum supported client</span></span><br/> | <span data-ttu-id="acf66-152">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="acf66-152">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="acf66-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="acf66-153">Minimum supported server</span></span><br/> | <span data-ttu-id="acf66-154">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="acf66-154">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="acf66-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="acf66-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="acf66-156"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="acf66-156"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="acf66-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="acf66-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acf66-158"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acf66-158"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acf66-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="acf66-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acf66-160">**MpFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="acf66-160">**MpFreeMemory**</span></span>](mpfreememory.md)
</dt> <dt>

[<span data-ttu-id="acf66-161">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="acf66-161">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="acf66-162">Códigos de error del motor de antimalware de Forefront Client Security</span><span class="sxs-lookup"><span data-stu-id="acf66-162">Forefront Client Security anti-malware engine error codes</span></span>](https://support.microsoft.com/kb/939359)
</dt> </dl>

 

 





