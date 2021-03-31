---
title: Función DsRestoreRegister (Ntdsbcli. h)
description: Registra una operación de restauración.
ms.assetid: 83a56985-89be-4a95-9a8d-7c6f78d61c9a
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsRestoreRegister
topic_type:
- apiref
api_name:
- DsRestoreRegister
- DsRestoreRegisterA
- DsRestoreRegisterW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 610d49c73ade9bab47c95e90af73bac606f4bd23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079491"
---
# <a name="dsrestoreregister-function"></a><span data-ttu-id="7256e-104">DsRestoreRegister función)</span><span class="sxs-lookup"><span data-stu-id="7256e-104">DsRestoreRegister function</span></span>

<span data-ttu-id="7256e-105">\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="7256e-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7256e-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="7256e-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7256e-107">A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="7256e-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="7256e-108">La función **DsRestoreRegister** registra una operación de restauración. Esta función bloquea todas las operaciones de restauración posteriores y evita que el destino de restauración se inicie hasta que se llame a la función [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="7256e-108">The **DsRestoreRegister** function registers a restore operation.This function interlocks all subsequent restore operations and prevents the restore target from starting until the [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) function is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="7256e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7256e-109">Syntax</span></span>


```C++
HRESULT DsRestoreRegister(
  _In_ HBC        hbc,
  _In_ LPCTSTR    szCheckPointFilePath,
  _In_ LPCTSTR    szLogPath,
  _In_ EDB_RSTMAP rgrstmap[],
  _In_ LONG       crstmap,
  _In_ LPCTSTR    szBackupLogPath,
  _In_ ULONG      genLow,
  _In_ ULONG      genHigh
);
```



## <a name="parameters"></a><span data-ttu-id="7256e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7256e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7256e-111">*HBC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7256e-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7256e-112">Contiene el identificador de contexto de restauración obtenido con la función [**DsRestorePrepare**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="7256e-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="7256e-113">*szCheckPointFilePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7256e-113">*szCheckPointFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7256e-114">Puntero a una cadena terminada en null que contiene la ruta de acceso al archivo de punto de comprobación.</span><span class="sxs-lookup"><span data-stu-id="7256e-114">Pointer to a null-terminated string that contains the path to the checkpoint file.</span></span> <span data-ttu-id="7256e-115">La función [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) proporciona esta ruta de acceso y tiene un valor **BFT** de **BFT \_ Checkpoint \_ dir**.</span><span class="sxs-lookup"><span data-stu-id="7256e-115">This path is provided by the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function and has a **BFT** value of **BFT\_CHECKPOINT\_DIR**.</span></span> <span data-ttu-id="7256e-116">Normalmente, es igual que la ruta de acceso de la base de datos del sistema.</span><span class="sxs-lookup"><span data-stu-id="7256e-116">Typically this is the same as the system database path.</span></span> <span data-ttu-id="7256e-117">Esta ruta de acceso es necesaria para la función de restauración de copia de seguridad adecuada.</span><span class="sxs-lookup"><span data-stu-id="7256e-117">This path is required for proper backup restore function.</span></span> <span data-ttu-id="7256e-118">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="7256e-118">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="7256e-119">Si se pasa **null** en este parámetro, se producirá un error durante el proceso de restauración.</span><span class="sxs-lookup"><span data-stu-id="7256e-119">Passing **NULL** in this parameter will cause an error during the restore process.</span></span>

</dd> <dt>

<span data-ttu-id="7256e-120">*szLogPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7256e-120">*szLogPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7256e-121">Puntero a una cadena terminada en null que contiene la ruta de acceso donde se restaurarán los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="7256e-121">Pointer to a null-terminated string that contains the path where the log files will be restored.</span></span> <span data-ttu-id="7256e-122">La función [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) proporciona esta ruta de acceso y tiene un valor **BFT** de **BFT \_ log \_ dir**.</span><span class="sxs-lookup"><span data-stu-id="7256e-122">This path is provided by the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function and has a **BFT** value of **BFT\_LOG\_DIR**.</span></span> <span data-ttu-id="7256e-123">Si la ruta de acceso apunta a un directorio vacío, se crean nuevos archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="7256e-123">If the path points to an empty directory, new log files are created there.</span></span> <span data-ttu-id="7256e-124">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="7256e-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7256e-125">*rgrstmap* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7256e-125">*rgrstmap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7256e-126">Una matriz de estructuras [**EDB \_ RSTMAP**](edb-rstmap.md) que contiene las rutas de acceso antiguas y nuevas para cada base de datos.</span><span class="sxs-lookup"><span data-stu-id="7256e-126">An array of [**EDB\_RSTMAP**](edb-rstmap.md) structures that contains the old and new paths for each database.</span></span> <span data-ttu-id="7256e-127">Hay una estructura para cada base de datos.</span><span class="sxs-lookup"><span data-stu-id="7256e-127">There is one structure for each database.</span></span> <span data-ttu-id="7256e-128">En el directorio, existe una estructura para la base de datos del sistema y otra estructura para la base de datos de directorio.</span><span class="sxs-lookup"><span data-stu-id="7256e-128">For the directory, there is a structure for the system database and another structure for the directory database.</span></span> <span data-ttu-id="7256e-129">No importa el orden de los elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="7256e-129">The order of the elements in the array does not matter.</span></span> <span data-ttu-id="7256e-130">El parámetro *crstmap* contiene el número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="7256e-130">The *crstmap* parameter contains the number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="7256e-131">*crstmap* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7256e-131">*crstmap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7256e-132">Contiene el número de elementos de la matriz *rgrstmap* .</span><span class="sxs-lookup"><span data-stu-id="7256e-132">Contains the number of elements in the *rgrstmap* array.</span></span>

</dd> <dt>

<span data-ttu-id="7256e-133">*szBackupLogPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7256e-133">*szBackupLogPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7256e-134">Puntero a una cadena terminada en null que contiene la ruta de acceso donde residen los archivos de registro de los que se ha realizado una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7256e-134">Pointer to a null-terminated string that contains the path where the backed up log files currently reside.</span></span> <span data-ttu-id="7256e-135">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="7256e-135">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7256e-136">*genLow* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7256e-136">*genLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7256e-137">Contiene el número de registro más bajo que se va a restaurar en esta sesión de restauración.</span><span class="sxs-lookup"><span data-stu-id="7256e-137">Contains the lowest log number to restore in this restore session.</span></span> <span data-ttu-id="7256e-138">Es un número hexadecimal en el intervalo de 0x00000 a 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="7256e-138">This is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="7256e-139">*genHigh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7256e-139">*genHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7256e-140">Contiene el número de registro más alto que se va a restaurar en esta sesión de restauración.</span><span class="sxs-lookup"><span data-stu-id="7256e-140">Contains the highest log number to restore in this restore session.</span></span> <span data-ttu-id="7256e-141">Es un número hexadecimal en el intervalo de 0x00000 a 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="7256e-141">This is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7256e-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7256e-142">Return value</span></span>

<span data-ttu-id="7256e-143">Devuelve **S \_ OK** si la función es correcta o un código de error de Win32 o RPC en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7256e-143">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="7256e-144">En la lista siguiente se enumeran los posibles códigos de error.</span><span class="sxs-lookup"><span data-stu-id="7256e-144">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="7256e-145">**ERROR de \_ acceso \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="7256e-145">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="7256e-146">El autor de la llamada no dispone de los privilegios de acceso adecuados para llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="7256e-146">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="7256e-147">La función [**DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para establecer las credenciales que se usarán para las funciones de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="7256e-147">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="7256e-148">**ERROR \_ de \_ parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="7256e-148">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="7256e-149">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="7256e-149">One or more parameters are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="7256e-150">**hrMissingExpiryToken**</span><span class="sxs-lookup"><span data-stu-id="7256e-150">**hrMissingExpiryToken**</span></span>
</dt> <dd>

<span data-ttu-id="7256e-151">El token de expiración proporcionado a [**DsRestorePrepare**](dsrestoreprepare.md) no era válido.</span><span class="sxs-lookup"><span data-stu-id="7256e-151">The expiry token supplied to [**DsRestorePrepare**](dsrestoreprepare.md) was invalid.</span></span> <span data-ttu-id="7256e-152">Este valor se define en Ntdsbmsg. h.</span><span class="sxs-lookup"><span data-stu-id="7256e-152">This value is defined in Ntdsbmsg.h.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7256e-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7256e-153">Requirements</span></span>



| <span data-ttu-id="7256e-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="7256e-154">Requirement</span></span> | <span data-ttu-id="7256e-155">Value</span><span class="sxs-lookup"><span data-stu-id="7256e-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7256e-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7256e-156">Minimum supported client</span></span><br/> | <span data-ttu-id="7256e-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7256e-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7256e-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7256e-158">Minimum supported server</span></span><br/> | <span data-ttu-id="7256e-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7256e-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7256e-160">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7256e-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="7256e-161"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="7256e-161"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="7256e-162">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7256e-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="7256e-163"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7256e-163"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="7256e-164">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7256e-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7256e-165"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7256e-165"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="7256e-166">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="7256e-166">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7256e-167">**DsRestoreRegisterW** (Unicode) y **DsRestoreRegisterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7256e-167">**DsRestoreRegisterW** (Unicode) and **DsRestoreRegisterA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="7256e-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="7256e-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7256e-169">**DsRestoreRegisterComplete**</span><span class="sxs-lookup"><span data-stu-id="7256e-169">**DsRestoreRegisterComplete**</span></span>](dsrestoreregistercomplete.md)
</dt> <dt>

[<span data-ttu-id="7256e-170">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="7256e-170">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="7256e-171">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="7256e-171">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="7256e-172">**DsRestoreEnd**</span><span class="sxs-lookup"><span data-stu-id="7256e-172">**DsRestoreEnd**</span></span>](dsrestoreend.md)
</dt> <dt>

[<span data-ttu-id="7256e-173">**EDB \_ RSTMAP**</span><span class="sxs-lookup"><span data-stu-id="7256e-173">**EDB\_RSTMAP**</span></span>](edb-rstmap.md)
</dt> <dt>

[<span data-ttu-id="7256e-174">Restauración de Active Directory</span><span class="sxs-lookup"><span data-stu-id="7256e-174">Restoring Active Directory</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="7256e-175">Funciones de copia de seguridad de directorios</span><span class="sxs-lookup"><span data-stu-id="7256e-175">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

