---
title: Método INapSoHConstructor GetSoH (NapProtocol. h)
description: Recupera el paquete SoHRequest o SoHResponse construido.
ms.assetid: 402c72fd-9e23-453a-8c95-57615295e056
keywords:
- Método GetSoH NAP
- Método GetSoH NAP, interfaz INapSoHConstructor
- Interfaz INapSoHConstructor NAP, método GetSoH
topic_type:
- apiref
api_name:
- INapSoHConstructor.GetSoH
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066257aadf0ed14816efec06936d4b070087159f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150222"
---
# <a name="inapsohconstructorgetsoh-method"></a><span data-ttu-id="39ef6-106">INapSoHConstructor:: GetSoH (método)</span><span class="sxs-lookup"><span data-stu-id="39ef6-106">INapSoHConstructor::GetSoH method</span></span>

> [!Note]  
> <span data-ttu-id="39ef6-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="39ef6-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="39ef6-108">El método **INapSoHConstructor:: GetSoH** recupera el paquete SoHRequest o SoHResponse construido.</span><span class="sxs-lookup"><span data-stu-id="39ef6-108">The **INapSoHConstructor::GetSoH** method retrieves the constructed SoHRequest or SoHResponse packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="39ef6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39ef6-109">Syntax</span></span>


```C++
HRESULT GetSoH(
  [out] SoH **soh
);
```



## <a name="parameters"></a><span data-ttu-id="39ef6-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39ef6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39ef6-111">*SOH* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="39ef6-111">*soh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39ef6-112">Un puntero a un puntero al paquete [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) o **SoHResponse** construido.</span><span class="sxs-lookup"><span data-stu-id="39ef6-112">A pointer to a pointer to the constructed [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) or **SoHResponse** packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39ef6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39ef6-113">Return value</span></span>

<span data-ttu-id="39ef6-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="39ef6-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="39ef6-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="39ef6-115">Return code</span></span>                                                                                     | <span data-ttu-id="39ef6-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="39ef6-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="39ef6-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="39ef6-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="39ef6-118">Operación correcta.</span><span class="sxs-lookup"><span data-stu-id="39ef6-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="39ef6-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="39ef6-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="39ef6-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="39ef6-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="39ef6-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="39ef6-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="39ef6-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="39ef6-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="39ef6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39ef6-123">Requirements</span></span>



| <span data-ttu-id="39ef6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="39ef6-124">Requirement</span></span> | <span data-ttu-id="39ef6-125">Value</span><span class="sxs-lookup"><span data-stu-id="39ef6-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="39ef6-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39ef6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="39ef6-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="39ef6-127">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="39ef6-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39ef6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="39ef6-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="39ef6-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="39ef6-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39ef6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="39ef6-131"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="39ef6-131"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="39ef6-132">IDL</span><span class="sxs-lookup"><span data-stu-id="39ef6-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="39ef6-133"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="39ef6-133"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="39ef6-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="39ef6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39ef6-135"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39ef6-135"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="39ef6-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="39ef6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39ef6-137">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="39ef6-137">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





