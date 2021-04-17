---
description: Esta clase está en desuso. En su lugar, se recomienda derivar de la \_ clase de servicio CIM.
ms.assetid: 67b3a96e-4549-41e0-8097-f8d145df0c49
title: CIM_NetworkService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkService
- CIM_NetworkService.Keywords
- CIM_NetworkService.ServiceURL
- CIM_NetworkService.StartupConditions
- CIM_NetworkService.StartupParameters
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b141e6e38f2fafefdf6e75670b975e0fcdd2961c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688376"
---
# <a name="cim_networkservice-class"></a><span data-ttu-id="deeb2-104">Clase de NetworkService de CIM \_</span><span class="sxs-lookup"><span data-stu-id="deeb2-104">CIM\_NetworkService class</span></span>

<span data-ttu-id="deeb2-105">Esta clase está en desuso.</span><span class="sxs-lookup"><span data-stu-id="deeb2-105">This class is deprecated.</span></span> <span data-ttu-id="deeb2-106">En su lugar, se recomienda derivar de la clase de [**\_ servicio CIM**](cim-service.md) .</span><span class="sxs-lookup"><span data-stu-id="deeb2-106">Instead, we recommend deriving from the [**CIM\_Service**](cim-service.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="deeb2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="deeb2-107">Syntax</span></span>

``` syntax
[Deprecated("CIM_Service"), Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::RoutingForwarding"), AMENDMENT]
class CIM_NetworkService : CIM_Service
{
  string Keywords[];
  string ServiceURL;
  string StartupConditions[];
  string StartupParameters[];
};
```

## <a name="members"></a><span data-ttu-id="deeb2-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="deeb2-108">Members</span></span>

<span data-ttu-id="deeb2-109">La clase de **\_ NetworkService de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="deeb2-109">The **CIM\_NetworkService** class has these types of members:</span></span>

-   [<span data-ttu-id="deeb2-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="deeb2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="deeb2-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="deeb2-111">Properties</span></span>

<span data-ttu-id="deeb2-112">La clase de **\_ NetworkService de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="deeb2-112">The **CIM\_NetworkService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="deeb2-113">**Palabras clave**</span><span class="sxs-lookup"><span data-stu-id="deeb2-113">**Keywords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deeb2-114">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="deeb2-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="deeb2-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="deeb2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="deeb2-116">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sin valor")</span><span class="sxs-lookup"><span data-stu-id="deeb2-116">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="deeb2-117">Esta propiedad está en desuso y no debe utilizarse.</span><span class="sxs-lookup"><span data-stu-id="deeb2-117">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="deeb2-118">Descripción desusada: una matriz de palabras clave que se pueden usar en las consultas.</span><span class="sxs-lookup"><span data-stu-id="deeb2-118">Deprecated description: An array of keywords that can be used in queries.</span></span>

 

</dd> <dt>

<span data-ttu-id="deeb2-119">**ServiceURL**</span><span class="sxs-lookup"><span data-stu-id="deeb2-119">**ServiceURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deeb2-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="deeb2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deeb2-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="deeb2-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="deeb2-122">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ ServiceAccessURI")</span><span class="sxs-lookup"><span data-stu-id="deeb2-122">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_ServiceAccessURI")</span></span>
</dt> </dl>

<span data-ttu-id="deeb2-123">Esta propiedad está desusada.</span><span class="sxs-lookup"><span data-stu-id="deeb2-123">This property is deprecated.</span></span> <span data-ttu-id="deeb2-124">En su lugar, se recomienda la clase **CIM \_ ServiceAccessURI** .</span><span class="sxs-lookup"><span data-stu-id="deeb2-124">Instead, we recommend the **CIM\_ServiceAccessURI** class.</span></span>

> [!Note]  
> <span data-ttu-id="deeb2-125">Descripción desusada: una dirección URL que proporciona el protocolo, la ubicación de red y otra información específica del servicio necesaria para obtener acceso al servicio.</span><span class="sxs-lookup"><span data-stu-id="deeb2-125">Deprecated description: A URL that provides the protocol, network location, and other service-specific information required in order to access the service.</span></span>

 

</dd> <dt>

<span data-ttu-id="deeb2-126">**StartupConditions**</span><span class="sxs-lookup"><span data-stu-id="deeb2-126">**StartupConditions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deeb2-127">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="deeb2-127">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="deeb2-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="deeb2-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="deeb2-129">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sin valor")</span><span class="sxs-lookup"><span data-stu-id="deeb2-129">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="deeb2-130">Esta propiedad está en desuso y no debe utilizarse.</span><span class="sxs-lookup"><span data-stu-id="deeb2-130">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="deeb2-131">Descripción desusada: las condiciones previas que deben cumplirse para que este servicio se inicie correctamente.</span><span class="sxs-lookup"><span data-stu-id="deeb2-131">Deprecated description: The pre-conditions that must be met in order for this service to start correctly.</span></span>

 

</dd> <dt>

<span data-ttu-id="deeb2-132">**StartupParameters**</span><span class="sxs-lookup"><span data-stu-id="deeb2-132">**StartupParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deeb2-133">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="deeb2-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="deeb2-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="deeb2-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="deeb2-135">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sin valor")</span><span class="sxs-lookup"><span data-stu-id="deeb2-135">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="deeb2-136">Esta propiedad está en desuso y no debe utilizarse.</span><span class="sxs-lookup"><span data-stu-id="deeb2-136">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="deeb2-137">Descripción desusada: los parámetros que se deben proporcionar al método **StartService** para que este servicio se inicie correctamente.</span><span class="sxs-lookup"><span data-stu-id="deeb2-137">Deprecated description: The parameters that must be supplied to the **StartService** method in order for this service to start correctly.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="deeb2-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="deeb2-138">Requirements</span></span>



| <span data-ttu-id="deeb2-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="deeb2-139">Requirement</span></span> | <span data-ttu-id="deeb2-140">Value</span><span class="sxs-lookup"><span data-stu-id="deeb2-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="deeb2-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="deeb2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="deeb2-142">Windows 8</span><span class="sxs-lookup"><span data-stu-id="deeb2-142">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="deeb2-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="deeb2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="deeb2-144">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="deeb2-144">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="deeb2-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="deeb2-145">Namespace</span></span><br/>                | <span data-ttu-id="deeb2-146">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="deeb2-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="deeb2-147">MOF</span><span class="sxs-lookup"><span data-stu-id="deeb2-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="deeb2-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="deeb2-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="deeb2-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="deeb2-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="deeb2-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="deeb2-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="deeb2-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="deeb2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deeb2-152">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="deeb2-152">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

