---
title: Función SisCreateBackupStructure (Sisbkup. h)
description: Crea una estructura de copia de seguridad de SIS basada en la información proporcionada.
ms.assetid: a8c48961-fa24-4eb6-92cd-1b9bc83cec41
keywords:
- Copia de seguridad de la función SisCreateBackupStructure
topic_type:
- apiref
api_name:
- SisCreateBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad432095f9d264e124df1d84070056fc827c625e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489820"
---
# <a name="siscreatebackupstructure-function"></a><span data-ttu-id="209dc-104">SisCreateBackupStructure función)</span><span class="sxs-lookup"><span data-stu-id="209dc-104">SisCreateBackupStructure function</span></span>

<span data-ttu-id="209dc-105">La función **SisCreateBackupStructure** crea una estructura de copia de seguridad de SIS basada en la información proporcionada.</span><span class="sxs-lookup"><span data-stu-id="209dc-105">The **SisCreateBackupStructure** function creates a SIS backup structure based on the supplied information.</span></span>

## <a name="syntax"></a><span data-ttu-id="209dc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="209dc-106">Syntax</span></span>


```C++
BOOL SisCreateBackupStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisBackupStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a><span data-ttu-id="209dc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="209dc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="209dc-108">*volumeRoot* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="209dc-108">*volumeRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="209dc-109">Nombre de archivo de la raíz del volumen, sin la barra diagonal inversa final, del volumen del que se va a realizar la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="209dc-109">File name of the volume root, without the trailing backslash, of the volume to be backed up.</span></span> <span data-ttu-id="209dc-110">Por ejemplo, especifique "C:" y no "C: \\ ".</span><span class="sxs-lookup"><span data-stu-id="209dc-110">For example, specify "C:" and not "C:\\".</span></span>

</dd> <dt>

<span data-ttu-id="209dc-111">*sisBackupStructure* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="209dc-111">*sisBackupStructure* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="209dc-112">Estructura de copia de seguridad de SIS devuelta.</span><span class="sxs-lookup"><span data-stu-id="209dc-112">Returned SIS backup structure.</span></span>

</dd> <dt>

<span data-ttu-id="209dc-113">*commonStoreRootPathname* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="209dc-113">*commonStoreRootPathname* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="209dc-114">Nombre completo de la ruta de acceso del almacén común del volumen especificado.</span><span class="sxs-lookup"><span data-stu-id="209dc-114">Fully qualified path name of the specified volume's common store.</span></span> <span data-ttu-id="209dc-115">Por ejemplo, "c: \\ SIS Common Store".</span><span class="sxs-lookup"><span data-stu-id="209dc-115">For example, "c:\\SIS Common Store".</span></span>

</dd> <dt>

<span data-ttu-id="209dc-116">*countOfCommonStoreFilesToBackUp* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="209dc-116">*countOfCommonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="209dc-117">Número de archivos enumerados en el parámetro *commonStoreFilesToBackUp* .</span><span class="sxs-lookup"><span data-stu-id="209dc-117">Number of files listed in the *commonStoreFilesToBackUp* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="209dc-118">*commonStoreFilesToBackUp* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="209dc-118">*commonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="209dc-119">Puntero a una matriz de nombres de archivo que especifica una lista de archivos internos utilizados por SIS para administrar el volumen especificado.</span><span class="sxs-lookup"><span data-stu-id="209dc-119">Pointer to an array of file names that specifies a list of internal files used by SIS to manage the specified volume.</span></span> <span data-ttu-id="209dc-120">Se debe realizar una copia de seguridad de estos archivos al mismo tiempo y de la misma manera que los archivos de almacenamiento común solicitados por [ **SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)</span><span class="sxs-lookup"><span data-stu-id="209dc-120">These files should be backed up at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="209dc-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="209dc-121">Return value</span></span>

<span data-ttu-id="209dc-122">Esta función devuelve **true** si se completa correctamente y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="209dc-122">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="209dc-123">Llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre la razón por la que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="209dc-123">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="209dc-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="209dc-124">Remarks</span></span>

<span data-ttu-id="209dc-125">Esta función crea una estructura de copia de seguridad de SIS, que usa la API de copia de seguridad de SIS para crear y mantener una lista de los vínculos de archivo en el volumen y los archivos originales a los que apuntan los vínculos.</span><span class="sxs-lookup"><span data-stu-id="209dc-125">This function creates a SIS backup structure, which is used by the SIS backup API to create and maintain a list of the file links on the volume and the original files the links point to.</span></span> <span data-ttu-id="209dc-126">Se debe llamar a esta función solo una vez para cada volumen habilitado para SIS en el que se realiza la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="209dc-126">This function should be called only once for each SIS-enabled volume being backed up.</span></span> <span data-ttu-id="209dc-127">Todos los archivos del volumen especificado deben tratarse como archivos de almacenamiento común y copia de seguridad solo si SIS indica que deben hacerlo.</span><span class="sxs-lookup"><span data-stu-id="209dc-127">All files within the specified volume should be treated as common-store files and backed up only if SIS indicates that they should.</span></span>

<span data-ttu-id="209dc-128">Los parámetros *countOfCommonStoreFilesToBackUp* y *commonStoreFilesToBackUp* devuelven conjuntamente una lista de archivos de los que se debe hacer una copia de seguridad, independientemente de los vínculos de los que se haya realizado una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="209dc-128">The *countOfCommonStoreFilesToBackUp* and *commonStoreFilesToBackUp* parameters together return a list of files that must be backed up regardless of which links are backed up.</span></span>

<span data-ttu-id="209dc-129">Si *countOfCommonStoreFilesToBackUp* es 0, *commonStoreFilesToBackUp* puede ser un puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="209dc-129">If *countOfCommonStoreFilesToBackUp* is 0, *commonStoreFilesToBackUp* may be a **NULL** pointer.</span></span> <span data-ttu-id="209dc-130">Se debe omitir el valor del parámetro *commonStoreFilesToBackUp* .</span><span class="sxs-lookup"><span data-stu-id="209dc-130">The value of the *commonStoreFilesToBackUp* parameter should be ignored.</span></span>

<span data-ttu-id="209dc-131">Una vez completada la operación de copia de seguridad, Desasigne la memoria usada por la matriz de cadenas *commonStoreFilesToBackUp* llamando a [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="209dc-131">After the backup operation is complete, deallocate the memory used by the *commonStoreFilesToBackUp* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="209dc-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="209dc-132">Requirements</span></span>



| <span data-ttu-id="209dc-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="209dc-133">Requirement</span></span> | <span data-ttu-id="209dc-134">Value</span><span class="sxs-lookup"><span data-stu-id="209dc-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="209dc-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="209dc-135">Minimum supported client</span></span><br/> | <span data-ttu-id="209dc-136">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="209dc-136">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="209dc-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="209dc-137">Minimum supported server</span></span><br/> | <span data-ttu-id="209dc-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="209dc-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="209dc-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="209dc-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="209dc-140"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="209dc-140"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="209dc-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="209dc-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="209dc-142"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="209dc-142"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="209dc-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="209dc-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="209dc-144"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="209dc-144"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="209dc-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="209dc-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="209dc-146">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="209dc-146">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="209dc-147">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="209dc-147">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="209dc-148">**SisFreeAllocatedMemory**</span><span class="sxs-lookup"><span data-stu-id="209dc-148">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> </dl>

 

