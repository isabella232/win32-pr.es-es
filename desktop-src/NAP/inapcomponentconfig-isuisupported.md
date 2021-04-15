---
title: Método INapComponentConfig IsUISupported (NapCommon. h)
description: Especifica si el componente admite una interfaz de usuario personalizada.
ms.assetid: 044f8014-f041-4e9c-922a-2691b799ba84
keywords:
- Método IsUISupported NAP
- Método IsUISupported NAP, interfaz INapComponentConfig
- Interfaz INapComponentConfig NAP, método IsUISupported
topic_type:
- apiref
api_name:
- INapComponentConfig.IsUISupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab7d3f6b87ba5e483b466e6746f0f63d039cb205
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676747"
---
# <a name="inapcomponentconfigisuisupported-method"></a><span data-ttu-id="90423-106">INapComponentConfig:: IsUISupported (método)</span><span class="sxs-lookup"><span data-stu-id="90423-106">INapComponentConfig::IsUISupported method</span></span>

> [!Note]  
> <span data-ttu-id="90423-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="90423-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="90423-108">El método **IsUISupported** especifica si el componente admite una interfaz de usuario personalizada.</span><span class="sxs-lookup"><span data-stu-id="90423-108">The **IsUISupported** method specifies whether the component supports a customized user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="90423-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90423-109">Syntax</span></span>


```C++
HRESULT IsUISupported(
  [out] BOOL *isSupported
) const;
```



## <a name="parameters"></a><span data-ttu-id="90423-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90423-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90423-111">*isSupported* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="90423-111">*isSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90423-112">Un puntero a un valor BOOLEANO que se establece en **true** si el componente admite una interfaz de usuario personalizada y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="90423-112">A pointer to a BOOL that is set to **TRUE** if the component supports a customized user interface and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90423-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90423-113">Return value</span></span>

<span data-ttu-id="90423-114">Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="90423-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="90423-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="90423-115">Return code</span></span>                                                                                     | <span data-ttu-id="90423-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="90423-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="90423-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="90423-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="90423-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="90423-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="90423-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="90423-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="90423-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="90423-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="90423-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="90423-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="90423-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="90423-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="90423-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90423-123">Remarks</span></span>

<span data-ttu-id="90423-124">La interfaz de usuario personalizada de un componente se debe iniciar mediante [**INapComponentConfig:: InvokeUI**](inapcomponentconfig-invokeui.md).</span><span class="sxs-lookup"><span data-stu-id="90423-124">A component's customized user interface should be launched using [**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90423-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90423-125">Requirements</span></span>



| <span data-ttu-id="90423-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="90423-126">Requirement</span></span> | <span data-ttu-id="90423-127">Value</span><span class="sxs-lookup"><span data-stu-id="90423-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="90423-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90423-128">Minimum supported client</span></span><br/> | <span data-ttu-id="90423-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="90423-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="90423-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90423-130">Minimum supported server</span></span><br/> | <span data-ttu-id="90423-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="90423-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="90423-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90423-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="90423-133"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="90423-133"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="90423-134">IDL</span><span class="sxs-lookup"><span data-stu-id="90423-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="90423-135"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="90423-135"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90423-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="90423-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90423-137">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="90423-137">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="90423-138">**INapComponentConfig::InvokeUI**</span><span class="sxs-lookup"><span data-stu-id="90423-138">**INapComponentConfig::InvokeUI**</span></span>](inapcomponentconfig-invokeui.md)
</dt> </dl>

 

 





