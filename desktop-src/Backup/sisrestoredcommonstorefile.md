---
title: Función SisRestoredCommonStoreFile (Sisbkup. h)
description: Informa a la arquitectura de SIS de que se ha escrito un archivo de almacenamiento común.
ms.assetid: 2b1cd9e7-a19c-4474-a40a-5a27d4feeab7
keywords:
- Copia de seguridad de la función SisRestoredCommonStoreFile
topic_type:
- apiref
api_name:
- SisRestoredCommonStoreFile
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093ff5f20db42bcafe62ee0ec57d5027abcf9f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996120"
---
# <a name="sisrestoredcommonstorefile-function"></a><span data-ttu-id="8c98e-104">SisRestoredCommonStoreFile función)</span><span class="sxs-lookup"><span data-stu-id="8c98e-104">SisRestoredCommonStoreFile function</span></span>

<span data-ttu-id="8c98e-105">La función **SisRestoredCommonStoreFile** notifica a la arquitectura de SIS que se ha escrito un archivo de almacenamiento común.</span><span class="sxs-lookup"><span data-stu-id="8c98e-105">The **SisRestoredCommonStoreFile** function reports to the SIS architecture that a common-store file has been written.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c98e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c98e-106">Syntax</span></span>


```C++
BOOL SisRestoredCommonStoreFile(
  _In_ PVOID  sisRestoreStructure,
  _In_ PWCHAR commonStoreFileName
);
```



## <a name="parameters"></a><span data-ttu-id="8c98e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c98e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c98e-108">*sisRestoreStructure* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c98e-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c98e-109">Puntero a una estructura de restauración de SIS devuelta desde [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span><span class="sxs-lookup"><span data-stu-id="8c98e-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c98e-110">*commonStoreFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c98e-110">*commonStoreFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c98e-111">Nombre del archivo de almacenamiento común restaurado.</span><span class="sxs-lookup"><span data-stu-id="8c98e-111">Name of the restored common-store file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c98e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c98e-112">Return value</span></span>

<span data-ttu-id="8c98e-113">Esta función devuelve **true** si se completa correctamente y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8c98e-113">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="8c98e-114">Llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre la razón por la que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="8c98e-114">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c98e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c98e-115">Remarks</span></span>

<span data-ttu-id="8c98e-116">Se debe llamar a esta función después de haber restaurado un archivo de almacenamiento común.</span><span class="sxs-lookup"><span data-stu-id="8c98e-116">This function should be called after you have restored a common-store file.</span></span> <span data-ttu-id="8c98e-117">Notifica a la arquitectura de SIS que se ha escrito un nuevo archivo de almacenamiento común, de modo que la arquitectura de SIS puede realizar tareas de mantenimiento internas como la inicialización de sus estructuras de datos internas o la corrección de los vínculos al archivo de almacenamiento común.</span><span class="sxs-lookup"><span data-stu-id="8c98e-117">It notifies the SIS architecture that a new common-store file has been written, so that the SIS architecture can perform internal maintenance tasks such as initializing its internal data structures or fixing the links to the common-store file.</span></span>

<span data-ttu-id="8c98e-118">La operación de restauración solo debe restaurar los archivos de almacenamiento común que notifique [**SisRestoredLink**](sisrestoredlink.md), aunque haya archivos de almacenamiento común adicionales en el medio de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8c98e-118">Your restore operation should restore only common-store files reported by [**SisRestoredLink**](sisrestoredlink.md), even if there are additional common-store files on the backup media.</span></span> <span data-ttu-id="8c98e-119">La operación de restauración puede restaurar los vínculos de SIS y archivos de almacenamiento común en cualquier orden que elija. sin embargo, debe llamar a **SisRestoredLink** después de restaurar cualquier vínculo y debe llamar a esta función después de que se haya restaurado cualquier archivo de almacenamiento común.</span><span class="sxs-lookup"><span data-stu-id="8c98e-119">Your restore operation can restore the SIS links and common-store files in any order it chooses; however, it must call **SisRestoredLink** after it restores any link, and it must call this function after it restores any common-store file.</span></span> <span data-ttu-id="8c98e-120">Dado que la operación de restauración no puede identificar los archivos de almacenamiento común que se restaurarán hasta que se notifiquen los nombres de archivo como resultado de la restauración de un vínculo, la operación de restauración siempre restaurará un archivo de almacenamiento común cuando se restaure al menos un vínculo que hace referencia a él.</span><span class="sxs-lookup"><span data-stu-id="8c98e-120">Because your restore operation cannot identify which common-store files will be restored until the file names are reported to it as a result of restoring a link, your restore operation will always restore a common-store file after at least one link referring to it is restored.</span></span> <span data-ttu-id="8c98e-121">Sin embargo, puede restaurar vínculos de SIS adicionales que apunten a ese archivo de almacenamiento común.</span><span class="sxs-lookup"><span data-stu-id="8c98e-121">However, you can then restore additional SIS links that point to that common-store file.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c98e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c98e-122">Requirements</span></span>



| <span data-ttu-id="8c98e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c98e-123">Requirement</span></span> | <span data-ttu-id="8c98e-124">Value</span><span class="sxs-lookup"><span data-stu-id="8c98e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c98e-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c98e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8c98e-126">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8c98e-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8c98e-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c98e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8c98e-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c98e-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8c98e-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c98e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c98e-130"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c98e-130"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="8c98e-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c98e-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="8c98e-132"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c98e-132"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="8c98e-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c98e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c98e-134"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c98e-134"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c98e-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c98e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c98e-136">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="8c98e-136">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="8c98e-137">**SisRestoredLink**</span><span class="sxs-lookup"><span data-stu-id="8c98e-137">**SisRestoredLink**</span></span>](sisrestoredlink.md)
</dt> </dl>

 

