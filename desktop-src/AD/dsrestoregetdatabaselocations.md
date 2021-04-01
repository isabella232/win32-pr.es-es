---
title: Función DsRestoreGetDatabaseLocations (Ntdsbcli. h)
description: Obtiene las ubicaciones en las que se deben copiar los archivos de copia de seguridad durante una operación de restauración.
ms.assetid: f91d701c-72cf-418a-8d1c-6bf6ef41c2c1
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsRestoreGetDatabaseLocations
topic_type:
- apiref
api_name:
- DsRestoreGetDatabaseLocations
- DsRestoreGetDatabaseLocationsA
- DsRestoreGetDatabaseLocationsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bcebb9f3822332269e1db09f3246c128e4ad1f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905410"
---
# <a name="dsrestoregetdatabaselocations-function"></a><span data-ttu-id="8c986-104">DsRestoreGetDatabaseLocations función)</span><span class="sxs-lookup"><span data-stu-id="8c986-104">DsRestoreGetDatabaseLocations function</span></span>

<span data-ttu-id="8c986-105">\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="8c986-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8c986-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="8c986-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="8c986-107">A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="8c986-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="8c986-108">La función **DsRestoreGetDatabaseLocations** obtiene las ubicaciones en las que se deben copiar los archivos de copia de seguridad durante una operación de restauración.</span><span class="sxs-lookup"><span data-stu-id="8c986-108">The **DsRestoreGetDatabaseLocations** function obtains the locations where backup files should be copied during a restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c986-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c986-109">Syntax</span></span>


```C++
HRESULT DsRestoreGetDatabaseLocations(
  _In_  HBC     hbc,
  _Out_ LPWSTR  *pszDatabaseLocationList,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="8c986-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c986-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c986-111">*HBC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c986-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c986-112">Contiene el identificador de contexto de restauración obtenido con la función [**DsRestorePrepare**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="8c986-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="8c986-113">*pszDatabaseLocationList* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8c986-113">*pszDatabaseLocationList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c986-114">Puntero a un puntero de cadena que recibe la lista de ubicaciones de la base de datos como rutas UNC.</span><span class="sxs-lookup"><span data-stu-id="8c986-114">Pointer to a string pointer that receives the list of database locations as UNC paths.</span></span> <span data-ttu-id="8c986-115">Esta lista recibe una lista de dos cadenas terminadas en NULL con un valor nulo.</span><span class="sxs-lookup"><span data-stu-id="8c986-115">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="8c986-116">Este búfer se asigna mediante la función **DsRestoreGetDatabaseLocations** y se debe liberar cuando ya no es necesario llamando a la función [**DsBackupFree**](dsbackupfree.md) .</span><span class="sxs-lookup"><span data-stu-id="8c986-116">This buffer is allocated by the **DsRestoreGetDatabaseLocations** function and must be freed when it is no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="8c986-117">El primer carácter de cada uno de los nombres de archivo contiene una de las [**constantes BFT**](bft-constants.md) que identifica el tipo de nombre.</span><span class="sxs-lookup"><span data-stu-id="8c986-117">The first character of each of the file names contains one of the [**BFT Constants**](bft-constants.md) that identifies the name type.</span></span> <span data-ttu-id="8c986-118">La función **DsRestoreGetDatabaseLocations** solo proporciona los siguientes tipos de nombre.</span><span class="sxs-lookup"><span data-stu-id="8c986-118">The **DsRestoreGetDatabaseLocations** function only supplies the following name types.</span></span>

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span data-ttu-id="8c986-119"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_base de \_ datos Ntds BFT**</span><span class="sxs-lookup"><span data-stu-id="8c986-119"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>


</dt> <dd>

<span data-ttu-id="8c986-120">El archivo de base de datos NTDS debe copiarse en este archivo.</span><span class="sxs-lookup"><span data-stu-id="8c986-120">The NTDS database file should be copied to this file.</span></span> <span data-ttu-id="8c986-121">Este es el archivo que se identificó como **BFT \_ NTDS \_ Database** cuando se realizó la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8c986-121">This is the file that was identified as **BFT\_NTDS\_DATABASE** when the backup was performed.</span></span>

</dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>

<span data-ttu-id="8c986-122"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**DIR. de registro de BFT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8c986-122"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT\_LOG\_DIR**</span></span>


</dt> <dd>

<span data-ttu-id="8c986-123">Todos los archivos de registro se copian en este directorio.</span><span class="sxs-lookup"><span data-stu-id="8c986-123">All log files are copied to this directory.</span></span> <span data-ttu-id="8c986-124">Los archivos de registro se identificaron como **\_ registro de BFT** cuando se realizó la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8c986-124">The log files were identified as **BFT\_LOG** when the backup was performed.</span></span>

</dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>

<span data-ttu-id="8c986-125"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**DIR. de punto de BFT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8c986-125"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT\_CHECKPOINT\_DIR**</span></span>


</dt> <dd>

<span data-ttu-id="8c986-126">Todos los archivos de revisión se copian en este directorio.</span><span class="sxs-lookup"><span data-stu-id="8c986-126">All patch files are copied to this directory.</span></span> <span data-ttu-id="8c986-127">Los archivos de revisión se identificaron como **\_ \_ archivo de revisión BFT** cuando se realizó la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8c986-127">The patch files were identified as **BFT\_PATCH\_FILE** when the backup was performed.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8c986-128">*PCB* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8c986-128">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c986-129">Puntero al valor **DWORD** que recibe el tamaño, en bytes, del búfer *pszDatabaseLocationList* .</span><span class="sxs-lookup"><span data-stu-id="8c986-129">Pointer to **DWORD** value that receives the size, in bytes, of the *pszDatabaseLocationList* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c986-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c986-130">Return value</span></span>

<span data-ttu-id="8c986-131">Devuelve **S \_ OK** si la función es correcta o un código de error de Win32 o RPC en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8c986-131">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="8c986-132">En la lista siguiente se enumeran los posibles códigos de error.</span><span class="sxs-lookup"><span data-stu-id="8c986-132">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="8c986-133">**ERROR de \_ acceso \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="8c986-133">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="8c986-134">El autor de la llamada no dispone de los privilegios de acceso adecuados para llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="8c986-134">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="8c986-135">La función [**DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para establecer las credenciales que se usarán para las funciones de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="8c986-135">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="8c986-136">**ERROR \_ de \_ parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="8c986-136">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="8c986-137">*HBC*, *pszDatabaseLocationList* o *PCB* no son válidos.</span><span class="sxs-lookup"><span data-stu-id="8c986-137">*hbc*, *pszDatabaseLocationList*, or *pcbSize* are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="8c986-138">**ERROR \_ de \_ memoria insuficiente \_**</span><span class="sxs-lookup"><span data-stu-id="8c986-138">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="8c986-139">Error de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="8c986-139">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c986-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c986-140">Remarks</span></span>

<span data-ttu-id="8c986-141">La función **DsRestoreGetDatabaseLocations** se puede usar para obtener los directorios de restauración sin acceso a los datos de los que se ha realizado una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8c986-141">The **DsRestoreGetDatabaseLocations** function can be used to obtain the restoration directories without access to the backed up data.</span></span> <span data-ttu-id="8c986-142">Para ello, llame a [**DsRestorePrepare**](dsrestoreprepare.md) con **null** para el parámetro *pvExpiryToken* .</span><span class="sxs-lookup"><span data-stu-id="8c986-142">To do this, call [**DsRestorePrepare**](dsrestoreprepare.md) with **NULL** for the *pvExpiryToken* parameter.</span></span> <span data-ttu-id="8c986-143">Esto hace que **DsRestorePrepare** devuelva un identificador de contexto restringido que solo se puede usar con la función **DsRestoreGetDatabaseLocations** .</span><span class="sxs-lookup"><span data-stu-id="8c986-143">This causes **DsRestorePrepare** to return a restricted context handle which can only be used with the **DsRestoreGetDatabaseLocations** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c986-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c986-144">Requirements</span></span>



| <span data-ttu-id="8c986-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c986-145">Requirement</span></span> | <span data-ttu-id="8c986-146">Value</span><span class="sxs-lookup"><span data-stu-id="8c986-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c986-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c986-147">Minimum supported client</span></span><br/> | <span data-ttu-id="8c986-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c986-148">Windows Vista</span></span><br/>                                                                              |
| <span data-ttu-id="8c986-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c986-149">Minimum supported server</span></span><br/> | <span data-ttu-id="8c986-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c986-150">Windows Server 2008</span></span><br/>                                                                        |
| <span data-ttu-id="8c986-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c986-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c986-152"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c986-152"><dt>Ntdsbcli.h</dt></span></span> </dl>                 |
| <span data-ttu-id="8c986-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c986-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="8c986-154"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c986-154"><dt>Ntdsbcli.lib</dt></span></span> </dl>               |
| <span data-ttu-id="8c986-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c986-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c986-156"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c986-156"><dt>Ntdsbcli.dll</dt></span></span> </dl>               |
| <span data-ttu-id="8c986-157">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="8c986-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8c986-158">**DsRestoreGetDatabaseLocationsW** (Unicode) y **DsRestoreGetDatabaseLocationsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8c986-158">**DsRestoreGetDatabaseLocationsW** (Unicode) and **DsRestoreGetDatabaseLocationsA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8c986-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c986-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c986-160">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="8c986-160">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="8c986-161">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="8c986-161">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="8c986-162">Funciones de copia de seguridad de directorios</span><span class="sxs-lookup"><span data-stu-id="8c986-162">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="8c986-163">Restauración de Active Directory</span><span class="sxs-lookup"><span data-stu-id="8c986-163">Restoring Active Directory</span></span>](restoring-an-active-directory-server.md)
</dt> </dl>

 

