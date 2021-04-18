---
description: Clase abstracta para las subclases que describe las capacidades de un elemento administrado asociado y el potencial de las capacidades.
ms.assetid: f0ffddf5-99d4-49be-ac0a-c2cfd4a92d96
title: CIM_Capabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Capabilities
- CIM_Capabilities.InstanceID
- CIM_Capabilities.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e08fcef34c8c2e932851fb428fd32533eee4877e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687786"
---
# <a name="cim_capabilities-class"></a><span data-ttu-id="f0da2-103">CIM \_ Capabilities (clase)</span><span class="sxs-lookup"><span data-stu-id="f0da2-103">CIM\_Capabilities class</span></span>

<span data-ttu-id="f0da2-104">Clase abstracta para las subclases que describe las capacidades de un elemento administrado asociado y el potencial de las capacidades.</span><span class="sxs-lookup"><span data-stu-id="f0da2-104">An abstract class for subclasses that describes the abilities of an associated managed element, and the potential of the abilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0da2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0da2-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_Capabilities : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="f0da2-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="f0da2-106">Members</span></span>

<span data-ttu-id="f0da2-107">La clase de **\_ capacidades CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f0da2-107">The **CIM\_Capabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="f0da2-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0da2-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f0da2-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0da2-109">Properties</span></span>

<span data-ttu-id="f0da2-110">La clase de **\_ capacidades CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f0da2-110">The **CIM\_Capabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f0da2-111">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f0da2-111">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0da2-112">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0da2-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0da2-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0da2-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0da2-114">Calificadores: [**obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="f0da2-114">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="f0da2-115">Nombre descriptivo de esta instancia de clase.</span><span class="sxs-lookup"><span data-stu-id="f0da2-115">The user friendly name for this class instance.</span></span> <span data-ttu-id="f0da2-116">Además, el nombre descriptivo del usuario se puede usar como una propiedad de índice para una consulta.</span><span class="sxs-lookup"><span data-stu-id="f0da2-116">In addition, the user friendly name can be used as a index property for a query.</span></span> <span data-ttu-id="f0da2-117">Este valor no tiene que ser único dentro de su espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="f0da2-117">This value does not have to be unique within its namespace.</span></span>

</dd> <dt>

<span data-ttu-id="f0da2-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f0da2-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0da2-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0da2-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0da2-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0da2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0da2-121">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span><span class="sxs-lookup"><span data-stu-id="f0da2-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="f0da2-122">Identifica de forma única y opaca una instancia de esta clase dentro del ámbito del espacio de nombres contenedor.</span><span class="sxs-lookup"><span data-stu-id="f0da2-122">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="f0da2-123">Con el fin de garantizar la unicidad dentro del espacio de nombres, el valor de la propiedad **InstanceID** debe construirse en el patrón siguiente: *OrgID*:*LocalID*</span><span class="sxs-lookup"><span data-stu-id="f0da2-123">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="f0da2-124">*OrgID* debe incluir un nombre con copyright, marca registrada o de otro tipo que sea propiedad de la entidad empresarial que define el **InstanceID**, o bien un identificador registrado asignado por una entidad global reconocida.</span><span class="sxs-lookup"><span data-stu-id="f0da2-124">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="f0da2-125">Este patrón es similar a la estructura de los nombres de clase de esquema.</span><span class="sxs-lookup"><span data-stu-id="f0da2-125">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="f0da2-126">Además, para garantizar la exclusividad, el primer signo de dos puntos en **InstanceID** debe estar entre el *OrgID* y el *LocalID*.</span><span class="sxs-lookup"><span data-stu-id="f0da2-126">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="f0da2-127">Por lo tanto, el *OrgID* no debe contener un signo de dos puntos (': ').</span><span class="sxs-lookup"><span data-stu-id="f0da2-127">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="f0da2-128">La entidad de negocio elige *LocalID* y no se debe volver a usar para identificar distintos elementos del mundo real subyacentes.</span><span class="sxs-lookup"><span data-stu-id="f0da2-128">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="f0da2-129">Si no se usa el patrón anterior, la entidad de definición debe asegurarse de que el valor **InstanceID** resultante no se vuelva a usar en las propiedades **InstanceID** producidas por este proveedor u otros proveedores para este espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="f0da2-129">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="f0da2-130">En el caso de las instancias definidas por el grupo de tareas de administración distribuida (DMTF), el patrón debe usarse con el valor de *OrgID* establecido en CIM.</span><span class="sxs-lookup"><span data-stu-id="f0da2-130">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0da2-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0da2-131">Requirements</span></span>



| <span data-ttu-id="f0da2-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0da2-132">Requirement</span></span> | <span data-ttu-id="f0da2-133">Value</span><span class="sxs-lookup"><span data-stu-id="f0da2-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0da2-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0da2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f0da2-135">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f0da2-135">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f0da2-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0da2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f0da2-137">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f0da2-137">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f0da2-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f0da2-138">Namespace</span></span><br/>                | <span data-ttu-id="f0da2-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f0da2-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f0da2-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f0da2-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0da2-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0da2-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0da2-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f0da2-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0da2-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f0da2-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f0da2-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0da2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0da2-145">**ManagedElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="f0da2-145">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

