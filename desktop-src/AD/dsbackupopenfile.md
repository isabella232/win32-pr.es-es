---
title: Función DsBackupOpenFile (Ntdsbcli. h)
description: Abre el archivo especificado y realiza las operaciones de cliente y servidor necesarias para preparar el archivo para la copia de seguridad.
ms.assetid: 1ffb81ee-9e7e-4d88-91fc-f1857377d125
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsBackupOpenFile
topic_type:
- apiref
api_name:
- DsBackupOpenFile
- DsBackupOpenFileA
- DsBackupOpenFileW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f9c4eac9c9825f510848583d7f707a2c244c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150411"
---
# <a name="dsbackupopenfile-function"></a><span data-ttu-id="92a0f-104">DsBackupOpenFile función)</span><span class="sxs-lookup"><span data-stu-id="92a0f-104">DsBackupOpenFile function</span></span>

<span data-ttu-id="92a0f-105">\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="92a0f-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="92a0f-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="92a0f-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="92a0f-107">A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="92a0f-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="92a0f-108">La función **DsBackupOpenFile** abre el archivo especificado y realiza las operaciones de cliente y servidor necesarias para preparar el archivo para la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="92a0f-108">The **DsBackupOpenFile** function opens the specified file and performs the client and server operations necessary to prepare the file for backup.</span></span>

## <a name="syntax"></a><span data-ttu-id="92a0f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92a0f-109">Syntax</span></span>


```C++
HRESULT DsBackupOpenFile(
  _In_  HBC           hbc,
  _In_  LPCTSTR       szAttachmentName,
  _In_  DWORD         cbReadHintSize,
  _Out_ LARGE_INTEGER *pliFileSize
);
```



## <a name="parameters"></a><span data-ttu-id="92a0f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92a0f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92a0f-111">*HBC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92a0f-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92a0f-112">Contiene el identificador de contexto de copia de seguridad obtenido con la función [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="92a0f-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="92a0f-113">*szAttachmentName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92a0f-113">*szAttachmentName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92a0f-114">Puntero a una cadena terminada en null que especifica el nombre del archivo de copia de seguridad que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="92a0f-114">Pointer to a null-terminated string that specifies the name of the backup file to open.</span></span>

</dd> <dt>

<span data-ttu-id="92a0f-115">*cbReadHintSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92a0f-115">*cbReadHintSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92a0f-116">Contiene el tamaño posible, en bytes, del búfer pasado como el argumento *pvBuffer* en la función [**DsBackupRead**](dsbackupread.md) .</span><span class="sxs-lookup"><span data-stu-id="92a0f-116">Contains the possible size, in bytes, of the buffer passed as the *pvBuffer* argument in the [**DsBackupRead**](dsbackupread.md) function.</span></span> <span data-ttu-id="92a0f-117">Las funciones de copia de seguridad usan este valor como una sugerencia para optimizar el tráfico de red.</span><span class="sxs-lookup"><span data-stu-id="92a0f-117">The backup functions use this value as a hint to optimize the network traffic.</span></span> <span data-ttu-id="92a0f-118">Este valor debe ser un múltiplo de 8192 y debe ser mayor o igual que 24576.</span><span class="sxs-lookup"><span data-stu-id="92a0f-118">This value must be a multiple of 8192 and must be greater than or equal to 24576.</span></span>

</dd> <dt>

<span data-ttu-id="92a0f-119">*pliFileSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="92a0f-119">*pliFileSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92a0f-120">Puntero a un **valor \_ entero grande** que recibe el tamaño, en bytes, del archivo de copia de seguridad abierto.</span><span class="sxs-lookup"><span data-stu-id="92a0f-120">Pointer to a **LARGE\_INTEGER** value that receives the size, in bytes, of the backup file opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92a0f-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92a0f-121">Return value</span></span>

<span data-ttu-id="92a0f-122">Devuelve **S \_ OK** si la función es correcta o un código de error de Win32 o RPC en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="92a0f-122">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="92a0f-123">En la lista siguiente se enumeran otros códigos de error posibles.</span><span class="sxs-lookup"><span data-stu-id="92a0f-123">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="92a0f-124">**ERROR de \_ acceso \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="92a0f-124">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="92a0f-125">El autor de la llamada no dispone de los privilegios de acceso adecuados para llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="92a0f-125">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="92a0f-126">La función [**DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para establecer las credenciales que se usarán para las funciones de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="92a0f-126">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="92a0f-127">**ERROR \_ de \_ parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="92a0f-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="92a0f-128">*HBC*, *szAttachmentName* o *pliFileSize* no son válidos.</span><span class="sxs-lookup"><span data-stu-id="92a0f-128">*hbc*, *szAttachmentName*, or *pliFileSize* are invalid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92a0f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92a0f-129">Requirements</span></span>



| <span data-ttu-id="92a0f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="92a0f-130">Requirement</span></span> | <span data-ttu-id="92a0f-131">Value</span><span class="sxs-lookup"><span data-stu-id="92a0f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92a0f-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92a0f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="92a0f-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92a0f-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="92a0f-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92a0f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="92a0f-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92a0f-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="92a0f-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92a0f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="92a0f-137"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="92a0f-137"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="92a0f-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92a0f-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="92a0f-139"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92a0f-139"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="92a0f-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="92a0f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92a0f-141"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92a0f-141"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="92a0f-142">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="92a0f-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="92a0f-143">**DsBackupOpenFileW** (Unicode) y **DsBackupOpenFileA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="92a0f-143">**DsBackupOpenFileW** (Unicode) and **DsBackupOpenFileA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="92a0f-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="92a0f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92a0f-145">**DsBackupRead**</span><span class="sxs-lookup"><span data-stu-id="92a0f-145">**DsBackupRead**</span></span>](dsbackupread.md)
</dt> <dt>

[<span data-ttu-id="92a0f-146">Copia de seguridad de un servidor Active Directory</span><span class="sxs-lookup"><span data-stu-id="92a0f-146">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="92a0f-147">Funciones de copia de seguridad de directorios</span><span class="sxs-lookup"><span data-stu-id="92a0f-147">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

