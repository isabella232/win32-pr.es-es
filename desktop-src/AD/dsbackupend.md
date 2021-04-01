---
title: Función DsBackupEnd (Ntdsbcli. h)
description: Se llama para finalizar una operación de copia de seguridad.
ms.assetid: 872645bc-3dbe-4b12-af4f-778d54feb18f
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsBackupEnd
topic_type:
- apiref
api_name:
- DsBackupEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9663eedec7bc298ef594990baababcf2083546e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905183"
---
# <a name="dsbackupend-function"></a><span data-ttu-id="0e1d3-104">DsBackupEnd función)</span><span class="sxs-lookup"><span data-stu-id="0e1d3-104">DsBackupEnd function</span></span>

<span data-ttu-id="0e1d3-105">\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="0e1d3-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0e1d3-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="0e1d3-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="0e1d3-107">A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="0e1d3-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="0e1d3-108">Se llama a la función **DsBackupEnd** para finalizar una operación de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="0e1d3-108">The **DsBackupEnd** function is called to terminate a backup operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e1d3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e1d3-109">Syntax</span></span>


```C++
HRESULT DsBackupEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="0e1d3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e1d3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e1d3-111">*HBC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0e1d3-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e1d3-112">Contiene el identificador de contexto de copia de seguridad obtenido con la función [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="0e1d3-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e1d3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0e1d3-113">Return value</span></span>

<span data-ttu-id="0e1d3-114">Devuelve **S \_ OK** si la función es correcta o un código de error de Win32 o RPC en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0e1d3-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="0e1d3-115">En la lista siguiente se enumeran otros códigos de error posibles.</span><span class="sxs-lookup"><span data-stu-id="0e1d3-115">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="0e1d3-116">**ERROR \_ de \_ parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="0e1d3-116">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="0e1d3-117">*HBC* no es válido.</span><span class="sxs-lookup"><span data-stu-id="0e1d3-117">*hbc* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e1d3-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e1d3-118">Remarks</span></span>

<span data-ttu-id="0e1d3-119">La función **DsBackupEnd** cierra los identificadores de enlace pendientes y realiza una limpieza después de un intento de copia de seguridad correcto o incorrecto.</span><span class="sxs-lookup"><span data-stu-id="0e1d3-119">The **DsBackupEnd** function closes outstanding binding handles and performs a cleanup after a successful or unsuccessful backup attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e1d3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e1d3-120">Requirements</span></span>



| <span data-ttu-id="0e1d3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e1d3-121">Requirement</span></span> | <span data-ttu-id="0e1d3-122">Value</span><span class="sxs-lookup"><span data-stu-id="0e1d3-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e1d3-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e1d3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0e1d3-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e1d3-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0e1d3-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e1d3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0e1d3-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e1d3-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e1d3-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e1d3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e1d3-128"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e1d3-128"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e1d3-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0e1d3-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="0e1d3-130"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e1d3-130"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="0e1d3-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0e1d3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e1d3-132"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e1d3-132"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e1d3-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e1d3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e1d3-134">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="0e1d3-134">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="0e1d3-135">Copia de seguridad de un servidor Active Directory</span><span class="sxs-lookup"><span data-stu-id="0e1d3-135">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="0e1d3-136">Funciones de copia de seguridad de directorios</span><span class="sxs-lookup"><span data-stu-id="0e1d3-136">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

