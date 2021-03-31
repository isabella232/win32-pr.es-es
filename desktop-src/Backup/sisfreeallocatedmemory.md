---
title: Función SisFreeAllocatedMemory (Sisbkup. h)
description: Libera memoria asignada por las funciones de la API de SIS.
ms.assetid: 8fab79c8-593c-46df-a885-09a59620a977
keywords:
- Copia de seguridad de la función SisFreeAllocatedMemory
topic_type:
- apiref
api_name:
- SisFreeAllocatedMemory
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724970817b89f6a9f2490b0776775f6a3a4e69ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905110"
---
# <a name="sisfreeallocatedmemory-function"></a><span data-ttu-id="d7cc1-104">SisFreeAllocatedMemory función)</span><span class="sxs-lookup"><span data-stu-id="d7cc1-104">SisFreeAllocatedMemory function</span></span>

<span data-ttu-id="d7cc1-105">La función **SisFreeAllocatedMemory** libera memoria asignada por las funciones de la API de SIS.</span><span class="sxs-lookup"><span data-stu-id="d7cc1-105">The **SisFreeAllocatedMemory** function frees memory allocated by SIS API functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7cc1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7cc1-106">Syntax</span></span>


```C++
void SisFreeAllocatedMemory(
  _In_ PVOID allocatedSpace
);
```



## <a name="parameters"></a><span data-ttu-id="d7cc1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7cc1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7cc1-108">*allocatedSpace* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7cc1-108">*allocatedSpace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7cc1-109">Puntero a la memoria asignada por la API de SIS.</span><span class="sxs-lookup"><span data-stu-id="d7cc1-109">Pointer to the memory allocated by the SIS API.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7cc1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7cc1-110">Return value</span></span>

<span data-ttu-id="d7cc1-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d7cc1-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7cc1-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7cc1-112">Remarks</span></span>

<span data-ttu-id="d7cc1-113">Una vez completada la llamada a esta función, es posible que el llamador ya no tenga acceso a la memoria liberada.</span><span class="sxs-lookup"><span data-stu-id="d7cc1-113">After the call to this function completes, the caller may no longer access the freed memory.</span></span>

<span data-ttu-id="d7cc1-114">Esta llamada debe usarse para desasignar la memoria asignada para las cadenas de parámetros de *commonStoreRootPathname* devueltas desde [**SisCreateBackupStructure**](siscreatebackupstructure.md) y [**SisCreateRestoreStructure**](siscreaterestorestructure.md), y la matriz de cadenas que contienen los nombres de archivo de almacenamiento común devueltos por **SisCreateBackupStructure**, [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md), **SisCreateRestoreStructure** y [**SisRestoredLink**](sisrestoredlink.md).</span><span class="sxs-lookup"><span data-stu-id="d7cc1-114">This call should be used to deallocate the memory allocated for the *commonStoreRootPathname* parameter strings returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md) and [**SisCreateRestoreStructure**](siscreaterestorestructure.md), and the array of strings containing common-store file names returned from **SisCreateBackupStructure**, [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md), **SisCreateRestoreStructure**, and [**SisRestoredLink**](sisrestoredlink.md).</span></span> <span data-ttu-id="d7cc1-115">En el último caso, la propia matriz también se debe liberar llamando a **SisFreeAllocatedMemory**.</span><span class="sxs-lookup"><span data-stu-id="d7cc1-115">In the latter case, the array itself also must be freed by calling **SisFreeAllocatedMemory**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7cc1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7cc1-116">Requirements</span></span>



| <span data-ttu-id="d7cc1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7cc1-117">Requirement</span></span> | <span data-ttu-id="d7cc1-118">Value</span><span class="sxs-lookup"><span data-stu-id="d7cc1-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7cc1-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7cc1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d7cc1-120">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d7cc1-120">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d7cc1-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7cc1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d7cc1-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7cc1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d7cc1-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7cc1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7cc1-124"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7cc1-124"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7cc1-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7cc1-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7cc1-126"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7cc1-126"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="d7cc1-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d7cc1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7cc1-128"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7cc1-128"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7cc1-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7cc1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7cc1-130">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="d7cc1-130">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> <dt>

[<span data-ttu-id="d7cc1-131">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="d7cc1-131">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="d7cc1-132">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="d7cc1-132">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="d7cc1-133">**SisRestoredLink**</span><span class="sxs-lookup"><span data-stu-id="d7cc1-133">**SisRestoredLink**</span></span>](sisrestoredlink.md)
</dt> </dl>

 

 





