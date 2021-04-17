---
description: Representa un elemento lógico que contiene información para representar y administrar la funcionalidad proporcionada por una característica de dispositivo o software.
ms.assetid: 0b2312da-433b-43d8-8d21-babab12a5b2c
title: CIM_Service (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.PrimaryOwnerName
- CIM_Service.PrimaryOwnerContact
- CIM_Service.StartMode
- CIM_Service.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b6ee3c51b6af50d77e94bb0a29bd1c8148cda8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666566"
---
# <a name="cim_service-class-hyper-v-management"></a><span data-ttu-id="29dc9-103">CIM_Service (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="29dc9-103">CIM_Service class (Hyper-V management)</span></span>

<span data-ttu-id="29dc9-104">Representa un elemento lógico que contiene información para representar y administrar la funcionalidad proporcionada por una característica de dispositivo o software.</span><span class="sxs-lookup"><span data-stu-id="29dc9-104">Represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="29dc9-105">Un servicio es un objeto de uso general para configurar y administrar la implementación de la funcionalidad. no es la propia funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="29dc9-105">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="29dc9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29dc9-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_Service : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  Name;
  string  PrimaryOwnerName;
  string  PrimaryOwnerContact;
  string  StartMode;
  boolean Started;
};
```

## <a name="members"></a><span data-ttu-id="29dc9-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="29dc9-107">Members</span></span>

<span data-ttu-id="29dc9-108">La clase de **\_ servicio CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="29dc9-108">The **CIM\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="29dc9-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="29dc9-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="29dc9-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="29dc9-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="29dc9-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="29dc9-111">Methods</span></span>

<span data-ttu-id="29dc9-112">La clase de **\_ servicio CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="29dc9-112">The **CIM\_Service** class has these methods.</span></span>



| <span data-ttu-id="29dc9-113">Método</span><span class="sxs-lookup"><span data-stu-id="29dc9-113">Method</span></span>                                           | <span data-ttu-id="29dc9-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="29dc9-114">Description</span></span>                    |
|:-------------------------------------------------|:-------------------------------|
| [<span data-ttu-id="29dc9-115">**StartService**</span><span class="sxs-lookup"><span data-stu-id="29dc9-115">**StartService**</span></span>](cim-service-startservice.md) | <span data-ttu-id="29dc9-116">inicia el servicio.</span><span class="sxs-lookup"><span data-stu-id="29dc9-116">Starts the service.</span></span><br/> |
| [<span data-ttu-id="29dc9-117">**StopService**</span><span class="sxs-lookup"><span data-stu-id="29dc9-117">**StopService**</span></span>](cim-service-stopservice.md)   | <span data-ttu-id="29dc9-118">detiene el servicio.</span><span class="sxs-lookup"><span data-stu-id="29dc9-118">Stops the service.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="29dc9-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="29dc9-119">Properties</span></span>

<span data-ttu-id="29dc9-120">La clase de **\_ servicio CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="29dc9-120">The **CIM\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="29dc9-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="29dc9-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29dc9-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="29dc9-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29dc9-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29dc9-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29dc9-124">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="29dc9-124">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="29dc9-125">Nombre de clase utilizado para crear una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="29dc9-125">The class name used to create an instance of this class.</span></span> <span data-ttu-id="29dc9-126">**CreationClassName** se combina con otras propiedades de clave de esta clase para identificar de forma única las instancias de esta clase y sus subclases.</span><span class="sxs-lookup"><span data-stu-id="29dc9-126">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="29dc9-127">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="29dc9-127">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29dc9-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="29dc9-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29dc9-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29dc9-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29dc9-130">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="29dc9-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="29dc9-131">Identificador único del servicio que indica la funcionalidad del servicio.</span><span class="sxs-lookup"><span data-stu-id="29dc9-131">A unique identifier of the service that indicates the functionality of the service.</span></span>

</dd> <dt>

<span data-ttu-id="29dc9-132">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="29dc9-132">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29dc9-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="29dc9-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29dc9-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="29dc9-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="29dc9-135">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información general de DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="29dc9-135">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="29dc9-136">Información de contacto del propietario principal del servicio.</span><span class="sxs-lookup"><span data-stu-id="29dc9-136">Contact information for the primary owner of the service.</span></span>

</dd> <dt>

<span data-ttu-id="29dc9-137">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="29dc9-137">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29dc9-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="29dc9-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29dc9-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="29dc9-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="29dc9-140">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información general de DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="29dc9-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="29dc9-141">Nombre del propietario principal del servicio.</span><span class="sxs-lookup"><span data-stu-id="29dc9-141">The name of the primary owner of the service.</span></span>

</dd> <dt>

<span data-ttu-id="29dc9-142">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="29dc9-142">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29dc9-143">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="29dc9-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="29dc9-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29dc9-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29dc9-145">**true** si se ha iniciado el servicio; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="29dc9-145">**true** if the service has been started; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="29dc9-146">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="29dc9-146">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29dc9-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="29dc9-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29dc9-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29dc9-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29dc9-149">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (**" \_ servicio CIM**.**EnabledDefault**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="29dc9-149">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_Service**.**EnabledDefault**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="29dc9-150">Esta propiedad está desusada.</span><span class="sxs-lookup"><span data-stu-id="29dc9-150">This property is deprecated.</span></span> <span data-ttu-id="29dc9-151">En su lugar, use la propiedad **EnabledDefault** que se hereda [**de \_ EnabledLogicalElement CIM**](cim-enabledlogicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="29dc9-151">Instead, use the **EnabledDefault** property that is inherited from [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).</span></span>

> [!Note]  
> <span data-ttu-id="29dc9-152">Descripción en desuso: indica si el servicio se inicia automáticamente (por ejemplo, por un sistema operativo) o solo se inicia después de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="29dc9-152">Deprecated description: Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

 

<dt>



 <span data-ttu-id="29dc9-153">("Automático")</span><span class="sxs-lookup"><span data-stu-id="29dc9-153">("Automatic")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="29dc9-154">("Manual")</span><span class="sxs-lookup"><span data-stu-id="29dc9-154">("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="29dc9-155">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="29dc9-155">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29dc9-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="29dc9-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29dc9-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29dc9-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29dc9-158">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="29dc9-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="29dc9-159">Nombre de clase utilizado para crear una instancia del sistema que contiene el servicio.</span><span class="sxs-lookup"><span data-stu-id="29dc9-159">The class name used to create an instance of the system that contains the service.</span></span> <span data-ttu-id="29dc9-160">**SystemCreationClassName** se combina con otras propiedades clave de esta clase para identificar de forma única las instancias de esta clase y sus subclases.</span><span class="sxs-lookup"><span data-stu-id="29dc9-160">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="29dc9-161">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="29dc9-161">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29dc9-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="29dc9-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29dc9-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29dc9-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29dc9-164">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**")</span><span class="sxs-lookup"><span data-stu-id="29dc9-164">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="29dc9-165">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="29dc9-165">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29dc9-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29dc9-166">Requirements</span></span>



| <span data-ttu-id="29dc9-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="29dc9-167">Requirement</span></span> | <span data-ttu-id="29dc9-168">Value</span><span class="sxs-lookup"><span data-stu-id="29dc9-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29dc9-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29dc9-169">Minimum supported client</span></span><br/> | <span data-ttu-id="29dc9-170">Windows 8</span><span class="sxs-lookup"><span data-stu-id="29dc9-170">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="29dc9-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29dc9-171">Minimum supported server</span></span><br/> | <span data-ttu-id="29dc9-172">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29dc9-172">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="29dc9-173">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="29dc9-173">Namespace</span></span><br/>                | <span data-ttu-id="29dc9-174">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="29dc9-174">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="29dc9-175">MOF</span><span class="sxs-lookup"><span data-stu-id="29dc9-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29dc9-176"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29dc9-176"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="29dc9-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="29dc9-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29dc9-178"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="29dc9-178"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="29dc9-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="29dc9-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29dc9-180">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="29dc9-180">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

