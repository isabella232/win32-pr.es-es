---
title: Interfaz INapComponentConfig3 (NapCommon. h)
description: Proporciona métodos de configuración del sistema NAP para que los validadores de mantenimiento del sistema (SHV) establezcan y modifiquen los datos de configuración de un identificador de configuración específico.
ms.assetid: dbb78f7a-7c6b-4bf1-b471-374857d5dafe
keywords:
- Interfaz INapComponentConfig3 NAP
- Interfaz INapComponentConfig3 NAP, descripción
topic_type:
- apiref
api_name:
- INapComponentConfig3
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac0cfead891da106a1a950ba83b9108b5950a738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676582"
---
# <a name="inapcomponentconfig3-interface"></a><span data-ttu-id="61bc8-105">Interfaz INapComponentConfig3</span><span class="sxs-lookup"><span data-stu-id="61bc8-105">INapComponentConfig3 interface</span></span>

> [!Note]  
> <span data-ttu-id="61bc8-106">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="61bc8-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="61bc8-107">La interfaz **INapComponentConfig3** proporciona métodos de configuración del sistema de NAP para que los validadores de mantenimiento del sistema (SHV) establezcan y modifiquen los datos de configuración de un identificador de configuración específico.</span><span class="sxs-lookup"><span data-stu-id="61bc8-107">The **INapComponentConfig3** interface provides NAP system configuration methods for system health validators (SHVs) to set and modify configuration data for a specific configuration ID.</span></span>

> [!Note]  
> <span data-ttu-id="61bc8-108">Esta interfaz hereda todos los métodos de [**INapComponentConfig2**](inapcomponentconfig2.md) y se debe usar en su lugar.</span><span class="sxs-lookup"><span data-stu-id="61bc8-108">This interface inherits all the methods of [**INapComponentConfig2**](inapcomponentconfig2.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="61bc8-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="61bc8-109">Members</span></span>

<span data-ttu-id="61bc8-110">La interfaz **INapComponentConfig3** hereda de [**INapComponentConfig2**](inapcomponentconfig2.md).</span><span class="sxs-lookup"><span data-stu-id="61bc8-110">The **INapComponentConfig3** interface inherits from [**INapComponentConfig2**](inapcomponentconfig2.md).</span></span> <span data-ttu-id="61bc8-111">**INapComponentConfig3** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="61bc8-111">**INapComponentConfig3** also has these types of members:</span></span>

-   [<span data-ttu-id="61bc8-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="61bc8-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="61bc8-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="61bc8-113">Methods</span></span>

<span data-ttu-id="61bc8-114">La interfaz **INapComponentConfig3** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="61bc8-114">The **INapComponentConfig3** interface has these methods.</span></span>



| <span data-ttu-id="61bc8-115">Método</span><span class="sxs-lookup"><span data-stu-id="61bc8-115">Method</span></span>                                                                                | <span data-ttu-id="61bc8-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="61bc8-116">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61bc8-117">**INapComponentConfig3::D eleteAllConfig**</span><span class="sxs-lookup"><span data-stu-id="61bc8-117">**INapComponentConfig3::DeleteAllConfig**</span></span>](inapcomponentconfig3-deleteallconfig.md) | <span data-ttu-id="61bc8-118">Implementado por SHV para proporcionar una manera de restablecer el almacén de SHV a su estado original después de la instalación.</span><span class="sxs-lookup"><span data-stu-id="61bc8-118">Implemented by SHVs to provide a way to reset the SHV store to its original state after setup.</span></span><br/>      |
| [<span data-ttu-id="61bc8-119">**INapComponentConfig3::D eleteConfig**</span><span class="sxs-lookup"><span data-stu-id="61bc8-119">**INapComponentConfig3::DeleteConfig**</span></span>](inapcomponentconfig3-deleteconfig.md)       | <span data-ttu-id="61bc8-120">Implementado por SHV para proporcionar una manera de eliminar los datos de configuración de un identificador de configuración específico.</span><span class="sxs-lookup"><span data-stu-id="61bc8-120">Implemented by SHVs to provide a way to delete configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="61bc8-121">**INapComponentConfig3::GetConfigFromID**</span><span class="sxs-lookup"><span data-stu-id="61bc8-121">**INapComponentConfig3::GetConfigFromID**</span></span>](inapcomponentconfig3-getconfigfromid.md) | <span data-ttu-id="61bc8-122">Implementado por SHV para proporcionar una manera de obtener datos de configuración para un identificador de configuración específico.</span><span class="sxs-lookup"><span data-stu-id="61bc8-122">Implemented by SHVs to provide a way to obtain configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="61bc8-123">**INapComponentConfig3:: documento newconfig**</span><span class="sxs-lookup"><span data-stu-id="61bc8-123">**INapComponentConfig3::NewConfig**</span></span>](inapcomponentconfig3-newconfig.md)             | <span data-ttu-id="61bc8-124">Implementado por SHV para proporcionar una manera de crear datos de configuración para un identificador de configuración específico.</span><span class="sxs-lookup"><span data-stu-id="61bc8-124">Implemented by SHVs to provide a way to create configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="61bc8-125">**INapComponentConfig3::SetConfigToID**</span><span class="sxs-lookup"><span data-stu-id="61bc8-125">**INapComponentConfig3::SetConfigToID**</span></span>](inapcomponentconfig3-setconfigtoid.md)     | <span data-ttu-id="61bc8-126">Implementado por SHV para proporcionar una manera de establecer los datos de configuración para un identificador de configuración específico.</span><span class="sxs-lookup"><span data-stu-id="61bc8-126">Implemented by SHVs to provide a way to set the configuration data for a specific configuration ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="61bc8-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61bc8-127">Remarks</span></span>

<span data-ttu-id="61bc8-128">Esta interfaz no debe ser implementada por los agentes de mantenimiento del sistema (SHA) o los clientes de aplicación de cuarentena (QECs).</span><span class="sxs-lookup"><span data-stu-id="61bc8-128">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="61bc8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61bc8-129">Requirements</span></span>



| <span data-ttu-id="61bc8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="61bc8-130">Requirement</span></span> | <span data-ttu-id="61bc8-131">Value</span><span class="sxs-lookup"><span data-stu-id="61bc8-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="61bc8-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61bc8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="61bc8-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="61bc8-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="61bc8-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61bc8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="61bc8-135">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="61bc8-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61bc8-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61bc8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="61bc8-137"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="61bc8-137"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="61bc8-138">IDL</span><span class="sxs-lookup"><span data-stu-id="61bc8-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="61bc8-139"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="61bc8-139"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61bc8-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="61bc8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61bc8-141">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="61bc8-141">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> <dt>

[<span data-ttu-id="61bc8-142">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="61bc8-142">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="61bc8-143">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="61bc8-143">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





