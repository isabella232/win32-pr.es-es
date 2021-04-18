---
title: Interfaz INapComponentConfig (NapCommon. h)
description: Proporciona métodos de configuración del sistema NAP para los validadores de mantenimiento del sistema (SHV).
ms.assetid: 979b5c34-8efe-4c48-8236-53fbd25d4249
keywords:
- Interfaz INapComponentConfig NAP
- Interfaz INapComponentConfig NAP, descripción
topic_type:
- apiref
api_name:
- INapComponentConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63a13ae74ba1de79803ff4a2d3716eec7fe934a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422179"
---
# <a name="inapcomponentconfig-interface"></a><span data-ttu-id="67897-105">Interfaz INapComponentConfig</span><span class="sxs-lookup"><span data-stu-id="67897-105">INapComponentConfig interface</span></span>

> [!Note]  
> <span data-ttu-id="67897-106">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="67897-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="67897-107">La interfaz **INapComponentConfig** proporciona métodos de configuración del sistema NAP para los validadores de mantenimiento del sistema (SHV).</span><span class="sxs-lookup"><span data-stu-id="67897-107">The **INapComponentConfig** interface provides NAP system configuration methods for system health validators (SHVs).</span></span>

> [!Note]  
> <span data-ttu-id="67897-108">[**INapComponentConfig2**](inapcomponentconfig2.md) y [**INapComponentConfig3**](inapcomponentconfig3.md) heredan todos los métodos de esta interfaz y deben usarse en su lugar.</span><span class="sxs-lookup"><span data-stu-id="67897-108">[**INapComponentConfig2**](inapcomponentconfig2.md) and [**INapComponentConfig3**](inapcomponentconfig3.md) inherit all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="67897-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="67897-109">Members</span></span>

<span data-ttu-id="67897-110">La interfaz **INapComponentConfig** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="67897-110">The **INapComponentConfig** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="67897-111">**INapComponentConfig** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="67897-111">**INapComponentConfig** also has these types of members:</span></span>

-   [<span data-ttu-id="67897-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="67897-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="67897-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="67897-113">Methods</span></span>

<span data-ttu-id="67897-114">La interfaz **INapComponentConfig** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="67897-114">The **INapComponentConfig** interface has these methods.</span></span>



| <span data-ttu-id="67897-115">Método</span><span class="sxs-lookup"><span data-stu-id="67897-115">Method</span></span>                                                                          | <span data-ttu-id="67897-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="67897-116">Description</span></span>                                                                          |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="67897-117">**INapComponentConfig:: GetConfig**</span><span class="sxs-lookup"><span data-stu-id="67897-117">**INapComponentConfig::GetConfig**</span></span>](inapcomponentconfig-getconfig.md)         | <span data-ttu-id="67897-118">Recupera la configuración del componente SHV.</span><span class="sxs-lookup"><span data-stu-id="67897-118">Retrieves the SHV component configuration.</span></span><br/>                                |
| [<span data-ttu-id="67897-119">**INapComponentConfig::InvokeUI**</span><span class="sxs-lookup"><span data-stu-id="67897-119">**INapComponentConfig::InvokeUI**</span></span>](inapcomponentconfig-invokeui.md)           | <span data-ttu-id="67897-120">Inicia la interfaz de usuario personalizada para un componente de SHV.</span><span class="sxs-lookup"><span data-stu-id="67897-120">Launches the customized user interface for an SHV component.</span></span><br/>              |
| [<span data-ttu-id="67897-121">**INapComponentConfig::IsUISupported**</span><span class="sxs-lookup"><span data-stu-id="67897-121">**INapComponentConfig::IsUISupported**</span></span>](inapcomponentconfig-isuisupported.md) | <span data-ttu-id="67897-122">Especifica si el componente de SHV admite una interfaz de usuario personalizada.</span><span class="sxs-lookup"><span data-stu-id="67897-122">Specifies whether the SHV component supports a customized user interface.</span></span><br/> |
| [<span data-ttu-id="67897-123">**INapComponentConfig::SetConfig**</span><span class="sxs-lookup"><span data-stu-id="67897-123">**INapComponentConfig::SetConfig**</span></span>](inapcomponentconfig-setconfig.md)         | <span data-ttu-id="67897-124">Establece la configuración del componente SHV.</span><span class="sxs-lookup"><span data-stu-id="67897-124">Sets the SHV component configuration.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="67897-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67897-125">Remarks</span></span>

<span data-ttu-id="67897-126">Esta interfaz no debe ser implementada por los agentes de mantenimiento del sistema (SHA) o los clientes de aplicación de cuarentena (QECs).</span><span class="sxs-lookup"><span data-stu-id="67897-126">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="67897-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67897-127">Requirements</span></span>



| <span data-ttu-id="67897-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="67897-128">Requirement</span></span> | <span data-ttu-id="67897-129">Value</span><span class="sxs-lookup"><span data-stu-id="67897-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="67897-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67897-130">Minimum supported client</span></span><br/> | <span data-ttu-id="67897-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="67897-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="67897-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67897-132">Minimum supported server</span></span><br/> | <span data-ttu-id="67897-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="67897-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="67897-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67897-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="67897-135"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="67897-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="67897-136">IDL</span><span class="sxs-lookup"><span data-stu-id="67897-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="67897-137"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="67897-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67897-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="67897-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67897-139">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="67897-139">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="67897-140">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="67897-140">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

