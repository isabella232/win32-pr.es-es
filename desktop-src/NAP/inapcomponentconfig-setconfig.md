---
title: Método INapComponentConfig SetConfig (NapCommon. h)
description: Establece la configuración del componente de validador de mantenimiento del sistema (SHV).
ms.assetid: ec27e30b-4205-40bc-a24b-61072a746e53
keywords:
- Método SetConfig NAP
- Método SetConfig NAP, interfaz INapComponentConfig
- Interfaz INapComponentConfig NAP, método SetConfig
topic_type:
- apiref
api_name:
- INapComponentConfig.SetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1f3d557517ec27f9537a7cbcd46be9e2cd107e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535613"
---
# <a name="inapcomponentconfigsetconfig-method"></a><span data-ttu-id="489f0-106">INapComponentConfig:: SetConfig (método)</span><span class="sxs-lookup"><span data-stu-id="489f0-106">INapComponentConfig::SetConfig method</span></span>

> [!Note]  
> <span data-ttu-id="489f0-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="489f0-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="489f0-108">El método **SetConfig** establece la configuración del componente de validador de mantenimiento del sistema (SHV).</span><span class="sxs-lookup"><span data-stu-id="489f0-108">The **SetConfig** method sets the system health validator (SHV) component configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="489f0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="489f0-109">Syntax</span></span>


```C++
HRESULT SetConfig(
  [in] UINT16 bCount,
  [in] BYTE   *data
);
```



## <a name="parameters"></a><span data-ttu-id="489f0-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="489f0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="489f0-111">*bCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="489f0-111">*bCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="489f0-112">Tamaño, en bytes, del BLOB de configuración de *datos* .</span><span class="sxs-lookup"><span data-stu-id="489f0-112">The size, in bytes, of the *data* configuration blob.</span></span>

</dd> <dt>

<span data-ttu-id="489f0-113">*datos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="489f0-113">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="489f0-114">Puntero a los datos de configuración del componente de SHV.</span><span class="sxs-lookup"><span data-stu-id="489f0-114">A pointer to the SHV component configuration data.</span></span>

> [!Note]  
> <span data-ttu-id="489f0-115">Los datos de configuración exportados desde un equipo x86 mediante el método [**GetConfig**](inapcomponentconfig-getconfig.md) se pueden importar en un equipo x64 mediante el método **SetConfig** y viceversa.</span><span class="sxs-lookup"><span data-stu-id="489f0-115">Configuration data exported from an x86 machine using the [**GetConfig**](inapcomponentconfig-getconfig.md) method may be imported onto an x64 machine using the **SetConfig** method, and vice versa.</span></span> <span data-ttu-id="489f0-116">Por lo tanto, los datos de configuración deben estar en un formato independiente de la arquitectura, como XML.</span><span class="sxs-lookup"><span data-stu-id="489f0-116">Therefore, configuration data must be in an architecture-agnostic format such as XML.</span></span> <span data-ttu-id="489f0-117">El uso de XML en lugar de un flujo de bytes facilita el uso de datos de configuración en diferentes arquitecturas.</span><span class="sxs-lookup"><span data-stu-id="489f0-117">Using XML instead of a byte stream makes it easier to use configuration data on different architectures.</span></span> <span data-ttu-id="489f0-118">El implementador determina los elementos XML utilizados en los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="489f0-118">The XML elements used in the configuration data are determined by the implementer.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="489f0-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="489f0-119">Return value</span></span>

<span data-ttu-id="489f0-120">Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="489f0-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="489f0-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="489f0-121">Return code</span></span>                                                                                     | <span data-ttu-id="489f0-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="489f0-122">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="489f0-123"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="489f0-123"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="489f0-124">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="489f0-124">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="489f0-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="489f0-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="489f0-126">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="489f0-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="489f0-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="489f0-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="489f0-128">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="489f0-128">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="489f0-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="489f0-129">Remarks</span></span>

<span data-ttu-id="489f0-130">La información de control de versiones de componentes debe incluirse en el BLOB de configuración de *datos* .</span><span class="sxs-lookup"><span data-stu-id="489f0-130">Component versioning information should be included in the *data* configuration blob.</span></span> <span data-ttu-id="489f0-131">Se puede usar la información de control de versiones al migrar de una versión de SHV a otra.</span><span class="sxs-lookup"><span data-stu-id="489f0-131">The versioning information may be used when migrating from one SHV version to another.</span></span>

## <a name="requirements"></a><span data-ttu-id="489f0-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="489f0-132">Requirements</span></span>



| <span data-ttu-id="489f0-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="489f0-133">Requirement</span></span> | <span data-ttu-id="489f0-134">Value</span><span class="sxs-lookup"><span data-stu-id="489f0-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="489f0-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="489f0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="489f0-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="489f0-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="489f0-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="489f0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="489f0-138">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="489f0-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="489f0-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="489f0-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="489f0-140"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="489f0-140"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="489f0-141">IDL</span><span class="sxs-lookup"><span data-stu-id="489f0-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="489f0-142"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="489f0-142"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="489f0-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="489f0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="489f0-144">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="489f0-144">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="489f0-145">**INapConponentConfig:: GetConfig**</span><span class="sxs-lookup"><span data-stu-id="489f0-145">**INapConponentConfig::GetConfig**</span></span>](inapcomponentconfig-getconfig.md)
</dt> </dl>

 

 





