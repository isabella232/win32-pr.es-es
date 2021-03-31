---
title: Función DsBackupGetBackupLogs (Ntdsbcli. h)
description: Obtiene la lista de archivos de registro de los que se debe hacer una copia de seguridad para el contexto de copia de seguridad dado.
ms.assetid: 09b3fdac-41ea-471c-a0dd-54414181f6fe
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsBackupGetBackupLogs
topic_type:
- apiref
api_name:
- DsBackupGetBackupLogs
- DsBackupGetBackupLogsA
- DsBackupGetBackupLogsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a02c5c7234810623a95dea030f0c623cca92293
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996512"
---
# <a name="dsbackupgetbackuplogs-function"></a><span data-ttu-id="1c839-104">DsBackupGetBackupLogs función)</span><span class="sxs-lookup"><span data-stu-id="1c839-104">DsBackupGetBackupLogs function</span></span>

<span data-ttu-id="1c839-105">\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="1c839-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1c839-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="1c839-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1c839-107">A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="1c839-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="1c839-108">La función **DsBackupGetBackupLogs** obtiene la lista de archivos de registro de los que se debe hacer una copia de seguridad para el contexto de copia de seguridad determinado.</span><span class="sxs-lookup"><span data-stu-id="1c839-108">The **DsBackupGetBackupLogs** function obtains the list of log files that must be backed up for the given backup context.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c839-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c839-109">Syntax</span></span>


```C++
HRESULT DsBackupGetBackupLogs(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszBackupLogFiles,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="1c839-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c839-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c839-111">*HBC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1c839-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c839-112">Contiene el identificador de contexto de copia de seguridad obtenido con la función [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="1c839-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="1c839-113">*pszBackupLogFiles* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1c839-113">*pszBackupLogFiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c839-114">Puntero a un puntero de cadena que recibe la lista de nombres de archivo de registro como rutas de acceso UNC.</span><span class="sxs-lookup"><span data-stu-id="1c839-114">Pointer to a string pointer that receives the list of log file names as UNC paths.</span></span> <span data-ttu-id="1c839-115">Inicialice este valor en **null** antes de llamar a **DsBackupGetBackupLogs**.</span><span class="sxs-lookup"><span data-stu-id="1c839-115">Initialize this value to **NULL** before calling **DsBackupGetBackupLogs**.</span></span>

<span data-ttu-id="1c839-116">Esta lista recibe una lista de dos cadenas terminadas en NULL con un valor nulo.</span><span class="sxs-lookup"><span data-stu-id="1c839-116">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="1c839-117">Este búfer se asigna mediante la función **DsBackupGetBackupLogs** y se debe liberar cuando ya no se necesite llamando a la función [**DsBackupFree**](dsbackupfree.md) .</span><span class="sxs-lookup"><span data-stu-id="1c839-117">This buffer is allocated by the **DsBackupGetBackupLogs** function and must be freed when no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="1c839-118">El primer carácter de cada uno de los nombres de archivo contiene una de las [**constantes BFT**](bft-constants.md) que identifica el tipo de nombre.</span><span class="sxs-lookup"><span data-stu-id="1c839-118">The first character of each of the file names contains one of the [**BFT Constants**](bft-constants.md) that identifies the type of name.</span></span>

</dd> <dt>

<span data-ttu-id="1c839-119">*PCB* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1c839-119">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c839-120">Puntero al valor **DWORD** que recibe el tamaño, en bytes, del búfer *pszBackupLogFiles* .</span><span class="sxs-lookup"><span data-stu-id="1c839-120">Pointer to **DWORD** value that receives the size, in bytes, of the *pszBackupLogFiles* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c839-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c839-121">Return value</span></span>

<span data-ttu-id="1c839-122">Devuelve **S \_ OK** si la función es correcta o un código de error de Win32 o RPC en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1c839-122">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="1c839-123">En la lista siguiente se enumeran otros códigos de error posibles.</span><span class="sxs-lookup"><span data-stu-id="1c839-123">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="1c839-124">**ERROR de \_ acceso \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="1c839-124">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="1c839-125">El autor de la llamada no dispone de los privilegios de acceso adecuados para llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="1c839-125">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="1c839-126">La función [**DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para establecer las credenciales que se usarán para las funciones de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="1c839-126">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="1c839-127">**ERROR \_ de \_ parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="1c839-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="1c839-128">*HBC*, *pszBackupLogFiles* o *PCB* no es válido.</span><span class="sxs-lookup"><span data-stu-id="1c839-128">*hbc*, *pszBackupLogFiles*, or *pcbSize* is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="1c839-129">**ERROR \_ de \_ memoria insuficiente \_**</span><span class="sxs-lookup"><span data-stu-id="1c839-129">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="1c839-130">Error de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="1c839-130">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c839-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c839-131">Remarks</span></span>

<span data-ttu-id="1c839-132">La función **DsBackupGetBackupLogs** proporciona una lista de los archivos de registro necesarios para una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1c839-132">The **DsBackupGetBackupLogs** function provides a list of the log files necessary for a backup.</span></span> <span data-ttu-id="1c839-133">Una copia de seguridad completa consta de los archivos de base de datos proporcionados por la función [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) y los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="1c839-133">A full backup consists of the database files provided by the [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) function and the log files.</span></span> <span data-ttu-id="1c839-134">No se admiten copias de seguridad incrementales de servidores de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1c839-134">Incremental backups of Active Directory servers are not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c839-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c839-135">Requirements</span></span>



| <span data-ttu-id="1c839-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c839-136">Requirement</span></span> | <span data-ttu-id="1c839-137">Value</span><span class="sxs-lookup"><span data-stu-id="1c839-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c839-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c839-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1c839-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c839-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1c839-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c839-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1c839-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c839-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1c839-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c839-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c839-143"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c839-143"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c839-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c839-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="1c839-145"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c839-145"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="1c839-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1c839-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c839-147"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c839-147"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="1c839-148">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="1c839-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1c839-149">**DsBackupGetBackupLogsW** (Unicode) y **DsBackupGetBackupLogsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1c839-149">**DsBackupGetBackupLogsW** (Unicode) and **DsBackupGetBackupLogsA** (ANSI)</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="1c839-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c839-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c839-151">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="1c839-151">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="1c839-152">**DsBackupGetDatabaseNames**</span><span class="sxs-lookup"><span data-stu-id="1c839-152">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
</dt> <dt>

[<span data-ttu-id="1c839-153">**Constantes de BFT**</span><span class="sxs-lookup"><span data-stu-id="1c839-153">**BFT Constants**</span></span>](bft-constants.md)
</dt> <dt>

[<span data-ttu-id="1c839-154">Copia de seguridad de un servidor Active Directory</span><span class="sxs-lookup"><span data-stu-id="1c839-154">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="1c839-155">Funciones de copia de seguridad de directorios</span><span class="sxs-lookup"><span data-stu-id="1c839-155">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

