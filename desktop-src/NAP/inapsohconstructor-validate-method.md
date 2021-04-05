---
title: Método Validate de INapSoHConstructor (NapProtocol. h)
description: Comprueba la validez del paquete SoH.
ms.assetid: 66338213-43c0-461a-a794-5f18d56bd505
keywords:
- Validar el método NAP
- Método Validate NAP, interfaz INapSoHConstructor
- Interfaz INapSoHConstructor NAP, método Validate
topic_type:
- apiref
api_name:
- INapSoHConstructor.Validate
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7db8a52d7986348e85c724171b6d417996c7315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803104"
---
# <a name="inapsohconstructorvalidate-method"></a><span data-ttu-id="895d1-106">INapSoHConstructor:: Validate (método)</span><span class="sxs-lookup"><span data-stu-id="895d1-106">INapSoHConstructor::Validate method</span></span>

> [!Note]  
> <span data-ttu-id="895d1-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="895d1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="895d1-108">El método **INapSoHConstructor:: Validate** comprueba la validez del paquete SOH.</span><span class="sxs-lookup"><span data-stu-id="895d1-108">The **INapSoHConstructor::Validate** method checks the validity of the SoH packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="895d1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="895d1-109">Syntax</span></span>


```C++
HRESULT Validate(
  [in] const SoH  *soh,
  [in]       BOOL isRequest
);
```



## <a name="parameters"></a><span data-ttu-id="895d1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="895d1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="895d1-111">*SOH* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="895d1-111">*soh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="895d1-112">Puntero al paquete [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) construido.</span><span class="sxs-lookup"><span data-stu-id="895d1-112">A pointer to the constructed [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="895d1-113">*isRequest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="895d1-113">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="895d1-114">Valor **booleano** que es **true** si el paquete es un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) y **false** si es un **SoHResponse**.</span><span class="sxs-lookup"><span data-stu-id="895d1-114">A **BOOL** that is **TRUE** if the packet is an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is an **SoHResponse**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="895d1-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="895d1-115">Return value</span></span>

<span data-ttu-id="895d1-116">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="895d1-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="895d1-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="895d1-117">Return code</span></span>                                                                                            | <span data-ttu-id="895d1-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="895d1-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="895d1-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="895d1-119"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="895d1-120">El paquete SoH es válido.</span><span class="sxs-lookup"><span data-stu-id="895d1-120">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="895d1-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="895d1-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="895d1-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="895d1-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="895d1-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="895d1-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="895d1-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="895d1-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="895d1-125"><dt>**\_paquete NAP E \_ no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="895d1-125"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="895d1-126">El paquete SoH no es válido.</span><span class="sxs-lookup"><span data-stu-id="895d1-126">The SoH packet is invalid.</span></span><br/>                              |



 

## <a name="requirements"></a><span data-ttu-id="895d1-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="895d1-127">Requirements</span></span>



| <span data-ttu-id="895d1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="895d1-128">Requirement</span></span> | <span data-ttu-id="895d1-129">Value</span><span class="sxs-lookup"><span data-stu-id="895d1-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="895d1-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="895d1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="895d1-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="895d1-131">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="895d1-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="895d1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="895d1-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="895d1-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="895d1-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="895d1-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="895d1-135"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="895d1-135"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="895d1-136">IDL</span><span class="sxs-lookup"><span data-stu-id="895d1-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="895d1-137"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="895d1-137"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="895d1-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="895d1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="895d1-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="895d1-139"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="895d1-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="895d1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="895d1-141">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="895d1-141">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





