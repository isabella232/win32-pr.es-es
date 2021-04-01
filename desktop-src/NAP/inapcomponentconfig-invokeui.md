---
title: Método INapComponentConfig InvokeUI (NapCommon. h)
description: Inicia una interfaz de usuario personalizada para un componente de validador de mantenimiento del sistema (SHV).
ms.assetid: da2a5e3e-bc17-4984-bdbe-b72e9e710a9d
keywords:
- Método InvokeUI NAP
- Método InvokeUI NAP, interfaz INapComponentConfig
- Interfaz INapComponentConfig NAP, método InvokeUI
topic_type:
- apiref
api_name:
- INapComponentConfig.InvokeUI
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd86d683365286fc2130c1ac9edf21ff075d61a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996188"
---
# <a name="inapcomponentconfiginvokeui-method"></a><span data-ttu-id="94075-106">INapComponentConfig:: InvokeUI (método)</span><span class="sxs-lookup"><span data-stu-id="94075-106">INapComponentConfig::InvokeUI method</span></span>

> [!Note]  
> <span data-ttu-id="94075-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="94075-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="94075-108">El método **InvokeUI** inicia una interfaz de usuario personalizada para un componente de validador de mantenimiento del sistema (SHV).</span><span class="sxs-lookup"><span data-stu-id="94075-108">The **InvokeUI** method launches a customized user interface for a system health validator (SHV) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="94075-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94075-109">Syntax</span></span>


```C++
HRESULT InvokeUI(
  [in] HWND hwndParent
) const;
```



## <a name="parameters"></a><span data-ttu-id="94075-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94075-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94075-111">*hwndParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="94075-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94075-112">Identificador de la ventana primaria o propietaria.</span><span class="sxs-lookup"><span data-stu-id="94075-112">A handle to the parent or owner window.</span></span> <span data-ttu-id="94075-113">Se debe proporcionar un identificador de ventana válido.</span><span class="sxs-lookup"><span data-stu-id="94075-113">A valid window handle must be supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94075-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94075-114">Return value</span></span>

<span data-ttu-id="94075-115">Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="94075-115">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="94075-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="94075-116">Return code</span></span>                                                                                     | <span data-ttu-id="94075-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="94075-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="94075-118"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="94075-118"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="94075-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="94075-119">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="94075-120"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="94075-120"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="94075-121">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="94075-121">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="94075-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="94075-122"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="94075-123">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="94075-123">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="94075-124"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="94075-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>       | <span data-ttu-id="94075-125">El SHV no es compatible con una interfaz de usuario personalizada.</span><span class="sxs-lookup"><span data-stu-id="94075-125">The SHV does not support a customized UI.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="94075-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94075-126">Remarks</span></span>

<span data-ttu-id="94075-127">Esta llamada al método debe bloquearse hasta que se cierre la interfaz de usuario de SHV.</span><span class="sxs-lookup"><span data-stu-id="94075-127">This method call should block until the SHV user interface exits.</span></span>

## <a name="requirements"></a><span data-ttu-id="94075-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94075-128">Requirements</span></span>



| <span data-ttu-id="94075-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="94075-129">Requirement</span></span> | <span data-ttu-id="94075-130">Value</span><span class="sxs-lookup"><span data-stu-id="94075-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="94075-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94075-131">Minimum supported client</span></span><br/> | <span data-ttu-id="94075-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="94075-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="94075-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94075-133">Minimum supported server</span></span><br/> | <span data-ttu-id="94075-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="94075-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="94075-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94075-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="94075-136"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="94075-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="94075-137">IDL</span><span class="sxs-lookup"><span data-stu-id="94075-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="94075-138"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="94075-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94075-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="94075-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94075-140">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="94075-140">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="94075-141">**INapComponentConfig::IsUISupported**</span><span class="sxs-lookup"><span data-stu-id="94075-141">**INapComponentConfig::IsUISupported**</span></span>](inapcomponentconfig-isuisupported.md)
</dt> </dl>

 

 





