---
title: Función DsBackupFree (Ntdsbcli. h)
description: Libera la memoria asignada por las funciones de copia de seguridad y restauración de Active Directory Domain Services.
ms.assetid: cde2a530-60e6-440c-9d4e-a90d55846973
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsBackupFree
topic_type:
- apiref
api_name:
- DsBackupFree
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27855eeb3417eede371357528457248857c3e626
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905182"
---
# <a name="dsbackupfree-function"></a><span data-ttu-id="4711c-104">DsBackupFree función)</span><span class="sxs-lookup"><span data-stu-id="4711c-104">DsBackupFree function</span></span>

<span data-ttu-id="4711c-105">\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="4711c-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4711c-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="4711c-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="4711c-107">A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="4711c-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="4711c-108">La función **DsBackupFree** libera la memoria asignada por las funciones de copia de seguridad y restauración de Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="4711c-108">The **DsBackupFree** function releases memory allocated by the Active Directory Domain Services backup and restore functions.</span></span> <span data-ttu-id="4711c-109">Las siguientes funciones asignan memoria que se debe liberar con la función **DsBackupFree** .</span><span class="sxs-lookup"><span data-stu-id="4711c-109">The following functions allocate memory that must be released with the **DsBackupFree** function.</span></span>

-   [<span data-ttu-id="4711c-110">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="4711c-110">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
-   [<span data-ttu-id="4711c-111">**DsBackupGetDatabaseNames**</span><span class="sxs-lookup"><span data-stu-id="4711c-111">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
-   [<span data-ttu-id="4711c-112">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="4711c-112">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
-   [<span data-ttu-id="4711c-113">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="4711c-113">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)

## <a name="syntax"></a><span data-ttu-id="4711c-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4711c-114">Syntax</span></span>


```C++
VOID NTDSBCLI_API DsBackupFree(
  _In_ PVOID pvBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="4711c-115">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4711c-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4711c-116">*pvBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4711c-116">*pvBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4711c-117">Puntero al búfer de memoria que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="4711c-117">Pointer to the memory buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4711c-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4711c-118">Return value</span></span>

<span data-ttu-id="4711c-119">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4711c-119">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4711c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4711c-120">Requirements</span></span>



| <span data-ttu-id="4711c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4711c-121">Requirement</span></span> | <span data-ttu-id="4711c-122">Value</span><span class="sxs-lookup"><span data-stu-id="4711c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4711c-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4711c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4711c-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4711c-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4711c-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4711c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4711c-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4711c-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4711c-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4711c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4711c-128"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="4711c-128"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="4711c-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4711c-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="4711c-130"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4711c-130"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="4711c-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4711c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4711c-132"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4711c-132"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4711c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="4711c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4711c-134">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="4711c-134">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="4711c-135">**DsBackupGetDatabaseNames**</span><span class="sxs-lookup"><span data-stu-id="4711c-135">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
</dt> <dt>

[<span data-ttu-id="4711c-136">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="4711c-136">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="4711c-137">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="4711c-137">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="4711c-138">Copia de seguridad de un servidor Active Directory</span><span class="sxs-lookup"><span data-stu-id="4711c-138">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="4711c-139">Funciones de copia de seguridad de directorios</span><span class="sxs-lookup"><span data-stu-id="4711c-139">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

