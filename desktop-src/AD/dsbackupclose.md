---
title: Función DsBackupClose (Ntdsbcli. h)
description: Cierra un archivo de copia de seguridad abierto con la función DsBackupOpenFile.
ms.assetid: 5452a222-abe8-4d2d-84ff-6f577073b220
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsBackupClose
topic_type:
- apiref
api_name:
- DsBackupClose
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d03c9cd7f125d223d264236a52120714d5198c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490252"
---
# <a name="dsbackupclose-function"></a><span data-ttu-id="996ac-104">DsBackupClose función)</span><span class="sxs-lookup"><span data-stu-id="996ac-104">DsBackupClose function</span></span>

<span data-ttu-id="996ac-105">\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="996ac-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="996ac-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="996ac-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="996ac-107">A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="996ac-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="996ac-108">La función **DsBackupClose** cierra un archivo de copia de seguridad abierto con la función [**DsBackupOpenFile**](dsbackupopenfile.md) .</span><span class="sxs-lookup"><span data-stu-id="996ac-108">The **DsBackupClose** function closes a backup file opened with the [**DsBackupOpenFile**](dsbackupopenfile.md) function.</span></span> <span data-ttu-id="996ac-109">Para cada identificador de copia de seguridad, solo se puede abrir un archivo cada vez, por lo que esta función cierra el archivo abierto actualmente.</span><span class="sxs-lookup"><span data-stu-id="996ac-109">For each backup handle, only one file can be opened at a time, so this function closes the currently open file.</span></span>

## <a name="syntax"></a><span data-ttu-id="996ac-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="996ac-110">Syntax</span></span>


```C++
HRESULT DsBackupClose(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="996ac-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="996ac-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="996ac-112">*HBC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="996ac-112">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="996ac-113">Contiene el identificador de contexto de copia de seguridad obtenido con la función [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="996ac-113">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="996ac-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="996ac-114">Return value</span></span>

<span data-ttu-id="996ac-115">Devuelve **S \_ OK** si la función es correcta o un código de error de Win32 o RPC en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="996ac-115">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="996ac-116">En la lista siguiente se enumeran otros códigos de error posibles.</span><span class="sxs-lookup"><span data-stu-id="996ac-116">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="996ac-117">**ERROR \_ de \_ parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="996ac-117">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="996ac-118">*HBC* no es válido.</span><span class="sxs-lookup"><span data-stu-id="996ac-118">*hbc* is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="996ac-119">**hrInvalidHandle**</span><span class="sxs-lookup"><span data-stu-id="996ac-119">**hrInvalidHandle**</span></span>
</dt> <dd>

<span data-ttu-id="996ac-120">No hay ningún archivo abierto actualmente.</span><span class="sxs-lookup"><span data-stu-id="996ac-120">No file is currently open.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="996ac-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="996ac-121">Requirements</span></span>



| <span data-ttu-id="996ac-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="996ac-122">Requirement</span></span> | <span data-ttu-id="996ac-123">Value</span><span class="sxs-lookup"><span data-stu-id="996ac-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="996ac-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="996ac-124">Minimum supported client</span></span><br/> | <span data-ttu-id="996ac-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="996ac-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="996ac-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="996ac-126">Minimum supported server</span></span><br/> | <span data-ttu-id="996ac-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="996ac-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="996ac-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="996ac-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="996ac-129"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="996ac-129"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="996ac-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="996ac-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="996ac-131"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="996ac-131"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="996ac-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="996ac-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="996ac-133"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="996ac-133"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="996ac-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="996ac-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="996ac-135">**DsBackupOpenFile**</span><span class="sxs-lookup"><span data-stu-id="996ac-135">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="996ac-136">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="996ac-136">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="996ac-137">Copia de seguridad de un servidor Active Directory</span><span class="sxs-lookup"><span data-stu-id="996ac-137">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="996ac-138">Funciones de copia de seguridad de directorios</span><span class="sxs-lookup"><span data-stu-id="996ac-138">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

