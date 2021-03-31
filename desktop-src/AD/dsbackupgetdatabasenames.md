---
title: Función DsBackupGetDatabaseNames (Ntdsbcli. h)
description: Obtiene la lista de archivos de base de datos de la que se va a realizar una copia de seguridad para el contexto de copia de seguridad determinado.
ms.assetid: ba0447a1-38b0-4c0a-8c63-abaefb5b908f
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsBackupGetDatabaseNames
topic_type:
- apiref
api_name:
- DsBackupGetDatabaseNames
- DsBackupGetDatabaseNamesA
- DsBackupGetDatabaseNamesW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6643b17a85727f6e0df4e8deea9609f73afd1e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491027"
---
# <a name="dsbackupgetdatabasenames-function"></a><span data-ttu-id="ec3e6-104">DsBackupGetDatabaseNames función)</span><span class="sxs-lookup"><span data-stu-id="ec3e6-104">DsBackupGetDatabaseNames function</span></span>

<span data-ttu-id="ec3e6-105">\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ec3e6-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="ec3e6-107">A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="ec3e6-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="ec3e6-108">La función **DsBackupGetDatabaseNames** obtiene la lista de archivos de base de datos de los que se va a realizar una copia de seguridad para el contexto de copia de seguridad determinado.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-108">The **DsBackupGetDatabaseNames** function obtains the list of database files to be backed up for the given backup context.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec3e6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec3e6-109">Syntax</span></span>


```C++
HRESULT DsBackupGetDatabaseNames(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszAttachmentInfo,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="ec3e6-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec3e6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec3e6-111">*HBC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ec3e6-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec3e6-112">Contiene el identificador de contexto de copia de seguridad obtenido con la función [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3e6-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="ec3e6-113">*pszAttachmentInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ec3e6-113">*pszAttachmentInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec3e6-114">Puntero a un puntero de cadena que recibe la lista de nombres de archivo de base de datos como rutas de acceso UNC.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-114">Pointer to a string pointer that receives the list of database file names as UNC paths.</span></span> <span data-ttu-id="ec3e6-115">Este valor se debe inicializar en **null** antes de llamar a **DsBackupGetDatabaseNames**.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-115">This value must be initialized to **NULL** prior to calling **DsBackupGetDatabaseNames**.</span></span>

<span data-ttu-id="ec3e6-116">Esta lista recibe una lista de dos cadenas terminadas en NULL con un valor nulo.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-116">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="ec3e6-117">Este búfer se asigna mediante la función **DsBackupGetDatabaseNames** y se debe liberar cuando ya no es necesario llamando a la función [**DsBackupFree**](dsbackupfree.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3e6-117">This buffer is allocated by the **DsBackupGetDatabaseNames** function and must be freed when it is no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="ec3e6-118">El primer carácter de cada nombre de archivo contiene una de las [**constantes BFT**](bft-constants.md) que identifica el tipo de nombre.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-118">The first character of each file name contains one of the [**BFT Constants**](bft-constants.md) that identifies the type of name.</span></span> <span data-ttu-id="ec3e6-119">La función [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) solo proporciona los siguientes tipos de nombres.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-119">The [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function only supplies the following types of names.</span></span>

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span data-ttu-id="ec3e6-120"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_base de \_ datos Ntds BFT**</span><span class="sxs-lookup"><span data-stu-id="ec3e6-120"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>


</dt> <dd>

<span data-ttu-id="ec3e6-121">El archivo es un archivo de base de datos NTDS.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-121">The file is an NTDS database file.</span></span> <span data-ttu-id="ec3e6-122">Este archivo debe copiarse en el archivo identificado como **BFT \_ NTDS \_ Database** cuando se restauren los datos.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-122">This file should be copied to the file identified as **BFT\_NTDS\_DATABASE** when the data is restored.</span></span>

</dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>

<span data-ttu-id="ec3e6-123"><span id="BFT_LOG"></span><span id="bft_log"></span>**registro de BFT \_**</span><span class="sxs-lookup"><span data-stu-id="ec3e6-123"><span id="BFT_LOG"></span><span id="bft_log"></span>**BFT\_LOG**</span></span>


</dt> <dd>

<span data-ttu-id="ec3e6-124">El archivo es un archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-124">The file is a log file.</span></span> <span data-ttu-id="ec3e6-125">Todos los archivos de registro se copian en el directorio identificado como **BFT de \_ registro de inicio de sesión \_** cuando se restauran los datos.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-125">All log files are copied to the directory identified as **BFT\_LOG\_DIR** when the data is restored.</span></span>

</dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>

<span data-ttu-id="ec3e6-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**\_archivo de revisión BFT \_**</span><span class="sxs-lookup"><span data-stu-id="ec3e6-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT\_PATCH\_FILE**</span></span>


</dt> <dd>

<span data-ttu-id="ec3e6-127">El archivo es un archivo de revisión.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-127">The file is a patch file.</span></span> <span data-ttu-id="ec3e6-128">Todos los archivos de revisión se copian en el directorio identificado como **BFT \_ Checkpoint \_ dir** cuando se restauran los datos.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-128">All patch files are copied to the directory identified as **BFT\_CHECKPOINT\_DIR** when the data is restored.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ec3e6-129">*PCB* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ec3e6-129">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec3e6-130">Puntero al valor **DWORD** que recibe el tamaño, en bytes, del búfer *pszAttachmentInfo* .</span><span class="sxs-lookup"><span data-stu-id="ec3e6-130">Pointer to **DWORD** value that receives the size, in bytes, of the *pszAttachmentInfo* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec3e6-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec3e6-131">Return value</span></span>

<span data-ttu-id="ec3e6-132">Devuelve **S \_ OK** si la función es correcta o un código de error de Win32 o RPC en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-132">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="ec3e6-133">En la lista siguiente se enumeran otros códigos de error posibles.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-133">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="ec3e6-134">**ERROR de \_ acceso \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="ec3e6-134">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="ec3e6-135">El autor de la llamada no dispone de los privilegios de acceso adecuados para llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-135">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="ec3e6-136">La función [**DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para establecer las credenciales que se usarán para las funciones de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-136">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="ec3e6-137">**ERROR \_ de \_ parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="ec3e6-137">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="ec3e6-138">*HBC*, *pszAttachmentInfo* o *PCB* no son válidos.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-138">*hbc*, *pszAttachmentInfo*, or *pcbSize* are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="ec3e6-139">**ERROR \_ de \_ memoria insuficiente \_**</span><span class="sxs-lookup"><span data-stu-id="ec3e6-139">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="ec3e6-140">Error de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-140">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec3e6-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ec3e6-141">Remarks</span></span>

<span data-ttu-id="ec3e6-142">La función **DsBackupGetDatabaseNames** proporciona una lista de los archivos de base de datos necesarios para una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-142">The **DsBackupGetDatabaseNames** function provides a list of the database files necessary for a backup.</span></span> <span data-ttu-id="ec3e6-143">Una copia de seguridad completa consta de los archivos de base de datos y los archivos de registro proporcionados por la función [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3e6-143">A full backup consists of the database files and the log files provided by the [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) function.</span></span> <span data-ttu-id="ec3e6-144">No se admiten copias de seguridad incrementales de servidores de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-144">Incremental backups of Active Directory servers are not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec3e6-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec3e6-145">Requirements</span></span>



| <span data-ttu-id="ec3e6-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec3e6-146">Requirement</span></span> | <span data-ttu-id="ec3e6-147">Value</span><span class="sxs-lookup"><span data-stu-id="ec3e6-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec3e6-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec3e6-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ec3e6-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec3e6-149">Windows Vista</span></span><br/>                                                                    |
| <span data-ttu-id="ec3e6-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec3e6-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ec3e6-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec3e6-151">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="ec3e6-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec3e6-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec3e6-153"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec3e6-153"><dt>Ntdsbcli.h</dt></span></span> </dl>       |
| <span data-ttu-id="ec3e6-154">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ec3e6-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="ec3e6-155"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec3e6-155"><dt>Ntdsbcli.lib</dt></span></span> </dl>     |
| <span data-ttu-id="ec3e6-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ec3e6-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec3e6-157"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec3e6-157"><dt>Ntdsbcli.dll</dt></span></span> </dl>     |
| <span data-ttu-id="ec3e6-158">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="ec3e6-158">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ec3e6-159">**DsBackupGetDatabaseNamesW** (Unicode) y **DsBackupGetDatabaseNamesA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ec3e6-159">**DsBackupGetDatabaseNamesW** (Unicode) and **DsBackupGetDatabaseNamesA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ec3e6-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec3e6-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec3e6-161">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="ec3e6-161">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="ec3e6-162">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="ec3e6-162">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="ec3e6-163">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="ec3e6-163">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="ec3e6-164">**Constantes de BFT**</span><span class="sxs-lookup"><span data-stu-id="ec3e6-164">**BFT Constants**</span></span>](bft-constants.md)
</dt> <dt>

[<span data-ttu-id="ec3e6-165">Copia de seguridad de un servidor Active Directory</span><span class="sxs-lookup"><span data-stu-id="ec3e6-165">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="ec3e6-166">Funciones de copia de seguridad de directorios</span><span class="sxs-lookup"><span data-stu-id="ec3e6-166">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

