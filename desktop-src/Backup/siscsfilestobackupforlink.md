---
title: Función SisCSFilesToBackupForLink (Sisbkup. h)
description: Devuelve información que describe los archivos de almacenamiento común a los que apunta el vínculo SIS especificado.
ms.assetid: 0580c34e-195a-4a2c-893f-bc339dcc88d7
keywords:
- Copia de seguridad de la función SisCSFilesToBackupForLink
topic_type:
- apiref
api_name:
- SisCSFilesToBackupForLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27d4f52728d662f43efed85d662874bd4b008947
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656501"
---
# <a name="siscsfilestobackupforlink-function"></a><span data-ttu-id="497f5-104">SisCSFilesToBackupForLink función)</span><span class="sxs-lookup"><span data-stu-id="497f5-104">SisCSFilesToBackupForLink function</span></span>

<span data-ttu-id="497f5-105">La función **SisCSFilesToBackupForLink** devuelve información que describe los archivos de almacenamiento común a los que apunta el vínculo SIS especificado.</span><span class="sxs-lookup"><span data-stu-id="497f5-105">The **SisCSFilesToBackupForLink** function returns information describing the common-store files the specified SIS link points to.</span></span>

## <a name="syntax"></a><span data-ttu-id="497f5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="497f5-106">Syntax</span></span>


```C++
BOOL SisCSFilesToBackupForLink(
  _In_  PVOID  sisBackupStructure,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PVOID  thisFileContext,
  _Out_ PVOID  *matchingFileContext,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a><span data-ttu-id="497f5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="497f5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="497f5-108">*sisBackupStructure* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="497f5-108">*sisBackupStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="497f5-109">Puntero a la estructura de copia de seguridad de SIS devuelta desde [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span><span class="sxs-lookup"><span data-stu-id="497f5-109">Pointer to the SIS backup structure returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="497f5-110">*reparseData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="497f5-110">*reparseData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="497f5-111">Puntero al contenido del punto de análisis de SIS.</span><span class="sxs-lookup"><span data-stu-id="497f5-111">Pointer to the contents of the SIS reparse point.</span></span> <span data-ttu-id="497f5-112">Este punto de reanálisis contiene datos que describen un vínculo de SIS.</span><span class="sxs-lookup"><span data-stu-id="497f5-112">This reparse point contains data describing a SIS link.</span></span> <span data-ttu-id="497f5-113">Para recuperar los datos del punto de reanálisis para un archivo, use el código de control de [**\_ \_ \_ punto de reanálisis de FSCTL**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) .</span><span class="sxs-lookup"><span data-stu-id="497f5-113">To retrieve the reparse point data for a file, use the [**FSCTL\_GET\_REPARSE\_POINT**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) control code.</span></span>

</dd> <dt>

<span data-ttu-id="497f5-114">*reparseDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="497f5-114">*reparseDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="497f5-115">Tamaño del contenido del punto de análisis de SIS al que apunta *reparseData*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="497f5-115">Size of the contents of the SIS reparse point pointed to by *reparseData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="497f5-116">*thisFileContext* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="497f5-116">*thisFileContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="497f5-117">Puntero a una cadena de contexto proporcionada por la aplicación de copia de seguridad que llama a esta función.</span><span class="sxs-lookup"><span data-stu-id="497f5-117">Pointer to a context string supplied by the backup application calling this function.</span></span> <span data-ttu-id="497f5-118">El contenido de esta cadena de contenido viene determinado por esta aplicación de copia de seguridad y la API de copia de seguridad de SIS no la interpreta.</span><span class="sxs-lookup"><span data-stu-id="497f5-118">The contents of this content string are entirely determined by this backup application and is not interpreted by the SIS Backup API.</span></span> <span data-ttu-id="497f5-119">Este parámetro es opcional; Si no se usa, establezca el valor de este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="497f5-119">This parameter is optional; if not used, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="497f5-120">En este caso, el valor de este parámetro no se procesará.</span><span class="sxs-lookup"><span data-stu-id="497f5-120">The value of this parameter will not be processed in this case.</span></span>

</dd> <dt>

<span data-ttu-id="497f5-121">*matchingFileContext* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="497f5-121">*matchingFileContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="497f5-122">Puntero de doble indirecto a la cadena de contexto del vínculo SIS identificada por la información pasada en los cuatro primeros parámetros de esta función.</span><span class="sxs-lookup"><span data-stu-id="497f5-122">Doubly-indirect pointer to the context string of the SIS link identified by the information passed in the first four parameters of this function.</span></span> <span data-ttu-id="497f5-123">Este parámetro es opcional; Si no se proporciona una cadena de contexto como valor del parámetro *thisFileContext* , establezca el valor de este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="497f5-123">This parameter is optional; if a context string is not provided as the value of the *thisFileContext* parameter, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="497f5-124">En este caso, el valor de este parámetro no se procesará.</span><span class="sxs-lookup"><span data-stu-id="497f5-124">The value of this parameter will not be processed in this case.</span></span>

</dd> <dt>

<span data-ttu-id="497f5-125">*countOfCommonStoreFilesToBackUp* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="497f5-125">*countOfCommonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="497f5-126">Número de archivos enumerados en el parámetro *commonStoreFilesToBackUp* .</span><span class="sxs-lookup"><span data-stu-id="497f5-126">Number of files listed in the *commonStoreFilesToBackUp* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="497f5-127">*commonStoreFilesToBackUp* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="497f5-127">*commonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="497f5-128">Puntero a una matriz de nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="497f5-128">Pointer to an array of file names.</span></span> <span data-ttu-id="497f5-129">Se debe realizar una copia de seguridad de estos archivos al mismo tiempo y de la misma manera que los archivos de almacenamiento común solicitados por [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span><span class="sxs-lookup"><span data-stu-id="497f5-129">These files should be backed up at the same time and in the same manner as the common-store files requested by [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="497f5-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="497f5-130">Return value</span></span>

<span data-ttu-id="497f5-131">Esta función devuelve **true** si se completa correctamente y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="497f5-131">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="497f5-132">Llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre la razón por la que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="497f5-132">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="497f5-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="497f5-133">Remarks</span></span>

<span data-ttu-id="497f5-134">La aplicación de copia de seguridad debe llamar a esta función solo una vez para cada archivo de vínculo SIS del que se realiza la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="497f5-134">The backup application should call this function only once for each SIS link file being backed up.</span></span>

<span data-ttu-id="497f5-135">La aplicación de copia de seguridad puede identificar un punto de análisis de SIS mediante su etiqueta, la etiqueta de reanálisis de e/s \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="497f5-135">The backup application can identify a SIS reparse point by its tag, IO\_REPARSE\_TAG\_SIS.</span></span> <span data-ttu-id="497f5-136">Esta etiqueta se define en Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="497f5-136">This tag is defined in Winnt.h.</span></span>

<span data-ttu-id="497f5-137">Si este punto de análisis identificado por el valor del parámetro *reparseData* describe la primera instancia de un archivo del que se va a hacer una copia de seguridad, esta función devolverá **null** como el valor del parámetro *matchingFileContext* e inicializará el valor de la matriz *commonStoreFilesToBackUp* de cadenas con los nombres del archivo o archivos de almacenamiento común que se van a incluir en la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="497f5-137">If this reparse point identified by the value of the *reparseData* parameter describes the first instance of a file to be backed up, this function will return **NULL** as the value of the *matchingFileContext* parameter, and initialize the value of the *commonStoreFilesToBackUp* array of strings with the names of the common-store file or files to be backed up.</span></span> <span data-ttu-id="497f5-138">De lo contrario, esta función establecerá el valor del parámetro *matchingFileContext* en la cadena de contexto correspondiente a la primera instancia del archivo especificado y establecerá el valor del parámetro *countOfCommonStoreFilesToBackUp* en 0.</span><span class="sxs-lookup"><span data-stu-id="497f5-138">Otherwise, this function will set the value of the *matchingFileContext* parameter to the context string corresponding to the first instance of the specified file and set the value of the *countOfCommonStoreFilesToBackUp* parameter to 0.</span></span> <span data-ttu-id="497f5-139">Si hay varios archivos de almacenamiento común correspondientes al vínculo especificado, el valor del parámetro *thisFileContext* será la cadena de contexto correspondiente al primer archivo de almacenamiento común devuelto en la matriz, es decir, commonStoreFilesToBackUp \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="497f5-139">If there are multiple common-store files corresponding to the specified link, the value of the *thisFileContext* parameter will be the context string corresponding to the first common-store file returned in the array that is, commonStoreFilesToBackUp\[0\].</span></span>

<span data-ttu-id="497f5-140">La versión actual de esta función devolverá como máximo un archivo de almacenamiento común, pero es posible que en versiones futuras un solo vínculo esté respaldado por varios archivos de almacenamiento común, por ejemplo, uno para cada flujo del archivo, por lo que la aplicación de copia de seguridad debe admitir varios archivos en cada llamada a esta función.</span><span class="sxs-lookup"><span data-stu-id="497f5-140">The current version of this function will return at most one common-store file, but it is possible that in future versions a single link may be backed by several common-store files for example, one for each stream in the file so your backup application should support multiple files in each call to this function.</span></span> <span data-ttu-id="497f5-141">En cualquier caso, cada archivo de almacenamiento común se devolverá una vez por cada paso de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="497f5-141">In any case, each common-store file will be returned at most once for each backup pass.</span></span>

<span data-ttu-id="497f5-142">La aplicación de copia de seguridad debe realizar una copia de seguridad o restaurar el archivo o los archivos de almacenamiento común identificados por el nombre de archivo o los nombres de archivo devueltos en el parámetro *commonStoreFilesToBackUp* .</span><span class="sxs-lookup"><span data-stu-id="497f5-142">Your backup application should back up or restore the common-store file or files identified by the file name or file names returned in the *commonStoreFilesToBackUp* parameter.</span></span> <span data-ttu-id="497f5-143">Independientemente de si hay un archivo de almacenamiento común correspondiente, la aplicación de copia de seguridad debe hacer una copia de seguridad del archivo de vínculo SIS tal como existe en el disco, por ejemplo, como un punto de reanálisis y un archivo disperso, y lo más probable es que no haya ningún rango rellenado.</span><span class="sxs-lookup"><span data-stu-id="497f5-143">Regardless of whether there is a corresponding common-store file, your backup application should back up the SIS link file as it exists on the disk for example, as a reparse point and a sparse file, and most likely with no ranges filled in.</span></span> <span data-ttu-id="497f5-144">La aplicación de copia de seguridad puede hacer una copia de seguridad o restaurar el archivo o los archivos de almacenamiento común inmediatamente, posponer las copias de seguridad o combinarlos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="497f5-144">Your backup application may back up or restore the common-store file or files immediately, postpone backing them up, or mix them together as necessary.</span></span>

<span data-ttu-id="497f5-145">Una vez completada la operación de copia de seguridad, Desasigne la memoria usada por la matriz de cadenas *commonStoreFilesToBackUp* llamando a [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="497f5-145">After the backup operation is complete, deallocate the memory used by the *commonStoreFilesToBackUp* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="497f5-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="497f5-146">Requirements</span></span>



| <span data-ttu-id="497f5-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="497f5-147">Requirement</span></span> | <span data-ttu-id="497f5-148">Value</span><span class="sxs-lookup"><span data-stu-id="497f5-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="497f5-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="497f5-149">Minimum supported client</span></span><br/> | <span data-ttu-id="497f5-150">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="497f5-150">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="497f5-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="497f5-151">Minimum supported server</span></span><br/> | <span data-ttu-id="497f5-152">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="497f5-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="497f5-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="497f5-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="497f5-154"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="497f5-154"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="497f5-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="497f5-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="497f5-156"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="497f5-156"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="497f5-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="497f5-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="497f5-158"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="497f5-158"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="497f5-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="497f5-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="497f5-160">**SisFreeAllocatedMemory**</span><span class="sxs-lookup"><span data-stu-id="497f5-160">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> <dt>

[<span data-ttu-id="497f5-161">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="497f5-161">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> </dl>

 

