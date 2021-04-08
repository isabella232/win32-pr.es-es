---
title: Función SisRestoredLink (Sisbkup. h)
description: Devuelve los nombres de los archivos de almacenamiento común a los que apunta el vínculo SIS restaurado especificado.
ms.assetid: 4eefd975-6055-44c0-93ab-900638948f3e
keywords:
- Copia de seguridad de la función SisRestoredLink
topic_type:
- apiref
api_name:
- SisRestoredLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd539d1ad6c203441b2bcd469a7d8f2fe8bdfc7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996119"
---
# <a name="sisrestoredlink-function"></a><span data-ttu-id="7111b-104">SisRestoredLink función)</span><span class="sxs-lookup"><span data-stu-id="7111b-104">SisRestoredLink function</span></span>

<span data-ttu-id="7111b-105">La función **SisRestoredLink** devuelve los nombres de los archivos de almacenamiento común a los que apunta el vínculo SIS restaurado especificado.</span><span class="sxs-lookup"><span data-stu-id="7111b-105">The **SisRestoredLink** function returns the names of the common-store file or files pointed to by the specified restored SIS link.</span></span>

## <a name="syntax"></a><span data-ttu-id="7111b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7111b-106">Syntax</span></span>


```C++
BOOL SisRestoredLink(
  _In_  PVOID  sisRestoreStructure,
  _In_  PWCHAR restoredFileName,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a><span data-ttu-id="7111b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7111b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7111b-108">*sisRestoreStructure* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7111b-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7111b-109">Puntero a una estructura de restauración de SIS devuelta desde [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span><span class="sxs-lookup"><span data-stu-id="7111b-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="7111b-110">*restoredFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7111b-110">*restoredFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7111b-111">Nombre de archivo completo del archivo de vínculo SIS restaurado.</span><span class="sxs-lookup"><span data-stu-id="7111b-111">Fully qualified file name of the restored SIS link file.</span></span>

</dd> <dt>

<span data-ttu-id="7111b-112">*reparseData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7111b-112">*reparseData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7111b-113">Puntero al contenido del punto de análisis de SIS.</span><span class="sxs-lookup"><span data-stu-id="7111b-113">Pointer to the contents of the SIS reparse point.</span></span> <span data-ttu-id="7111b-114">Este punto de reanálisis contiene datos que describen el vínculo SIS restaurado.</span><span class="sxs-lookup"><span data-stu-id="7111b-114">This reparse point contains data describing the restored SIS link.</span></span> <span data-ttu-id="7111b-115">Para recuperar los datos del punto de reanálisis para un archivo, use el código de control de [**\_ \_ \_ punto de reanálisis de FSCTL**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) .</span><span class="sxs-lookup"><span data-stu-id="7111b-115">To retrieve the reparse point data for a file, use the [**FSCTL\_GET\_REPARSE\_POINT**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) control code.</span></span>

</dd> <dt>

<span data-ttu-id="7111b-116">*reparseDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7111b-116">*reparseDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7111b-117">Tamaño del contenido del punto de análisis de SIS al que apunta *reparseData*, en bytes.</span><span class="sxs-lookup"><span data-stu-id="7111b-117">Size of the contents of the SIS reparse point pointed to by *reparseData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7111b-118">*countOfCommonStoreFilesToRestore* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7111b-118">*countOfCommonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7111b-119">Número de archivos enumerados en el parámetro *commonStoreFilesToRestore* .</span><span class="sxs-lookup"><span data-stu-id="7111b-119">Number of files listed in the *commonStoreFilesToRestore* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7111b-120">*commonStoreFilesToRestore* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7111b-120">*commonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7111b-121">Puntero a una matriz de nombres de archivo de almacenamiento común.</span><span class="sxs-lookup"><span data-stu-id="7111b-121">Pointer to an array of common-store file names.</span></span> <span data-ttu-id="7111b-122">Estos archivos deben restaurarse al mismo tiempo y de la misma manera que los archivos de almacenamiento común solicitados por [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span><span class="sxs-lookup"><span data-stu-id="7111b-122">These files should be restored at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span></span>

<span data-ttu-id="7111b-123">Si el valor del parámetro *countOfCommonStoreFilesToRestore* no es 0, el valor del parámetro *commonStoreFilesToRestore* contendrá los nombres de los archivos de almacenamiento común que se restaurarán como resultado de la restauración del vínculo SIS.</span><span class="sxs-lookup"><span data-stu-id="7111b-123">If the value of the *countOfCommonStoreFilesToRestore* parameter is not 0, the value of the *commonStoreFilesToRestore* parameter will contain the names of the common-store files to be restored as a result of restoring the SIS link.</span></span> <span data-ttu-id="7111b-124">Si el valor es 0, se devuelven los archivos de almacenamiento común una vez o ya están presentes en el volumen.</span><span class="sxs-lookup"><span data-stu-id="7111b-124">If the value is 0, then either the common-store files have been returned once, or they are already present on the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7111b-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7111b-125">Return value</span></span>

<span data-ttu-id="7111b-126">Esta función devuelve **true** si se completa correctamente y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7111b-126">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="7111b-127">Llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre la razón por la que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="7111b-127">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="7111b-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7111b-128">Remarks</span></span>

<span data-ttu-id="7111b-129">Debe llamar a esta función para cada vínculo SIS que se haya restaurado.</span><span class="sxs-lookup"><span data-stu-id="7111b-129">You should call this function for each SIS link that has been restored.</span></span>

<span data-ttu-id="7111b-130">Esta función devolverá cada archivo de almacenamiento común como máximo una vez por cada operación de restauración. cualquier intento de restaurar vínculos de SIS adicionales que ven el mismo archivo de almacenamiento común no dará como resultado que se devuelva el nombre de archivo de almacenamiento común.</span><span class="sxs-lookup"><span data-stu-id="7111b-130">This function will return each common-store file at most once for each restore operation; any attempt to restore additional SIS links that see the same common-store file will not result in that common-store file name being returned.</span></span>

<span data-ttu-id="7111b-131">Esta función no devolverá un archivo de almacenamiento común que no se devolvió también en una llamada a [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) durante la operación de copia de seguridad, suponiendo que los datos de análisis de SIS almacenados en el medio no se han dañado.</span><span class="sxs-lookup"><span data-stu-id="7111b-131">This function will not return a common-store file that was not also returned in a call to [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) during the backup operation, assuming that the SIS reparse data stored on the media has not been corrupted.</span></span>

<span data-ttu-id="7111b-132">Al restaurar un vínculo de SIS, la operación de restauración solo debe crear el archivo disperso adecuado, inicializar los intervalos asignados y, a continuación, escribir los datos de reanálisis de SIS exactamente como se leyeron durante la operación de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7111b-132">When restoring a SIS link, your restore operation should create only the appropriate sparse file, initialize any allocated ranges, and then write the SIS reparse data exactly as it was read during the backup operation.</span></span> <span data-ttu-id="7111b-133">Es fundamental que la operación de restauración cree archivos dispersos con intervalos sin asignar en lugar de archivos dispersos (o archivos no dispersos) inicializados con ceros.</span><span class="sxs-lookup"><span data-stu-id="7111b-133">It is crucial that your restore operation create sparse files with unallocated ranges rather than sparse files (or nonsparse files) initialized with zeroes.</span></span>

<span data-ttu-id="7111b-134">Tenga en cuenta que esta función no identificará necesariamente el archivo o los archivos de almacenamiento común correspondientes a un conjunto de vínculos de SIS en el medio de copia de seguridad si todavía existen en el disco.</span><span class="sxs-lookup"><span data-stu-id="7111b-134">Note that this function will not necessarily identify the common-store file or files corresponding to a set of SIS links on the backup media if those common-store file or files still exist on disk.</span></span> <span data-ttu-id="7111b-135">El contenido de un flujo de datos de un archivo de almacenamiento común nunca cambia una vez que se crea, por lo que si el archivo ya existe en el disco, no es necesario restaurarlo.</span><span class="sxs-lookup"><span data-stu-id="7111b-135">The contents of a common-store file's data stream never changes once it is created, so if the file already exists on the disk there is no need to restore it.</span></span>

<span data-ttu-id="7111b-136">Los nombres de archivo de almacenamiento común son únicos globalmente para garantizar la integridad de la operación de restauración, incluso si no se produce en el mismo volumen habilitado para SIS al que ha tenido acceso la operación de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7111b-136">Common-store file names are globally unique to ensure the integrity of the restore operation even if it does not occur on the same SIS-enabled volume that the backup operation has accessed.</span></span>

## <a name="requirements"></a><span data-ttu-id="7111b-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7111b-137">Requirements</span></span>



| <span data-ttu-id="7111b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="7111b-138">Requirement</span></span> | <span data-ttu-id="7111b-139">Value</span><span class="sxs-lookup"><span data-stu-id="7111b-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7111b-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7111b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="7111b-141">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7111b-141">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7111b-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7111b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="7111b-143">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7111b-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7111b-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7111b-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="7111b-145"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="7111b-145"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="7111b-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7111b-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="7111b-147"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7111b-147"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="7111b-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7111b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7111b-149"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7111b-149"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7111b-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="7111b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7111b-151">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="7111b-151">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="7111b-152">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="7111b-152">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> </dl>

 

