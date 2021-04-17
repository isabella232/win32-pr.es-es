---
title: Método SetFlags de INapEnforcementClientConnection (NapEnforcementClient. h)
description: Se usa para diferenciar las respuestas por primera vez de las respuestas debido a SoHRequests almacenados en memoria caché por los imforcedores. | Método SetFlags de INapEnforcementClientConnection (NapEnforcementClient. h)
ms.assetid: 2f35bcdf-662c-431f-a39e-a7c758f35603
keywords:
- Método SetFlags NAP
- Método SetFlags NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método SetFlags
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489997fb97f0e97c5a72d23646af8ae92272628
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105653201"
---
# <a name="inapenforcementclientconnectionsetflags-method"></a><span data-ttu-id="bacf3-107">INapEnforcementClientConnection:: SetFlags (método)</span><span class="sxs-lookup"><span data-stu-id="bacf3-107">INapEnforcementClientConnection::SetFlags method</span></span>

> [!Note]  
> <span data-ttu-id="bacf3-108">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="bacf3-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="bacf3-109">El método **INapEnforcementClientConnection:: SetFlags** se usa para diferenciar las respuestas por primera vez de las respuestas debidas a SoHRequests almacenados en memoria caché por los imforcedores.</span><span class="sxs-lookup"><span data-stu-id="bacf3-109">The **INapEnforcementClientConnection::SetFlags** method is used to differentiate first-time responses from responses due to SoHRequests cached by the enforcers.</span></span>

## <a name="syntax"></a><span data-ttu-id="bacf3-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bacf3-110">Syntax</span></span>


```C++
HRESULT SetFlags(
  [in] UINT8 flags
);
```



## <a name="parameters"></a><span data-ttu-id="bacf3-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bacf3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bacf3-112">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="bacf3-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bacf3-113">Marcas que determinan si el [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) se debe a un **SoHRequest** almacenado en memoria caché.</span><span class="sxs-lookup"><span data-stu-id="bacf3-113">Flags that determines if the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) is due to a cached **SoHRequest**.</span></span> <span data-ttu-id="bacf3-114">Si *Flags* tiene un valor de [**freshSoHRequest**](nap-type-constants.md), es una solicitud nueva; en caso contrario, se trata de una solicitud almacenada en caché.</span><span class="sxs-lookup"><span data-stu-id="bacf3-114">If *flags* has a value of [**freshSoHRequest**](nap-type-constants.md), it is a new request; otherwise it is a cached request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bacf3-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bacf3-115">Return value</span></span>

<span data-ttu-id="bacf3-116">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="bacf3-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="bacf3-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bacf3-117">Return code</span></span>                                                                                     | <span data-ttu-id="bacf3-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="bacf3-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="bacf3-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="bacf3-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="bacf3-120">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="bacf3-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bacf3-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="bacf3-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="bacf3-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="bacf3-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="bacf3-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bacf3-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="bacf3-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="bacf3-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bacf3-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bacf3-125">Remarks</span></span>

<span data-ttu-id="bacf3-126">NapAgent establece este valor.</span><span class="sxs-lookup"><span data-stu-id="bacf3-126">This value is set by the NapAgent.</span></span>

## <a name="requirements"></a><span data-ttu-id="bacf3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bacf3-127">Requirements</span></span>



| <span data-ttu-id="bacf3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bacf3-128">Requirement</span></span> | <span data-ttu-id="bacf3-129">Value</span><span class="sxs-lookup"><span data-stu-id="bacf3-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bacf3-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bacf3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bacf3-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bacf3-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bacf3-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bacf3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bacf3-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bacf3-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bacf3-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bacf3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="bacf3-135"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="bacf3-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="bacf3-136">IDL</span><span class="sxs-lookup"><span data-stu-id="bacf3-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bacf3-137"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bacf3-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="bacf3-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bacf3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bacf3-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bacf3-139"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="bacf3-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="bacf3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bacf3-141">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="bacf3-141">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





