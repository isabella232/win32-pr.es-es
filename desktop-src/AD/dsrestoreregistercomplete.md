---
title: Función DsRestoreRegisterComplete (Ntdsbcli. h)
description: Se llama para desbloquear un servidor Active Directory una vez completada una operación de restauración.
ms.assetid: 781cd2ec-d2e2-4f3a-903d-feda4b871de5
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsRestoreRegisterComplete
topic_type:
- apiref
api_name:
- DsRestoreRegisterComplete
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5e5e01b29281860dff59fbcd08a3b48ec66c4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079490"
---
# <a name="dsrestoreregistercomplete-function"></a><span data-ttu-id="e49c7-104">DsRestoreRegisterComplete función)</span><span class="sxs-lookup"><span data-stu-id="e49c7-104">DsRestoreRegisterComplete function</span></span>

<span data-ttu-id="e49c7-105">\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="e49c7-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e49c7-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="e49c7-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e49c7-107">En su lugar, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="e49c7-107">Use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="e49c7-108">Se llama a la función **DsRestoreRegisterComplete** para desbloquear un servidor Active Directory una vez finalizada una operación de restauración.</span><span class="sxs-lookup"><span data-stu-id="e49c7-108">The **DsRestoreRegisterComplete** function is called to unlock an Active Directory server after a restore operation is complete.</span></span> <span data-ttu-id="e49c7-109">Esta función es equivalente a la función [**DsRestoreRegister**](dsrestoreregister.md) .</span><span class="sxs-lookup"><span data-stu-id="e49c7-109">This function is counterpart to the [**DsRestoreRegister**](dsrestoreregister.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="e49c7-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e49c7-110">Syntax</span></span>


```C++
HRESULT DsRestoreRegisterComplete(
  _In_ HBC     hbc,
  _In_ HRESULT hrRestoreState
);
```



## <a name="parameters"></a><span data-ttu-id="e49c7-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e49c7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e49c7-112">*HBC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e49c7-112">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e49c7-113">Contiene el identificador de contexto de restauración obtenido con la función [**DsRestorePrepare**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="e49c7-113">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e49c7-114">*hrRestoreState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e49c7-114">*hrRestoreState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e49c7-115">Contiene el estado final de la operación de restauración.</span><span class="sxs-lookup"><span data-stu-id="e49c7-115">Contains the final status of the restore operation.</span></span> <span data-ttu-id="e49c7-116">Este parámetro debe contener **S \_ OK** si la operación de restauración se realizó correctamente o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e49c7-116">This parameter should contain **S\_OK** if the restore operation was successful or an error code otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e49c7-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e49c7-117">Return value</span></span>

<span data-ttu-id="e49c7-118">Devuelve **S \_ OK** si la función es correcta o un código de error de Win32 o RPC en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e49c7-118">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="e49c7-119">En la lista siguiente se enumeran los posibles códigos de error.</span><span class="sxs-lookup"><span data-stu-id="e49c7-119">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="e49c7-120">**ERROR de \_ acceso \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="e49c7-120">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="e49c7-121">El autor de la llamada no dispone de los privilegios de acceso adecuados para llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="e49c7-121">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="e49c7-122">La función [**DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para establecer las credenciales que se usarán para las funciones de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="e49c7-122">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e49c7-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e49c7-123">Remarks</span></span>

<span data-ttu-id="e49c7-124">Antes de reiniciar el controlador de dominio, llame a esta función para proporcionar el estado de la operación de restauración.</span><span class="sxs-lookup"><span data-stu-id="e49c7-124">Before you restart the domain controller, call this function to provide the status of the restore operation.</span></span> <span data-ttu-id="e49c7-125">Si el estado no es correcto, el servicio de directorio no se iniciará hasta que se haya restaurado una base de datos válida.</span><span class="sxs-lookup"><span data-stu-id="e49c7-125">If the status is not successful, the directory service will not start until a valid database has been restored.</span></span> <span data-ttu-id="e49c7-126">Esta función completa la operación de restauración y permite iniciar Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="e49c7-126">This function completes the restore operation and allows Active Directory Domain Services to start.</span></span>

## <a name="requirements"></a><span data-ttu-id="e49c7-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e49c7-127">Requirements</span></span>



| <span data-ttu-id="e49c7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e49c7-128">Requirement</span></span> | <span data-ttu-id="e49c7-129">Value</span><span class="sxs-lookup"><span data-stu-id="e49c7-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e49c7-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e49c7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e49c7-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e49c7-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e49c7-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e49c7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e49c7-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e49c7-133">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e49c7-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="e49c7-134">End of client support</span></span><br/>    | <span data-ttu-id="e49c7-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e49c7-135">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e49c7-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="e49c7-136">End of server support</span></span><br/>    | <span data-ttu-id="e49c7-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e49c7-137">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e49c7-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e49c7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e49c7-139"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="e49c7-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="e49c7-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e49c7-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="e49c7-141"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e49c7-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="e49c7-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e49c7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e49c7-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e49c7-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e49c7-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="e49c7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e49c7-145">**DsRestoreRegister**</span><span class="sxs-lookup"><span data-stu-id="e49c7-145">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="e49c7-146">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="e49c7-146">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="e49c7-147">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="e49c7-147">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="e49c7-148">Restauración de un servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="e49c7-148">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="e49c7-149">Funciones de copia de seguridad de directorios</span><span class="sxs-lookup"><span data-stu-id="e49c7-149">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

