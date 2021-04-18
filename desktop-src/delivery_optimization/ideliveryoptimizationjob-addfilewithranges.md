---
title: Método IDeliveryOptimizationJob AddFileWithRanges (Deliveryoptimization. h)
description: Agrega un archivo a un trabajo de descarga y especifica los intervalos del archivo que desea descargar.
ms.assetid: 23F0A39F-670F-4030-A3B3-4F9277FFA8AB
keywords:
- Método AddFileWithRanges
- Método AddFileWithRanges, interfaz IDeliveryOptimizationJob
- Interfaz IDeliveryOptimizationJob, método AddFileWithRanges
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob.AddFileWithRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc147f5cb3f91a2fe0b8518493dba72798ce8056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714645"
---
# <a name="ideliveryoptimizationjobaddfilewithranges-method"></a><span data-ttu-id="85852-106">IDeliveryOptimizationJob:: AddFileWithRanges (método)</span><span class="sxs-lookup"><span data-stu-id="85852-106">IDeliveryOptimizationJob::AddFileWithRanges method</span></span>

<span data-ttu-id="85852-107">Agrega un archivo a un trabajo de descarga y especifica los intervalos del archivo que desea descargar.</span><span class="sxs-lookup"><span data-stu-id="85852-107">Adds a file to a download job and specifies the ranges of the file you want to download.</span></span>

## <a name="syntax"></a><span data-ttu-id="85852-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85852-108">Syntax</span></span>


```C++
HRESULT AddFileWithRanges(
  [in]           LPCWSTR       fileId,
  [in]           LPCWSTR       remoteUrl,
  [in]           LPCWSTR       localName,
  [in, optional] DWORD         rangeCount,
  [in, optional] BG_FILE_RANGE ranges[],
  [in, optional] ULONG64       fileSize
);
```



## <a name="parameters"></a><span data-ttu-id="85852-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85852-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85852-110">*fileid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85852-110">*fileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85852-111">Cadena terminada en null que es un identificador único del contenido publicado.</span><span class="sxs-lookup"><span data-stu-id="85852-111">Null terminated string that s an unique identifier of the published content.</span></span> <span data-ttu-id="85852-112">En el caso de contenido no publicado, puede ser cualquier cadena única que el llamador pueda usar para identificar los archivos dentro de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="85852-112">For non-published content, this can be any unique string that caller can use to identify files within a job.</span></span>

</dd> <dt>

<span data-ttu-id="85852-113">*remoteUrl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85852-113">*remoteUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85852-114">Cadena terminada en null que contiene el nombre del archivo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="85852-114">Null-terminated string that contains the name of the file on the server.</span></span>

</dd> <dt>

<span data-ttu-id="85852-115">*localname* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85852-115">*localName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85852-116">Cadena terminada en null que contiene el nombre del archivo en el cliente.</span><span class="sxs-lookup"><span data-stu-id="85852-116">Null-terminated string that contains the name of the file on the client.</span></span>

</dd> <dt>

<span data-ttu-id="85852-117">*rangeCount* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="85852-117">*rangeCount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85852-118">Número de elementos de *intervalos*.</span><span class="sxs-lookup"><span data-stu-id="85852-118">Number of elements in *Ranges*.</span></span>

</dd> <dt>

<span data-ttu-id="85852-119">*intervalos* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="85852-119">*ranges* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85852-120">Matriz de una o varias estructuras de [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) que especifican los intervalos que se van a descargar.</span><span class="sxs-lookup"><span data-stu-id="85852-120">Array of one or more [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) structures that specify the ranges to download.</span></span> <span data-ttu-id="85852-121">No especifique intervalos duplicados o superpuestos.</span><span class="sxs-lookup"><span data-stu-id="85852-121">Do not specify duplicate or overlapping ranges.</span></span>

</dd> <dt>

<span data-ttu-id="85852-122">*archivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="85852-122">*fileSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85852-123">Tamaño del archivo en bytes.</span><span class="sxs-lookup"><span data-stu-id="85852-123">Size of the file in bytes.</span></span> <span data-ttu-id="85852-124">Pase **DO_UNKNOWN_FILE_SIZE** si la aplicación del llamador no conoce el tamaño.</span><span class="sxs-lookup"><span data-stu-id="85852-124">Pass in **DO_UNKNOWN_FILE_SIZE** if size is not known to the caller application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85852-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85852-125">Return value</span></span>

<span data-ttu-id="85852-126">Este método devuelve los siguientes valores devueltos, así como otros.</span><span class="sxs-lookup"><span data-stu-id="85852-126">This method returns the following return values, as well as others.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85852-127">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="85852-127">Return code</span></span></th>
<th><span data-ttu-id="85852-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="85852-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="85852-129"><dt><strong><strong>S_OK</strong></strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85852-129"><dt><strong><strong>S_OK</strong></strong></dt> </span></span></dl></td>
<td><span data-ttu-id="85852-130">Correcto.</span><span class="sxs-lookup"><span data-stu-id="85852-130">Success.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="85852-131"><dt><strong>E_INVALIDARG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85852-131"><dt><strong>E_INVALIDARG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="85852-132">El nombre del archivo local es nulo o es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="85852-132">The local file name is NULL or empty string.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="85852-133"><dt><strong>E_ACCESSDENIED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85852-133"><dt><strong>E_ACCESSDENIED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="85852-134">El usuario no tiene permiso para escribir en el directorio especificado en el cliente.</span><span class="sxs-lookup"><span data-stu-id="85852-134">User does not have permission to write to the specified directory on the client.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="85852-135"><dt><strong>DO_E_INVALID_RANGE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85852-135"><dt><strong>DO_E_INVALID_RANGE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="85852-136">Uno de los intervalos no es válido.</span><span class="sxs-lookup"><span data-stu-id="85852-136">One of the ranges is invalid.</span></span> <span data-ttu-id="85852-137">Por ejemplo, InitialOffset se establece en <strong>BG_LENGTH_TO_EOF</strong>.</span><span class="sxs-lookup"><span data-stu-id="85852-137">For example, InitialOffset is set to <strong>BG_LENGTH_TO_EOF</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="85852-138"><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85852-138"><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="85852-139">No se pueden especificar intervalos duplicados o superpuestos.</span><span class="sxs-lookup"><span data-stu-id="85852-139">You cannot specify duplicate or overlapping ranges.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="85852-140">Los intervalos se ordenan por el desplazamiento del valor, no por la longitud.</span><span class="sxs-lookup"><span data-stu-id="85852-140">The ranges are sorted by the offset of the value, not the length.</span></span> <span data-ttu-id="85852-141">Si se especifican intervalos que tienen el mismo desplazamiento, pero están en orden inverso, se devolverá este error.</span><span class="sxs-lookup"><span data-stu-id="85852-141">If ranges are entered that have the same offset, but are in reverse order, then this error will be returned.</span></span> <span data-ttu-id="85852-142">Por ejemplo, si se escriben 100,5 y 100,0 en ese orden, no podrá agregar el archivo al trabajo.</span><span class="sxs-lookup"><span data-stu-id="85852-142">For example, if 100.5 and 100.0 are entered in that order, then you will not be able to add the file to the job.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="85852-143"><dt><strong>DO_E_INVALID_STATE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="85852-143"><dt><strong>DO_E_INVALID_STATE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="85852-144">El estado del trabajo no puede ser <strong>BG_JOB_STATE_CANCELLED</strong> o <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.</span><span class="sxs-lookup"><span data-stu-id="85852-144">The state of the job cannot be <strong>BG_JOB_STATE_CANCELLED</strong> or <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="85852-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85852-145">Requirements</span></span>



| <span data-ttu-id="85852-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="85852-146">Requirement</span></span> | <span data-ttu-id="85852-147">Value</span><span class="sxs-lookup"><span data-stu-id="85852-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85852-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85852-148">Minimum supported client</span></span><br/> | <span data-ttu-id="85852-149">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="85852-149">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="85852-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85852-150">Minimum supported server</span></span><br/> | <span data-ttu-id="85852-151">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="85852-151">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="85852-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85852-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="85852-153"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="85852-153"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="85852-154">IDL</span><span class="sxs-lookup"><span data-stu-id="85852-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="85852-155"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="85852-155"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="85852-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85852-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="85852-157"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85852-157"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="85852-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="85852-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85852-159"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85852-159"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="85852-160">IID</span><span class="sxs-lookup"><span data-stu-id="85852-160">IID</span></span><br/>                      | <span data-ttu-id="85852-161">IID_IDeliveryOptimizationJob se define como EE2584CF-A69C-4848-B633-2649962B3EF7</span><span class="sxs-lookup"><span data-stu-id="85852-161">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="85852-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="85852-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85852-163">**IDeliveryOptimizationJob**</span><span class="sxs-lookup"><span data-stu-id="85852-163">**IDeliveryOptimizationJob**</span></span>](ideliveryoptimizationjob.md)
</dt> </dl>

 

