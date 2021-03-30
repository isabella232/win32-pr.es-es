---
title: Función DsRestoreEnd (Ntdsbcli. h)
description: Se llama para finalizar una operación de restauración.
ms.assetid: 2c3b9aba-3e92-4e5b-afff-3ed9bf64832b
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsRestoreEnd
topic_type:
- apiref
api_name:
- DsRestoreEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabbe216875c2fe934f3c87e32688cd17bc8992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079279"
---
# <a name="dsrestoreend-function"></a><span data-ttu-id="1a7ae-104">DsRestoreEnd función)</span><span class="sxs-lookup"><span data-stu-id="1a7ae-104">DsRestoreEnd function</span></span>

<span data-ttu-id="1a7ae-105">\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="1a7ae-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1a7ae-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="1a7ae-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1a7ae-107">En su lugar, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="1a7ae-107">Use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="1a7ae-108">Se llama a la función **DsRestoreEnd** para finalizar una operación de restauración.</span><span class="sxs-lookup"><span data-stu-id="1a7ae-108">The **DsRestoreEnd** function is called to terminate a restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a7ae-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a7ae-109">Syntax</span></span>


```C++
HRESULT DsRestoreEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="1a7ae-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a7ae-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a7ae-111">*HBC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1a7ae-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a7ae-112">Contiene el identificador de contexto de restauración obtenido con la función [**DsRestorePrepare**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="1a7ae-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a7ae-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a7ae-113">Return value</span></span>

<span data-ttu-id="1a7ae-114">Devuelve **S \_ OK** si la función es correcta o un código de error de Win32 o RPC en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1a7ae-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="1a7ae-115">En la lista siguiente se enumeran los posibles códigos de error.</span><span class="sxs-lookup"><span data-stu-id="1a7ae-115">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="1a7ae-116">**ERROR \_ de \_ parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="1a7ae-116">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="1a7ae-117">*HBC* no es válido.</span><span class="sxs-lookup"><span data-stu-id="1a7ae-117">*hbc* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a7ae-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a7ae-118">Remarks</span></span>

<span data-ttu-id="1a7ae-119">La función **DsRestoreEnd** cierra los identificadores de enlace pendientes y realiza una operación de limpieza después de un intento de restauración.</span><span class="sxs-lookup"><span data-stu-id="1a7ae-119">The **DsRestoreEnd** function closes outstanding binding handles and performs a cleanup operation after a restore attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a7ae-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a7ae-120">Requirements</span></span>



| <span data-ttu-id="1a7ae-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a7ae-121">Requirement</span></span> | <span data-ttu-id="1a7ae-122">Value</span><span class="sxs-lookup"><span data-stu-id="1a7ae-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a7ae-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a7ae-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1a7ae-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1a7ae-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1a7ae-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a7ae-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1a7ae-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1a7ae-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1a7ae-127">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="1a7ae-127">End of client support</span></span><br/>    | <span data-ttu-id="1a7ae-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1a7ae-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1a7ae-129">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="1a7ae-129">End of server support</span></span><br/>    | <span data-ttu-id="1a7ae-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1a7ae-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1a7ae-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a7ae-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a7ae-132"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a7ae-132"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a7ae-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a7ae-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="1a7ae-134"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a7ae-134"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="1a7ae-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1a7ae-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a7ae-136"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a7ae-136"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a7ae-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a7ae-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a7ae-138">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="1a7ae-138">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="1a7ae-139">Restauración de un servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="1a7ae-139">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="1a7ae-140">Funciones de copia de seguridad de directorios</span><span class="sxs-lookup"><span data-stu-id="1a7ae-140">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

