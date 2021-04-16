---
title: Método INapSystemHealthValidationRequest2 GetConfigID (NapSystemHealthValidator. h)
description: Lo usan los validadores de mantenimiento del sistema (SHV) para recuperar el identificador de configuración en una solicitud de validación.
ms.assetid: 6d5564e4-8386-444b-a859-f0c855e4ee30
keywords:
- Método GetConfigID NAP
- Método GetConfigID NAP, interfaz INapSystemHealthValidationRequest2
- Interfaz INapSystemHealthValidationRequest2 NAP, método GetConfigID
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2.GetConfigID
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3b41d2f08dc117fd28e704d607c628ec73e6ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676961"
---
# <a name="inapsystemhealthvalidationrequest2getconfigid-method"></a><span data-ttu-id="a397c-106">INapSystemHealthValidationRequest2:: GetConfigID (método)</span><span class="sxs-lookup"><span data-stu-id="a397c-106">INapSystemHealthValidationRequest2::GetConfigID method</span></span>

> [!Note]  
> <span data-ttu-id="a397c-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="a397c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a397c-108">Los validadores de mantenimiento del sistema (SHV) usan el método **INapSystemHealthValidationRequest2:: GetConfigId** para recuperar el identificador de configuración en una solicitud de validación.</span><span class="sxs-lookup"><span data-stu-id="a397c-108">The **INapSystemHealthValidationRequest2::GetConfigId** method is used by the System Health Validators (SHVs) to retrieve the configuration ID in a validation request.</span></span>

## <a name="syntax"></a><span data-ttu-id="a397c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a397c-109">Syntax</span></span>


```C++
HRESULT GetConfigID(
  [out] UINT32 *configID
) const;
```



## <a name="parameters"></a><span data-ttu-id="a397c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a397c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a397c-111">*configID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a397c-111">*configID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a397c-112">En la devolución, un puntero a UINT32 que contiene un ID. de configuración del SHV.</span><span class="sxs-lookup"><span data-stu-id="a397c-112">On return, a pointer to UINT32 that contains a configuration ID of the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a397c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a397c-113">Return value</span></span>

<span data-ttu-id="a397c-114">Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="a397c-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="a397c-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a397c-115">Return code</span></span>                                                                                  | <span data-ttu-id="a397c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a397c-116">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="a397c-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a397c-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a397c-118">Operación correcta.</span><span class="sxs-lookup"><span data-stu-id="a397c-118">Operation successful.</span></span><br/>                |
| <dl> <span data-ttu-id="a397c-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a397c-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a397c-120">El parámetro configID era **null**.</span><span class="sxs-lookup"><span data-stu-id="a397c-120">The configID parameter was **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a397c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a397c-121">Requirements</span></span>



| <span data-ttu-id="a397c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a397c-122">Requirement</span></span> | <span data-ttu-id="a397c-123">Value</span><span class="sxs-lookup"><span data-stu-id="a397c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a397c-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a397c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a397c-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a397c-125">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="a397c-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a397c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a397c-127">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a397c-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a397c-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a397c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a397c-129"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="a397c-129"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="a397c-130">IDL</span><span class="sxs-lookup"><span data-stu-id="a397c-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a397c-131"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a397c-131"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="a397c-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a397c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a397c-133"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a397c-133"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="a397c-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="a397c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a397c-135">**INapSystemHealthValidationRequest2**</span><span class="sxs-lookup"><span data-stu-id="a397c-135">**INapSystemHealthValidationRequest2**</span></span>](inapsystemhealthvalidationrequest2.md)
</dt> </dl>

 

 





