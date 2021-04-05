---
title: Método Initialize INapSoHConstructor (NapProtocol. h)
description: Inicializa un paquete de protocolo SoH en el sistema NAP.
ms.assetid: 1678b677-c8c8-465c-a412-9b929e39bbac
keywords:
- Inicializar el método NAP
- Inicializar método NAP, interfaz INapSoHConstructor
- Interfaz INapSoHConstructor NAP, método Initialize
topic_type:
- apiref
api_name:
- INapSoHConstructor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab8d6b27547be6e7c7e9abb59f7edb7b49e716e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996319"
---
# <a name="inapsohconstructorinitialize-method"></a><span data-ttu-id="4bde3-106">INapSoHConstructor:: Initialize (método)</span><span class="sxs-lookup"><span data-stu-id="4bde3-106">INapSoHConstructor::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="4bde3-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="4bde3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4bde3-108">El método **INapSoHConstructor:: Initialize** Inicializa un paquete de protocolo SOH en el sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="4bde3-108">The **INapSoHConstructor::Initialize** method initializes a SoH protocol packet in the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bde3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4bde3-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId id,
  [in] BOOL                 isRequest
);
```



## <a name="parameters"></a><span data-ttu-id="4bde3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4bde3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bde3-111">*ID.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="4bde3-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bde3-112">Un [SystemHealthEntityId](nap-datatypes.md) único que contiene el identificador del Sha o SHV que está construyendo el paquete.</span><span class="sxs-lookup"><span data-stu-id="4bde3-112">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA or SHV that is constructing the packet.</span></span>

</dd> <dt>

<span data-ttu-id="4bde3-113">*isRequest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4bde3-113">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bde3-114">Valor **booleano** que es **true** si el paquete va a ser un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) y **false** si va a ser un **SoHResponse**.</span><span class="sxs-lookup"><span data-stu-id="4bde3-114">A **BOOL** that is **TRUE** if the packet is to be an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is to be an **SoHResponse**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bde3-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4bde3-115">Return value</span></span>

<span data-ttu-id="4bde3-116">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="4bde3-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="4bde3-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4bde3-117">Return code</span></span>                                                                                     | <span data-ttu-id="4bde3-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="4bde3-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="4bde3-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="4bde3-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="4bde3-120">Operación correcta.</span><span class="sxs-lookup"><span data-stu-id="4bde3-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="4bde3-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="4bde3-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="4bde3-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="4bde3-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="4bde3-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4bde3-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="4bde3-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="4bde3-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4bde3-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4bde3-125">Remarks</span></span>

<span data-ttu-id="4bde3-126">Se debe llamar a este método exactamente una vez por paquete.</span><span class="sxs-lookup"><span data-stu-id="4bde3-126">This method must be called exactly once per packet.</span></span>

<span data-ttu-id="4bde3-127">El [SystemHealthEntityId](nap-datatypes.md) especificado en *ID*. es el primer TLV del paquete SOH recién construido y tiene el tipo de atributo [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md).</span><span class="sxs-lookup"><span data-stu-id="4bde3-127">The [SystemHealthEntityId](nap-datatypes.md) specified in *id*, is the first TLV in the newly constructed SOH packet and has the attribute type [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bde3-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bde3-128">Requirements</span></span>



| <span data-ttu-id="4bde3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bde3-129">Requirement</span></span> | <span data-ttu-id="4bde3-130">Value</span><span class="sxs-lookup"><span data-stu-id="4bde3-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bde3-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bde3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4bde3-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4bde3-132">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4bde3-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bde3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4bde3-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4bde3-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4bde3-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4bde3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bde3-136"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bde3-136"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="4bde3-137">IDL</span><span class="sxs-lookup"><span data-stu-id="4bde3-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4bde3-138"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4bde3-138"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="4bde3-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4bde3-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bde3-140"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bde3-140"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="4bde3-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="4bde3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bde3-142">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="4bde3-142">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





