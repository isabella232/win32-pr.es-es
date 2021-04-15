---
title: Función DsBackupPrepare (Ntdsbcli. h)
description: Prepara el directorio en el servidor especificado para la copia de seguridad en línea y devuelve un identificador de contexto de copia de seguridad utilizado en llamadas posteriores a otras funciones de copia de seguridad.
ms.assetid: 18c6dbcf-b707-4674-9af5-40f2178e6d2b
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsBackupPrepare
topic_type:
- apiref
api_name:
- DsBackupPrepare
- DsBackupPrepareA
- DsBackupPrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa561a7e41164ece68fb18fd882a8b05d6357cec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491026"
---
# <a name="dsbackupprepare-function"></a><span data-ttu-id="a3632-104">DsBackupPrepare función)</span><span class="sxs-lookup"><span data-stu-id="a3632-104">DsBackupPrepare function</span></span>

<span data-ttu-id="a3632-105">\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="a3632-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a3632-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="a3632-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a3632-107">A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="a3632-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="a3632-108">La función **DsBackupPrepare** prepara el directorio en el servidor especificado para la copia de seguridad en línea y devuelve un identificador de contexto de copia de seguridad utilizado en llamadas posteriores a otras funciones de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a3632-108">The **DsBackupPrepare** function prepares the directory on the specified server for the online backup and returns a backup context handle used in subsequent calls to other backup functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3632-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3632-109">Syntax</span></span>


```C++
HRESULT DsBackupPrepare(
  _In_  LPCTSTR szBackupServer,
  _In_  ULONG   grbit,
  _In_  ULONG   btBackupType,
  _Out_ PVOID   *ppvExpiryToken,
  _Out_ LPDWORD pcbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a><span data-ttu-id="a3632-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3632-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3632-111">*szBackupServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a3632-111">*szBackupServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3632-112">Puntero a una cadena terminada en null que contiene el nombre del servidor del que se va a realizar la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a3632-112">Pointer to a null-terminated string that contains the name of the server to backup.</span></span> <span data-ttu-id="a3632-113">Las barras diagonales inversas anteriores son opcionales.</span><span class="sxs-lookup"><span data-stu-id="a3632-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="a3632-114">El servidor debe ser el mismo equipo desde el que se llama a esta función.</span><span class="sxs-lookup"><span data-stu-id="a3632-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="a3632-115">El nombre del servidor no puede contener un carácter de subrayado ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="a3632-115">The server name cannot contain an underscore (\_) character.</span></span> <span data-ttu-id="a3632-116">Un ejemplo de un nombre de servidor es " \\ \\ server1".</span><span class="sxs-lookup"><span data-stu-id="a3632-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="a3632-117">*grbit* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a3632-117">*grbit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3632-118">Determina si se realizará una copia de seguridad de los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="a3632-118">Determines if the log files will be backed up.</span></span> <span data-ttu-id="a3632-119">Este valor siempre debe ser 0, ya que no se admiten las copias de seguridad incrementales.</span><span class="sxs-lookup"><span data-stu-id="a3632-119">This value should always be 0 because incremental backups are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a3632-120">*btBackupType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a3632-120">*btBackupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3632-121">Especifica el tipo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a3632-121">Specifies the type of backup.</span></span> <span data-ttu-id="a3632-122">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a3632-122">This can be one of the following values.</span></span>

<dt>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>

<span data-ttu-id="a3632-123"><span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**tipo de copia de seguridad \_ \_ completo**</span><span class="sxs-lookup"><span data-stu-id="a3632-123"><span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**BACKUP\_TYPE\_FULL**</span></span>


</dt> <dd>

<span data-ttu-id="a3632-124">Especifica una copia de seguridad completa.</span><span class="sxs-lookup"><span data-stu-id="a3632-124">Specifies a full backup.</span></span> <span data-ttu-id="a3632-125">Se realiza una copia de seguridad del directorio completo (DIT, archivos de registro y archivos de actualización).</span><span class="sxs-lookup"><span data-stu-id="a3632-125">The complete directory (DIT, log files, and update files) are backed up.</span></span> <span data-ttu-id="a3632-126">Se realiza una copia de seguridad de todos los datos y los archivos de registro de transacciones se truncan.</span><span class="sxs-lookup"><span data-stu-id="a3632-126">All data is backed up and transaction log files are truncated.</span></span> <span data-ttu-id="a3632-127">Solo se admiten copias de seguridad completas.</span><span class="sxs-lookup"><span data-stu-id="a3632-127">Only full backups are supported.</span></span>

</dd> <dt>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>

<span data-ttu-id="a3632-128"><span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**\_ \_ solo registros de tipo de copia de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="a3632-128"><span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**BACKUP\_TYPE\_LOGS\_ONLY**</span></span>


</dt> <dd>

<span data-ttu-id="a3632-129">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="a3632-129">This value is not supported.</span></span> <span data-ttu-id="a3632-130">Especifica que solo se hará una copia de seguridad de los registros de la base de datos, y no de la propia base de datos.</span><span class="sxs-lookup"><span data-stu-id="a3632-130">Specifies that only the database logs, and not the database itself, will be backed up.</span></span> <span data-ttu-id="a3632-131">Normalmente se utiliza cuando se realiza una copia de seguridad diferencial o incremental.</span><span class="sxs-lookup"><span data-stu-id="a3632-131">This is normally used when performing a differential or incremental backup.</span></span>

</dd> <dt>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>

<span data-ttu-id="a3632-132"><span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**tipo de copia de seguridad \_ \_ incremental**</span><span class="sxs-lookup"><span data-stu-id="a3632-132"><span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**BACKUP\_TYPE\_INCREMENTAL**</span></span>


</dt> <dd>

<span data-ttu-id="a3632-133">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="a3632-133">This value is not supported.</span></span> <span data-ttu-id="a3632-134">**DsBackupPrepare** devuelve **un \_ \_ parámetro de error no válido**.</span><span class="sxs-lookup"><span data-stu-id="a3632-134">**DsBackupPrepare** returns **ERROR\_INVALID\_PARAMETER**.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a3632-135">*ppvExpiryToken* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a3632-135">*ppvExpiryToken* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3632-136">Puntero a un valor de **PVOID** que recibe un puntero a un token de expiración asociado a esta copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a3632-136">Pointer to a **PVOID** value that receives a pointer to an expiry token associated with this backup.</span></span> <span data-ttu-id="a3632-137">*pcbExpiryTokenSize* recibe el tamaño, en bytes, de estos datos.</span><span class="sxs-lookup"><span data-stu-id="a3632-137">*pcbExpiryTokenSize* receives the size, in bytes, of this data.</span></span> <span data-ttu-id="a3632-138">El autor de la llamada debe guardar el contenido de este token con la copia de seguridad porque el token se debe pasar a [**DsRestorePrepare**](dsrestoreprepare.md) al intentar restaurar los datos.</span><span class="sxs-lookup"><span data-stu-id="a3632-138">The caller must save the contents of this token with the backup because the token must be passed to [**DsRestorePrepare**](dsrestoreprepare.md) when attempting to restore data.</span></span> <span data-ttu-id="a3632-139">Una vez que el token se ha almacenado y ya no es necesario, el llamador debe liberar la memoria asignada mediante [**DsBackupFree**](dsbackupfree.md).</span><span class="sxs-lookup"><span data-stu-id="a3632-139">After the token has been stored and is no longer required, the caller should free the allocated memory using [**DsBackupFree**](dsbackupfree.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3632-140">*pcbExpiryTokenSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a3632-140">*pcbExpiryTokenSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3632-141">Puntero a un valor **DWORD** que recibe el tamaño, en bytes, del token en *ppvExpiryToken*.</span><span class="sxs-lookup"><span data-stu-id="a3632-141">Pointer to a **DWORD** value that receives the size, in bytes, of the token in *ppvExpiryToken*.</span></span>

</dd> <dt>

<span data-ttu-id="a3632-142">*phbc* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a3632-142">*phbc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3632-143">Puntero a un valor de **HBC** que recibe el identificador de la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a3632-143">Pointer to an **HBC** value that receives the handle for the backup.</span></span> <span data-ttu-id="a3632-144">Este identificador se usa al llamar a otras funciones de copia de seguridad del servicio de directorio, como [**DsBackupOpenFile**](dsbackupopenfile.md) y [**DsBackupEnd**](dsbackupend.md).</span><span class="sxs-lookup"><span data-stu-id="a3632-144">This handle is used when calling other Directory Service backup functions, such as [**DsBackupOpenFile**](dsbackupopenfile.md) and [**DsBackupEnd**](dsbackupend.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3632-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3632-145">Return value</span></span>

<span data-ttu-id="a3632-146">Devuelve **S \_ OK** si la función es correcta o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a3632-146">Returns **S\_OK** if the function is successful or an error code otherwise.</span></span> <span data-ttu-id="a3632-147">En la lista siguiente se enumeran otros códigos de error posibles.</span><span class="sxs-lookup"><span data-stu-id="a3632-147">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="a3632-148">**ERROR de \_ acceso \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="a3632-148">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="a3632-149">El autor de la llamada no dispone de los privilegios de acceso adecuados para llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="a3632-149">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="a3632-150">La función [**DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para establecer las credenciales que se usarán para las funciones de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="a3632-150">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="a3632-151">**ERROR \_ de \_ parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="a3632-151">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="a3632-152">*szBackupServer* o *phbcBackupContext* no son válidos.</span><span class="sxs-lookup"><span data-stu-id="a3632-152">*szBackupServer* or *phbcBackupContext* are not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a3632-153">**ERROR \_ de \_ memoria insuficiente \_**</span><span class="sxs-lookup"><span data-stu-id="a3632-153">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="a3632-154">Error de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="a3632-154">A memory allocation failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="a3632-155">**hrCouldNotConnect**</span><span class="sxs-lookup"><span data-stu-id="a3632-155">**hrCouldNotConnect**</span></span>
</dt> <dd>

<span data-ttu-id="a3632-156">No se encontró el servidor en *szBackupServer* , no es un controlador de dominio o *szBackupServer* no tiene el formato correcto.</span><span class="sxs-lookup"><span data-stu-id="a3632-156">The server in *szBackupServer* could not be found, is not a domain controller or *szBackupServer* is not formatted correctly.</span></span> <span data-ttu-id="a3632-157">Este valor se define en ntdsbmsg. h.</span><span class="sxs-lookup"><span data-stu-id="a3632-157">This value is defined in ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="a3632-158">**hrInvalidParam**</span><span class="sxs-lookup"><span data-stu-id="a3632-158">**hrInvalidParam**</span></span>
</dt> <dd>

<span data-ttu-id="a3632-159">*ppvExpiryToken* y/o *pcbExpiryTokenSize* no son válidos.</span><span class="sxs-lookup"><span data-stu-id="a3632-159">*ppvExpiryToken* and/or *pcbExpiryTokenSize* are invalid.</span></span> <span data-ttu-id="a3632-160">Este valor se define en Ntdsbmsg. h.</span><span class="sxs-lookup"><span data-stu-id="a3632-160">This value is defined in Ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="a3632-161">**enlace de RPC \_ S \_ no válido \_**</span><span class="sxs-lookup"><span data-stu-id="a3632-161">**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd>

<span data-ttu-id="a3632-162">Se llama a la función de forma remota o el servidor de *szServerName* no es un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="a3632-162">The function is called remotely or the server in *szServerName* is not a domain controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3632-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3632-163">Remarks</span></span>

<span data-ttu-id="a3632-164">Esta función requiere que el autor de la llamada tenga el privilegio de **\_ \_ nombre de copia de seguridad** .</span><span class="sxs-lookup"><span data-stu-id="a3632-164">This function requires that the caller has the **SE\_BACKUP\_NAME** privilege.</span></span> <span data-ttu-id="a3632-165">La función [**DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para cambiar el contexto de seguridad en el que se llama a esta función.</span><span class="sxs-lookup"><span data-stu-id="a3632-165">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to change the security context under which this function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3632-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3632-166">Requirements</span></span>



| <span data-ttu-id="a3632-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3632-167">Requirement</span></span> | <span data-ttu-id="a3632-168">Value</span><span class="sxs-lookup"><span data-stu-id="a3632-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3632-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3632-169">Minimum supported client</span></span><br/> | <span data-ttu-id="a3632-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3632-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a3632-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3632-171">Minimum supported server</span></span><br/> | <span data-ttu-id="a3632-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3632-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a3632-173">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3632-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3632-174"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3632-174"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="a3632-175">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a3632-175">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3632-176"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3632-176"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="a3632-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a3632-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3632-178"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3632-178"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="a3632-179">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="a3632-179">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a3632-180">**DsBackupPrepareW** (Unicode) y **DsBackupPrepareA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a3632-180">**DsBackupPrepareW** (Unicode) and **DsBackupPrepareA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a3632-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3632-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3632-182">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="a3632-182">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="a3632-183">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="a3632-183">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="a3632-184">**DsBackupOpenFile**</span><span class="sxs-lookup"><span data-stu-id="a3632-184">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="a3632-185">**DsBackupEnd**</span><span class="sxs-lookup"><span data-stu-id="a3632-185">**DsBackupEnd**</span></span>](dsbackupend.md)
</dt> <dt>

[<span data-ttu-id="a3632-186">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="a3632-186">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="a3632-187">Copia de seguridad de un servidor Active Directory</span><span class="sxs-lookup"><span data-stu-id="a3632-187">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="a3632-188">Funciones de copia de seguridad de directorios</span><span class="sxs-lookup"><span data-stu-id="a3632-188">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

