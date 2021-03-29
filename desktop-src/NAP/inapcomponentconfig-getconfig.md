---
title: Método GetConfig de INapComponentConfig (NapCommon. h)
description: Recupera la configuración del componente de validador de mantenimiento del sistema (SHV).
ms.assetid: 57a1d3a7-05c0-4e0f-91b8-b3cf8982d04f
keywords:
- GetConfig (método) NAP
- Método GetConfig NAP, interfaz INapComponentConfig
- Interfaz INapComponentConfig NAP, método GetConfig
topic_type:
- apiref
api_name:
- INapComponentConfig.GetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e07465d768c8902166150e53d4200e775e2597
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492335"
---
# <a name="inapcomponentconfiggetconfig-method"></a><span data-ttu-id="bbc5e-106">INapComponentConfig:: GetConfig (método)</span><span class="sxs-lookup"><span data-stu-id="bbc5e-106">INapComponentConfig::GetConfig method</span></span>

> [!Note]  
> <span data-ttu-id="bbc5e-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="bbc5e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="bbc5e-108">El método **GetConfig** recupera la configuración del componente de validador de mantenimiento del sistema (SHV).</span><span class="sxs-lookup"><span data-stu-id="bbc5e-108">The **GetConfig** method retrieves the system health validator (SHV) component configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbc5e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bbc5e-109">Syntax</span></span>


```C++
HRESULT GetConfig(
  [out] UINT16 *bCount,
  [out] BYTE   **data
) const;
```



## <a name="parameters"></a><span data-ttu-id="bbc5e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bbc5e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbc5e-111">*bCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bbc5e-111">*bCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bbc5e-112">Tamaño, en bytes, del BLOB de configuración de *datos* .</span><span class="sxs-lookup"><span data-stu-id="bbc5e-112">The size, in bytes, of the *data* configuration blob.</span></span>

</dd> <dt>

<span data-ttu-id="bbc5e-113">*datos* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bbc5e-113">*data* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bbc5e-114">Puntero a la dirección de los datos de configuración del componente de SHV.</span><span class="sxs-lookup"><span data-stu-id="bbc5e-114">A pointer to the address of the SHV component configuration data.</span></span>

> [!Note]  
> <span data-ttu-id="bbc5e-115">Los datos de configuración exportados desde un equipo x86 mediante el método **GetConfig** se pueden importar en un equipo x64 mediante el método [**SetConfig**](inapcomponentconfig-setconfig.md) y viceversa.</span><span class="sxs-lookup"><span data-stu-id="bbc5e-115">Configuration data exported from an x86 machine using the **GetConfig** method may be imported onto an x64 machine using the [**SetConfig**](inapcomponentconfig-setconfig.md) method, and vice versa.</span></span> <span data-ttu-id="bbc5e-116">Por lo tanto, los datos de configuración deben estar en un formato independiente de la arquitectura, como XML.</span><span class="sxs-lookup"><span data-stu-id="bbc5e-116">Therefore, configuration data must be in an architecture-agnostic format such as XML.</span></span> <span data-ttu-id="bbc5e-117">El uso de XML en lugar de un flujo de bytes facilita el uso de datos de configuración en diferentes arquitecturas.</span><span class="sxs-lookup"><span data-stu-id="bbc5e-117">Using XML instead of a byte stream makes it easier to use configuration data on different architectures.</span></span> <span data-ttu-id="bbc5e-118">El implementador determina los elementos XML utilizados en los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="bbc5e-118">The XML elements used in the configuration data are determined by the implementer.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbc5e-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bbc5e-119">Return value</span></span>

<span data-ttu-id="bbc5e-120">Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="bbc5e-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="bbc5e-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bbc5e-121">Return code</span></span>                                                                                     | <span data-ttu-id="bbc5e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbc5e-122">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="bbc5e-123"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="bbc5e-123"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="bbc5e-124">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="bbc5e-124">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="bbc5e-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="bbc5e-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="bbc5e-126">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="bbc5e-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="bbc5e-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bbc5e-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="bbc5e-128">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="bbc5e-128">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bbc5e-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bbc5e-129">Remarks</span></span>

<span data-ttu-id="bbc5e-130">El destinatario (implementador de componentes) debe asignar el parámetro de datos mediante **CoTaskMemAlloc** y el autor de la llamada lo libera mediante **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="bbc5e-130">The data parameter must be allocated by the callee (component implementor) using **CoTaskMemAlloc** and freed by the caller using **CoTaskMemFree**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbc5e-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbc5e-131">Requirements</span></span>



| <span data-ttu-id="bbc5e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbc5e-132">Requirement</span></span> | <span data-ttu-id="bbc5e-133">Value</span><span class="sxs-lookup"><span data-stu-id="bbc5e-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc5e-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbc5e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bbc5e-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bbc5e-135">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bbc5e-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbc5e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bbc5e-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bbc5e-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bbc5e-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bbc5e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbc5e-139"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbc5e-139"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="bbc5e-140">IDL</span><span class="sxs-lookup"><span data-stu-id="bbc5e-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bbc5e-141"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bbc5e-141"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbc5e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbc5e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbc5e-143">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="bbc5e-143">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="bbc5e-144">**INapComponentConfig::SetConfig**</span><span class="sxs-lookup"><span data-stu-id="bbc5e-144">**INapComponentConfig::SetConfig**</span></span>](inapcomponentconfig-setconfig.md)
</dt> </dl>

 

 





