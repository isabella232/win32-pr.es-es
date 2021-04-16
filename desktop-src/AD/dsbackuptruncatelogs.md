---
title: Función DsBackupTruncateLogs (Ntdsbcli. h)
description: Trunca los registros de copia de seguridad previamente leídos.
ms.assetid: fae2e19f-08b8-410f-a735-dd4d41fc71a6
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsBackupTruncateLogs
topic_type:
- apiref
api_name:
- DsBackupTruncateLogs
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 051ced828656c6b6e5af156e2d1a69c3b741cdce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534053"
---
# <a name="dsbackuptruncatelogs-function"></a><span data-ttu-id="ba28f-104">DsBackupTruncateLogs función)</span><span class="sxs-lookup"><span data-stu-id="ba28f-104">DsBackupTruncateLogs function</span></span>

<span data-ttu-id="ba28f-105">\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="ba28f-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ba28f-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="ba28f-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="ba28f-107">A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="ba28f-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="ba28f-108">La función **DsBackupTruncateLogs** trunca los registros de copia de seguridad previamente leídos.</span><span class="sxs-lookup"><span data-stu-id="ba28f-108">The **DsBackupTruncateLogs** function truncates the previously read backup logs.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba28f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba28f-109">Syntax</span></span>


```C++
HRESULT DsBackupTruncateLogs(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="ba28f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba28f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba28f-111">*HBC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ba28f-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba28f-112">Contiene el identificador de contexto de copia de seguridad obtenido con la función [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="ba28f-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba28f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba28f-113">Return value</span></span>

<span data-ttu-id="ba28f-114">Devuelve **S \_ OK** si la función es correcta o un código de error de Win32 o RPC en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ba28f-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="ba28f-115">En la lista siguiente se enumeran otros códigos de error posibles.</span><span class="sxs-lookup"><span data-stu-id="ba28f-115">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="ba28f-116">**ERROR de \_ acceso \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="ba28f-116">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="ba28f-117">El autor de la llamada no dispone de los privilegios de acceso adecuados para llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="ba28f-117">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="ba28f-118">La función [**DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para establecer las credenciales que se usarán para las funciones de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="ba28f-118">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="ba28f-119">**ERROR \_ de \_ parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="ba28f-119">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="ba28f-120">*HBC* no es válido.</span><span class="sxs-lookup"><span data-stu-id="ba28f-120">*hbc* is invalid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba28f-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba28f-121">Remarks</span></span>

<span data-ttu-id="ba28f-122">Utilice la función **DsBackupTruncateLogs** cuando se haya completado correctamente una copia de seguridad completa o incremental.</span><span class="sxs-lookup"><span data-stu-id="ba28f-122">Use the **DsBackupTruncateLogs** function when a full or incremental backup has completed successfully.</span></span>

> [!Caution]  
> <span data-ttu-id="ba28f-123">Si se llama a esta función después de una copia de seguridad diferencial, se perderá toda la información de copia de seguridad incremental.</span><span class="sxs-lookup"><span data-stu-id="ba28f-123">If this function is called after a differential backup, all of the incremental backup information will be lost.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ba28f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba28f-124">Requirements</span></span>



| <span data-ttu-id="ba28f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba28f-125">Requirement</span></span> | <span data-ttu-id="ba28f-126">Value</span><span class="sxs-lookup"><span data-stu-id="ba28f-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba28f-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba28f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ba28f-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba28f-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ba28f-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba28f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ba28f-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba28f-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ba28f-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba28f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba28f-132"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba28f-132"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="ba28f-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba28f-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="ba28f-134"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba28f-134"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="ba28f-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ba28f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba28f-136"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba28f-136"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba28f-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba28f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba28f-138">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="ba28f-138">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="ba28f-139">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="ba28f-139">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="ba28f-140">**DsSetCurrentBackupLog**</span><span class="sxs-lookup"><span data-stu-id="ba28f-140">**DsSetCurrentBackupLog**</span></span>](dssetcurrentbackuplog.md)
</dt> <dt>

[<span data-ttu-id="ba28f-141">Copia de seguridad de un servidor Active Directory</span><span class="sxs-lookup"><span data-stu-id="ba28f-141">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="ba28f-142">Funciones de copia de seguridad de directorios</span><span class="sxs-lookup"><span data-stu-id="ba28f-142">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

