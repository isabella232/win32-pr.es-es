---
title: Función SisCreateRestoreStructure (Sisbkup. h)
description: Crea una estructura de restauración de SIS basada en la información proporcionada.
ms.assetid: acdd4258-813d-42af-a2e1-e59a1426f86c
keywords:
- Copia de seguridad de la función SisCreateRestoreStructure
topic_type:
- apiref
api_name:
- SisCreateRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b83ebcdd609b00fdec19666a6915926692a2048
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905111"
---
# <a name="siscreaterestorestructure-function"></a><span data-ttu-id="a8c1e-104">SisCreateRestoreStructure función)</span><span class="sxs-lookup"><span data-stu-id="a8c1e-104">SisCreateRestoreStructure function</span></span>

<span data-ttu-id="a8c1e-105">La función **SisCreateRestoreStructure** crea una estructura de restauración de SIS basada en la información proporcionada.</span><span class="sxs-lookup"><span data-stu-id="a8c1e-105">The **SisCreateRestoreStructure** function creates a SIS restore structure based on the supplied information.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8c1e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8c1e-106">Syntax</span></span>


```C++
BOOL SisCreateRestoreStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisRestoreStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a><span data-ttu-id="a8c1e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8c1e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8c1e-108">*volumeRoot* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a8c1e-108">*volumeRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8c1e-109">Nombre de archivo de la raíz del volumen, sin la barra diagonal inversa final, del volumen del que se va a realizar la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a8c1e-109">File name of the volume root, without the trailing backslash, of the volume to be backed up.</span></span> <span data-ttu-id="a8c1e-110">Por ejemplo, especifique "C:" y no "C: \\ ".</span><span class="sxs-lookup"><span data-stu-id="a8c1e-110">For example, specify "C:" and not "C:\\".</span></span> <span data-ttu-id="a8c1e-111">El volumen no puede ser el volumen de sistema o de arranque.</span><span class="sxs-lookup"><span data-stu-id="a8c1e-111">The volume cannot be the system or boot volume.</span></span>

</dd> <dt>

<span data-ttu-id="a8c1e-112">*sisRestoreStructure* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a8c1e-112">*sisRestoreStructure* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8c1e-113">Se devolvió la estructura de restauración de SIS.</span><span class="sxs-lookup"><span data-stu-id="a8c1e-113">Returned SIS restore structure.</span></span> <span data-ttu-id="a8c1e-114">El llamador debe tratar esta estructura como opaca.</span><span class="sxs-lookup"><span data-stu-id="a8c1e-114">This structure should be treated as opaque by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="a8c1e-115">*commonStoreRootPathname* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a8c1e-115">*commonStoreRootPathname* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8c1e-116">Nombre completo de la ruta de acceso del almacén común del volumen especificado.</span><span class="sxs-lookup"><span data-stu-id="a8c1e-116">Fully qualified path name of the specified volume's common store.</span></span> <span data-ttu-id="a8c1e-117">Por ejemplo, "c: \\ SIS Common Store".</span><span class="sxs-lookup"><span data-stu-id="a8c1e-117">For example, "c:\\SIS Common Store".</span></span>

</dd> <dt>

<span data-ttu-id="a8c1e-118">*countOfCommonStoreFilesToRestore* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a8c1e-118">*countOfCommonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8c1e-119">Número de archivos enumerados en el parámetro *commonStoreFilesToRestore* .</span><span class="sxs-lookup"><span data-stu-id="a8c1e-119">Number of files listed in the *commonStoreFilesToRestore* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a8c1e-120">*commonStoreFilesToRestore* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a8c1e-120">*commonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8c1e-121">Puntero a una matriz de nombres de archivo que especifica la lista de archivos internos que SIS usa para administrar el volumen especificado.</span><span class="sxs-lookup"><span data-stu-id="a8c1e-121">Pointer to an array of file names that specifies the list of internal files used by SIS to manage the specified volume.</span></span> <span data-ttu-id="a8c1e-122">Estos archivos deben restaurarse al mismo tiempo y de la misma manera que los archivos de almacenamiento común solicitados por [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span><span class="sxs-lookup"><span data-stu-id="a8c1e-122">These files should be restored at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8c1e-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8c1e-123">Return value</span></span>

<span data-ttu-id="a8c1e-124">Esta función devuelve **true** si se completa correctamente y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a8c1e-124">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="a8c1e-125">Llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre la razón por la que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="a8c1e-125">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8c1e-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8c1e-126">Remarks</span></span>

<span data-ttu-id="a8c1e-127">Esta función establece el entorno de restauración en el volumen especificado en la forma en que [**SisCreateBackupStructure**](siscreatebackupstructure.md) establece el entorno de copia de seguridad en el volumen especificado.</span><span class="sxs-lookup"><span data-stu-id="a8c1e-127">This function establishes the restore environment on the specified volume in the way that [**SisCreateBackupStructure**](siscreatebackupstructure.md) establishes the backup environment on the specified volume.</span></span>

<span data-ttu-id="a8c1e-128">Tenga en cuenta que esta función no identifica necesariamente el archivo o los archivos de almacenamiento común correspondientes a un conjunto de vínculos de SIS en el medio de copia de seguridad si esos archivos de almacenamiento comunes todavía existen en el disco.</span><span class="sxs-lookup"><span data-stu-id="a8c1e-128">Note that this function will not necessarily identify the common-store file or files corresponding to a set of SIS links on the backup media if those common store file or files still exist on disk.</span></span> <span data-ttu-id="a8c1e-129">El contenido de la secuencia de datos de un archivo de almacenamiento común nunca cambia una vez que se crea, por lo que si el archivo ya existe en el disco, no es necesario restaurarlo.</span><span class="sxs-lookup"><span data-stu-id="a8c1e-129">The contents of a common-store file's data stream never change once it is created, so if the file already exists on the disk there is no need to restore it.</span></span>

<span data-ttu-id="a8c1e-130">Los nombres de archivo de almacenamiento común son únicos globalmente para garantizar la integridad de la operación de restauración, incluso si no se produce en el mismo volumen habilitado para SIS al que ha tenido acceso la operación de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a8c1e-130">Common-store file names are globally unique to ensure the integrity of the restore operation even if it does not occur on the same SIS-enabled volume that the backup operation has accessed.</span></span>

<span data-ttu-id="a8c1e-131">Una vez completada la operación de restauración, cancele la asignación de la memoria usada por la matriz de cadenas *commonStoreFilesToRestore* llamando a [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="a8c1e-131">After the restore operation is complete, deallocate the memory used by the *commonStoreFilesToRestore* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8c1e-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8c1e-132">Requirements</span></span>



| <span data-ttu-id="a8c1e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8c1e-133">Requirement</span></span> | <span data-ttu-id="a8c1e-134">Value</span><span class="sxs-lookup"><span data-stu-id="a8c1e-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8c1e-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8c1e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a8c1e-136">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a8c1e-136">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a8c1e-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8c1e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a8c1e-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8c1e-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a8c1e-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8c1e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8c1e-140"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8c1e-140"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8c1e-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8c1e-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="a8c1e-142"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8c1e-142"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="a8c1e-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a8c1e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8c1e-144"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8c1e-144"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8c1e-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8c1e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8c1e-146">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="a8c1e-146">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> <dt>

[<span data-ttu-id="a8c1e-147">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="a8c1e-147">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="a8c1e-148">**SisFreeAllocatedMemory**</span><span class="sxs-lookup"><span data-stu-id="a8c1e-148">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> <dt>

[<span data-ttu-id="a8c1e-149">**SisFreeBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="a8c1e-149">**SisFreeBackupStructure**</span></span>](sisfreebackupstructure.md)
</dt> </dl>

 

