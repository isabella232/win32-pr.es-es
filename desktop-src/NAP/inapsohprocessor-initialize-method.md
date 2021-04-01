---
title: Método Initialize INapSoHProcessor (NapProtocol. h)
description: Inicializa el paquete de protocolo y el sistema de procesador SoH. Se debe llamar a este método exactamente una vez.
ms.assetid: 4fccc847-3c4d-4fc5-935d-28fb2964a9be
keywords:
- Inicializar el método NAP
- Inicializar método NAP, interfaz INapSoHProcessor
- Interfaz INapSoHProcessor NAP, método Initialize
topic_type:
- apiref
api_name:
- INapSoHProcessor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ff3a32bb213caf19964ccea8175a43e5016f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996392"
---
# <a name="inapsohprocessorinitialize-method"></a><span data-ttu-id="544cb-107">INapSoHProcessor:: Initialize (método)</span><span class="sxs-lookup"><span data-stu-id="544cb-107">INapSoHProcessor::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="544cb-108">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="544cb-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="544cb-109">El método **INapSoHProcessor:: Initialize** inicializa el sistema del procesador SOH y el paquete de protocolo.</span><span class="sxs-lookup"><span data-stu-id="544cb-109">The **INapSoHProcessor::Initialize** method initializes the protocol packet and SoH processor system.</span></span> <span data-ttu-id="544cb-110">Se debe llamar a este método exactamente una vez.</span><span class="sxs-lookup"><span data-stu-id="544cb-110">This method must be called exactly once.</span></span>

## <a name="syntax"></a><span data-ttu-id="544cb-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="544cb-111">Syntax</span></span>


```C++
HRESULT Initialize(
  [in]  const SoH                  *soh,
  [in]        BOOL                 isRequest,
  [out]       SystemHealthEntityId *id
);
```



## <a name="parameters"></a><span data-ttu-id="544cb-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="544cb-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="544cb-113">*SOH* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="544cb-113">*soh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="544cb-114">Un puntero al paquete [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) que se va a procesar.</span><span class="sxs-lookup"><span data-stu-id="544cb-114">A pointer to the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="544cb-115">*isRequest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="544cb-115">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="544cb-116">Valor **booleano** que es **true** si el paquete es un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) y **false** si es un **SoHResponse**.</span><span class="sxs-lookup"><span data-stu-id="544cb-116">A **BOOL** that is **TRUE** if the packet is an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is an **SoHResponse**.</span></span>

</dd> <dt>

<span data-ttu-id="544cb-117">*ID.* de \[ salida\]</span><span class="sxs-lookup"><span data-stu-id="544cb-117">*id* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="544cb-118">Un [SystemHealthEntityId](nap-datatypes.md) único que contiene el identificador del Sha o SHV que construyó el paquete.</span><span class="sxs-lookup"><span data-stu-id="544cb-118">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA or SHV that constructed the packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="544cb-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="544cb-119">Return value</span></span>

<span data-ttu-id="544cb-120">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="544cb-120">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="544cb-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="544cb-121">Return code</span></span>                                                                                            | <span data-ttu-id="544cb-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="544cb-122">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="544cb-123"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="544cb-123"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="544cb-124">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="544cb-124">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="544cb-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="544cb-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="544cb-126">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="544cb-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="544cb-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="544cb-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="544cb-128">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="544cb-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="544cb-129"><dt>**\_paquete NAP E \_ no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="544cb-129"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="544cb-130">El paquete SoH no es válido.</span><span class="sxs-lookup"><span data-stu-id="544cb-130">The SoH packet is invalid.</span></span><br/>                              |



 

## <a name="requirements"></a><span data-ttu-id="544cb-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="544cb-131">Requirements</span></span>



| <span data-ttu-id="544cb-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="544cb-132">Requirement</span></span> | <span data-ttu-id="544cb-133">Value</span><span class="sxs-lookup"><span data-stu-id="544cb-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="544cb-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="544cb-134">Minimum supported client</span></span><br/> | <span data-ttu-id="544cb-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="544cb-135">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="544cb-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="544cb-136">Minimum supported server</span></span><br/> | <span data-ttu-id="544cb-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="544cb-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="544cb-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="544cb-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="544cb-139"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="544cb-139"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="544cb-140">IDL</span><span class="sxs-lookup"><span data-stu-id="544cb-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="544cb-141"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="544cb-141"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="544cb-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="544cb-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="544cb-143"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="544cb-143"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="544cb-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="544cb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="544cb-145">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="544cb-145">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





