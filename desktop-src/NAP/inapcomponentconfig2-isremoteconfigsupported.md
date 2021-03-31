---
title: Método INapComponentConfig2 IsRemoteConfigSupported (NapCommon. h)
description: Lo implementan los validadores de mantenimiento del sistema (SHV) para indicar si se admite la configuración remota.
ms.assetid: c4b8e60b-ed60-49ec-b4d6-4e1575e4d1a5
keywords:
- Método IsRemoteConfigSupported NAP
- Método IsRemoteConfigSupported NAP, interfaz INapComponentConfig2
- Interfaz INapComponentConfig2 NAP, método IsRemoteConfigSupported
topic_type:
- apiref
api_name:
- INapComponentConfig2.IsRemoteConfigSupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2d144926aafff6f5ad7e243efe2a81a2955f497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996187"
---
# <a name="inapcomponentconfig2isremoteconfigsupported-method"></a><span data-ttu-id="5736d-106">INapComponentConfig2:: IsRemoteConfigSupported (método)</span><span class="sxs-lookup"><span data-stu-id="5736d-106">INapComponentConfig2::IsRemoteConfigSupported method</span></span>

> [!Note]  
> <span data-ttu-id="5736d-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="5736d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5736d-108">Los validadores de mantenimiento del sistema (SHV) implementan el método **IsRemoteConfigSupported** para indicar si se admite la configuración remota.</span><span class="sxs-lookup"><span data-stu-id="5736d-108">The **IsRemoteConfigSupported** method is implemented by system health validators (SHVs) to indicate whether remote configuration is supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="5736d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5736d-109">Syntax</span></span>


```C++
HRESULT IsRemoteConfigSupported(
  [out] BOOL  *isSupported,
  [out] UINT8 *remoteConfigType
);
```



## <a name="parameters"></a><span data-ttu-id="5736d-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5736d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5736d-111">*isSupported* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5736d-111">*isSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5736d-112">Un puntero a un valor BOOLEANO que se establece en **true** si el componente admite la configuración remota y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5736d-112">A pointer to a BOOL that is set to **TRUE** if the component supports remote configuration, and **FALSE** if it does not.</span></span>

</dd> <dt>

<span data-ttu-id="5736d-113">*remoteConfigType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5736d-113">*remoteConfigType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5736d-114">Indica el tipo de configuración remota admitida mediante el valor de la enumeración [**RemoteConfigurationType**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) :</span><span class="sxs-lookup"><span data-stu-id="5736d-114">Indicates the type of remote configuration supported using value from the [**RemoteConfigurationType**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) enumeration:</span></span>



| <span data-ttu-id="5736d-115">Value</span><span class="sxs-lookup"><span data-stu-id="5736d-115">Value</span></span>                                                                                                 | <span data-ttu-id="5736d-116">Significado</span><span class="sxs-lookup"><span data-stu-id="5736d-116">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5736d-117"><dt>remoteConfigTypeMachine</dt></span><span class="sxs-lookup"><span data-stu-id="5736d-117"><dt>remoteConfigTypeMachine</dt></span></span> </dl>    | <span data-ttu-id="5736d-118">Se implementa [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) .</span><span class="sxs-lookup"><span data-stu-id="5736d-118">[**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) is implemented.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="5736d-119"><dt>remoteConfigTypeConfigBlob</dt></span><span class="sxs-lookup"><span data-stu-id="5736d-119"><dt>remoteConfigTypeConfigBlob</dt></span></span> </dl> | <span data-ttu-id="5736d-120">Se implementa [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) .</span><span class="sxs-lookup"><span data-stu-id="5736d-120">[**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) is implemented.</span></span> <span data-ttu-id="5736d-121">Se puede llamar a [**INapComponentConfig:: GetConfig**](inapcomponentconfig-getconfig.md) y [**INapComponentConfig:: SetConfig**](inapcomponentconfig-setconfig.md) de forma remota mediante DCOM.</span><span class="sxs-lookup"><span data-stu-id="5736d-121">[**INapComponentConfig::GetConfig**](inapcomponentconfig-getconfig.md) and [**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md) can be called remotely using DCOM.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5736d-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5736d-122">Return value</span></span>

<span data-ttu-id="5736d-123">Devuelve \_ si es correcto, o uno de los códigos de error estándar de Windows.</span><span class="sxs-lookup"><span data-stu-id="5736d-123">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="5736d-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5736d-124">Remarks</span></span>

<span data-ttu-id="5736d-125">Si no se implementan [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) ni [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) , no es posible la configuración remota del SHV.</span><span class="sxs-lookup"><span data-stu-id="5736d-125">If neither [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) nor [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) are implemented, remote configuration of the SHV is not possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="5736d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5736d-126">Requirements</span></span>



| <span data-ttu-id="5736d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5736d-127">Requirement</span></span> | <span data-ttu-id="5736d-128">Value</span><span class="sxs-lookup"><span data-stu-id="5736d-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5736d-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5736d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5736d-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5736d-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5736d-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5736d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5736d-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5736d-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5736d-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5736d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5736d-134"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5736d-134"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="5736d-135">IDL</span><span class="sxs-lookup"><span data-stu-id="5736d-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5736d-136"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5736d-136"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5736d-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="5736d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5736d-138">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="5736d-138">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





