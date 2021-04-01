---
title: Función DsRestorePrepare (Ntdsbcli. h)
description: Conecta con el servidor de directorio especificado y lo prepara para la operación de restauración.
ms.assetid: e847d57a-32e1-49c0-800c-7ce0e5f442fa
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsRestorePrepare
topic_type:
- apiref
api_name:
- DsRestorePrepare
- DsRestorePrepareA
- DsRestorePrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb040a315b6cc94f2d296b032a954b00473a4ca2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150203"
---
# <a name="dsrestoreprepare-function"></a><span data-ttu-id="247f2-104">DsRestorePrepare función)</span><span class="sxs-lookup"><span data-stu-id="247f2-104">DsRestorePrepare function</span></span>

<span data-ttu-id="247f2-105">\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="247f2-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="247f2-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="247f2-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="247f2-107">A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="247f2-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="247f2-108">La función **DsRestorePrepare** se conecta al servidor de directorio especificado y lo prepara para la operación de restauración.</span><span class="sxs-lookup"><span data-stu-id="247f2-108">The **DsRestorePrepare** function connects to the specified directory server and prepares it for the restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="247f2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="247f2-109">Syntax</span></span>


```C++
HRESULT DsRestorePrepare(
  _In_  LPCWSTR szServerName,
  _In_  ULONG   rtFlag,
  _In_  PVOID   pvExpiryToken,
  _In_  DWORD   cbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a><span data-ttu-id="247f2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="247f2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="247f2-111">*szServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="247f2-111">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="247f2-112">Puntero a una cadena terminada en null que contiene el nombre del servidor que se va a restaurar.</span><span class="sxs-lookup"><span data-stu-id="247f2-112">Pointer to a null-terminated string that contains the name of the server to restore.</span></span> <span data-ttu-id="247f2-113">Las barras diagonales inversas anteriores son opcionales.</span><span class="sxs-lookup"><span data-stu-id="247f2-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="247f2-114">El servidor debe ser el mismo equipo desde el que se llama a esta función.</span><span class="sxs-lookup"><span data-stu-id="247f2-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="247f2-115">El nombre del servidor no puede contener caracteres de subrayado ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="247f2-115">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="247f2-116">Un ejemplo de un nombre de servidor es " \\ \\ server1".</span><span class="sxs-lookup"><span data-stu-id="247f2-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="247f2-117">*rtFlag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="247f2-117">*rtFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="247f2-118">Especifica el tipo de restauración que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="247f2-118">Specifies the type of restoration to perform.</span></span> <span data-ttu-id="247f2-119">Puede ser cero o uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="247f2-119">This can be zero or one of the following values.</span></span>

<dt>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>

<span data-ttu-id="247f2-120"><span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**tipo de restauración \_ \_ puesta al día**</span><span class="sxs-lookup"><span data-stu-id="247f2-120"><span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**RESTORE\_TYPE\_CATCHUP**</span></span>


</dt> <dd>

<span data-ttu-id="247f2-121">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="247f2-121">Default.</span></span> <span data-ttu-id="247f2-122">La versión restaurada se concilia a través de la lógica de conciliación estándar para que el DIT restaurado pueda sincronizarse con otros equipos de servidor de empresa.</span><span class="sxs-lookup"><span data-stu-id="247f2-122">The restored version is reconciled through the standard reconciliation logic so that the restored DIT can synchronize with other enterprise server computers.</span></span>

</dd> <dt>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>

<span data-ttu-id="247f2-123"><span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**tipo de restauración \_ \_ AUTHORATATIVE**</span><span class="sxs-lookup"><span data-stu-id="247f2-123"><span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**RESTORE\_TYPE\_AUTHORATATIVE**</span></span>


</dt> <dd>

<span data-ttu-id="247f2-124">No compatible.</span><span class="sxs-lookup"><span data-stu-id="247f2-124">Not Supported.</span></span>

</dd> <dt>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>

<span data-ttu-id="247f2-125"><span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**tipo de restauración \_ \_ en línea**</span><span class="sxs-lookup"><span data-stu-id="247f2-125"><span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**RESTORE\_TYPE\_ONLINE**</span></span>


</dt> <dd>

<span data-ttu-id="247f2-126">No compatible.</span><span class="sxs-lookup"><span data-stu-id="247f2-126">Not Supported.</span></span> <span data-ttu-id="247f2-127">La restauración se realiza cuando NTDS está en línea.</span><span class="sxs-lookup"><span data-stu-id="247f2-127">Restoration is performed when NTDS is online.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="247f2-128">*pvExpiryToken* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="247f2-128">*pvExpiryToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="247f2-129">Puntero al token de expiración asociado a la copia de seguridad que se está restaurando.</span><span class="sxs-lookup"><span data-stu-id="247f2-129">Pointer to the expiry token associated with the backup being restored.</span></span> <span data-ttu-id="247f2-130">Este token se obtuvo de la función [**DsBackupPrepare**](dsbackupprepare.md) cuando se realizó una copia de seguridad del directorio.</span><span class="sxs-lookup"><span data-stu-id="247f2-130">This token was obtained from the [**DsBackupPrepare**](dsbackupprepare.md) function when the directory was backed up.</span></span>

<span data-ttu-id="247f2-131">Si este parámetro es **null**, el identificador devuelto en *phbc* solo se puede usar para obtener los directorios de restauración con la función [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) .</span><span class="sxs-lookup"><span data-stu-id="247f2-131">If this parameter is **NULL**, the handle returned in *phbc* can only be used to obtain the restoration directories with the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function.</span></span> <span data-ttu-id="247f2-132">El identificador no se puede usar para otras funciones de restauración.</span><span class="sxs-lookup"><span data-stu-id="247f2-132">The handle cannot be used for any other restoration functions.</span></span>

</dd> <dt>

<span data-ttu-id="247f2-133">*cbExpiryTokenSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="247f2-133">*cbExpiryTokenSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="247f2-134">Contiene el tamaño, en bytes, del token de expiración en *pvExpiryToken*.</span><span class="sxs-lookup"><span data-stu-id="247f2-134">Contains the size, in bytes, of the expiry token in *pvExpiryToken*.</span></span>

</dd> <dt>

<span data-ttu-id="247f2-135">*phbc* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="247f2-135">*phbc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="247f2-136">Puntero a un valor de **HBC** que recibe el identificador de la restauración.</span><span class="sxs-lookup"><span data-stu-id="247f2-136">Pointer to an **HBC** value that receives the handle for the restore.</span></span> <span data-ttu-id="247f2-137">Este identificador se usa al llamar a otras funciones de restauración del servicio de directorio, como [**DsBackupOpenFile**](dsbackupopenfile.md) y [**DsRestoreEnd**](dsrestoreend.md).</span><span class="sxs-lookup"><span data-stu-id="247f2-137">This handle is used when calling other Directory Service restore functions, such as [**DsBackupOpenFile**](dsbackupopenfile.md) and [**DsRestoreEnd**](dsrestoreend.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="247f2-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="247f2-138">Return value</span></span>

<span data-ttu-id="247f2-139">Si es correcto, devuelve un código **HRESULT** estándar; de lo contrario, se devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="247f2-139">If successful, returns a standard **HRESULT** codes; otherwise, a failure code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="247f2-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="247f2-140">Remarks</span></span>

<span data-ttu-id="247f2-141">La función **DsRestorePrepare** requiere que el autor de la llamada sea miembro del grupo administradores en el servidor.</span><span class="sxs-lookup"><span data-stu-id="247f2-141">The **DsRestorePrepare** function requires that the caller is a member of the Administrators group on the server.</span></span>

<span data-ttu-id="247f2-142">**DsRestorePrepare** se puede usar con o sin un token proporcionado.</span><span class="sxs-lookup"><span data-stu-id="247f2-142">**DsRestorePrepare** may be used with or without a token provided.</span></span> <span data-ttu-id="247f2-143">Si se proporciona el token, se comprueba la expiración y se permiten todas las operaciones en el contexto devuelto.</span><span class="sxs-lookup"><span data-stu-id="247f2-143">If the token is provided, it is checked for expiration, and all operations are allowed on the context returned.</span></span> <span data-ttu-id="247f2-144">Si no se proporciona el token, el contexto devuelto es restringido y solo se puede usar para la función [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) .</span><span class="sxs-lookup"><span data-stu-id="247f2-144">If the token is not provided, the context returned is restricted, and may be used only for the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function.</span></span> <span data-ttu-id="247f2-145">No se puede usar para la función [**DsRestoreRegister**](dsrestoreregister.md) .</span><span class="sxs-lookup"><span data-stu-id="247f2-145">It may not be used for the [**DsRestoreRegister**](dsrestoreregister.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="247f2-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="247f2-146">Requirements</span></span>



| <span data-ttu-id="247f2-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="247f2-147">Requirement</span></span> | <span data-ttu-id="247f2-148">Value</span><span class="sxs-lookup"><span data-stu-id="247f2-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="247f2-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="247f2-149">Minimum supported client</span></span><br/> | <span data-ttu-id="247f2-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="247f2-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="247f2-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="247f2-151">Minimum supported server</span></span><br/> | <span data-ttu-id="247f2-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="247f2-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="247f2-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="247f2-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="247f2-154"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="247f2-154"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="247f2-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="247f2-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="247f2-156"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="247f2-156"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="247f2-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="247f2-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="247f2-158"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="247f2-158"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="247f2-159">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="247f2-159">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="247f2-160">**DsRestorePrepareW** (Unicode) y **DsRestorePrepareA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="247f2-160">**DsRestorePrepareW** (Unicode) and **DsRestorePrepareA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="247f2-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="247f2-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="247f2-162">Restauración de un servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="247f2-162">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="247f2-163">Funciones de copia de seguridad de directorios</span><span class="sxs-lookup"><span data-stu-id="247f2-163">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="247f2-164">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="247f2-164">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="247f2-165">**DsRestoreRegister**</span><span class="sxs-lookup"><span data-stu-id="247f2-165">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="247f2-166">**DsRestoreRegisterComplete**</span><span class="sxs-lookup"><span data-stu-id="247f2-166">**DsRestoreRegisterComplete**</span></span>](dsrestoreregistercomplete.md)
</dt> <dt>

[<span data-ttu-id="247f2-167">**DsRestoreEnd**</span><span class="sxs-lookup"><span data-stu-id="247f2-167">**DsRestoreEnd**</span></span>](dsrestoreend.md)
</dt> </dl>

 

