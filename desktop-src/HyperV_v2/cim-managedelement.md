---
description: La \_ clase ManagedElement de CIM es una clase abstracta que proporciona una superclase común (o parte superior del árbol de herencia) para las clases que no son de asociación en el esquema CIM.
ms.assetid: 6655a480-37bd-403c-9673-4eaa3d381201
title: CIM_ManagedElement (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedElement
- CIM_ManagedElement.InstanceID
- CIM_ManagedElement.Caption
- CIM_ManagedElement.Description
- CIM_ManagedElement.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5d98c6e594103932b180fcb63a2eebaf2c328c4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686510"
---
# <a name="cim_managedelement-class"></a><span data-ttu-id="95fc1-103">CIM \_ ManagedElement (clase)</span><span class="sxs-lookup"><span data-stu-id="95fc1-103">CIM\_ManagedElement class</span></span>

<span data-ttu-id="95fc1-104">La **clase \_ ManagedElement de CIM** es una clase abstracta que proporciona una superclase común (o parte superior del árbol de herencia) para las clases que no son de asociación en el esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="95fc1-104">The **CIM\_ManagedElement** class is an abstract class that provides a common superclass (or top of the inheritance tree) for the non-association classes in the CIM Schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="95fc1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95fc1-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="95fc1-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="95fc1-106">Members</span></span>

<span data-ttu-id="95fc1-107">La clase **CIM \_ ManagedElement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="95fc1-107">The **CIM\_ManagedElement** class has these types of members:</span></span>

-   [<span data-ttu-id="95fc1-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="95fc1-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="95fc1-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="95fc1-109">Properties</span></span>

<span data-ttu-id="95fc1-110">La clase **CIM \_ ManagedElement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="95fc1-110">The **CIM\_ManagedElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95fc1-111">**Caption**</span><span class="sxs-lookup"><span data-stu-id="95fc1-111">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fc1-112">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="95fc1-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fc1-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95fc1-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95fc1-114">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="95fc1-114">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="95fc1-115">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="95fc1-115">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="95fc1-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95fc1-116">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fc1-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="95fc1-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fc1-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95fc1-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fc1-119">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="95fc1-119">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="95fc1-120">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="95fc1-120">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fc1-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="95fc1-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fc1-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95fc1-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fc1-123">Un nombre descriptivo para el objeto.</span><span class="sxs-lookup"><span data-stu-id="95fc1-123">A user-friendly name for the object.</span></span> <span data-ttu-id="95fc1-124">Esta propiedad permite a cada instancia definir un nombre descriptivo además de las propiedades clave, los datos de identidad y la información de descripción.</span><span class="sxs-lookup"><span data-stu-id="95fc1-124">This property allows each instance to define a user-friendly name in addition to its key properties, identity data, and description information.</span></span>

</dd> <dt>

<span data-ttu-id="95fc1-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="95fc1-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fc1-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="95fc1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fc1-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95fc1-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fc1-128">Identifica de forma única y opaca una instancia de esta clase dentro del ámbito del espacio de nombres contenedor.</span><span class="sxs-lookup"><span data-stu-id="95fc1-128">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="95fc1-129">Con el fin de garantizar la unicidad dentro del espacio de nombres, el valor de la propiedad **InstanceID** debe construirse en el patrón siguiente: *OrgID*:*LocalID*</span><span class="sxs-lookup"><span data-stu-id="95fc1-129">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="95fc1-130">*OrgID* debe incluir un nombre con copyright, marca registrada o de otro tipo que sea propiedad de la entidad empresarial que define el **InstanceID**, o bien un identificador registrado asignado por una entidad global reconocida.</span><span class="sxs-lookup"><span data-stu-id="95fc1-130">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="95fc1-131">Este patrón es similar a la estructura de los nombres de clase de esquema.</span><span class="sxs-lookup"><span data-stu-id="95fc1-131">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="95fc1-132">Además, para garantizar la exclusividad, el primer signo de dos puntos en **InstanceID** debe estar entre el *OrgID* y el *LocalID*.</span><span class="sxs-lookup"><span data-stu-id="95fc1-132">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="95fc1-133">Por lo tanto, el *OrgID* no debe contener un signo de dos puntos (': ').</span><span class="sxs-lookup"><span data-stu-id="95fc1-133">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="95fc1-134">La entidad de negocio elige *LocalID* y no se debe volver a usar para identificar distintos elementos del mundo real subyacentes.</span><span class="sxs-lookup"><span data-stu-id="95fc1-134">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="95fc1-135">Si no se usa el patrón anterior, la entidad de definición debe asegurarse de que el valor **InstanceID** resultante no se vuelva a usar en las propiedades **InstanceID** producidas por este proveedor u otros proveedores para este espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="95fc1-135">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="95fc1-136">En el caso de las instancias definidas por el grupo de tareas de administración distribuida (DMTF), el patrón debe usarse con el valor de *OrgID* establecido en CIM.</span><span class="sxs-lookup"><span data-stu-id="95fc1-136">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95fc1-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95fc1-137">Requirements</span></span>



| <span data-ttu-id="95fc1-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="95fc1-138">Requirement</span></span> | <span data-ttu-id="95fc1-139">Value</span><span class="sxs-lookup"><span data-stu-id="95fc1-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95fc1-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95fc1-140">Minimum supported client</span></span><br/> | <span data-ttu-id="95fc1-141">Windows 8</span><span class="sxs-lookup"><span data-stu-id="95fc1-141">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="95fc1-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95fc1-142">Minimum supported server</span></span><br/> | <span data-ttu-id="95fc1-143">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="95fc1-143">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="95fc1-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="95fc1-144">Namespace</span></span><br/>                | <span data-ttu-id="95fc1-145">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="95fc1-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="95fc1-146">MOF</span><span class="sxs-lookup"><span data-stu-id="95fc1-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95fc1-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95fc1-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="95fc1-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="95fc1-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95fc1-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="95fc1-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

