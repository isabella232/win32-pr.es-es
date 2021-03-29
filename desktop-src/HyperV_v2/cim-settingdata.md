---
description: Representa los parámetros operativos y de configuración de \_ las instancias de ManagedElement de CIM.
ms.assetid: a9ee0eb6-dc48-43f2-bdb5-f84fe7bbc1f2
title: CIM_SettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingData
- CIM_SettingData.InstanceID
- CIM_SettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 934aaaf694a79537f5761717f91db398141c33d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277386"
---
# <a name="cim_settingdata-class"></a><span data-ttu-id="f98ef-103">\_Clase SettingData de CIM</span><span class="sxs-lookup"><span data-stu-id="f98ef-103">CIM\_SettingData class</span></span>

<span data-ttu-id="f98ef-104">Representa los parámetros operativos y de configuración de las instancias de [**\_ ManagedElement de CIM**](cim-managedelement.md) .</span><span class="sxs-lookup"><span data-stu-id="f98ef-104">Represents configuration and operational parameters for [**CIM\_ManagedElement**](cim-managedelement.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="f98ef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f98ef-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingData : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="f98ef-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="f98ef-106">Members</span></span>

<span data-ttu-id="f98ef-107">La **clase \_ SettingData de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f98ef-107">The **CIM\_SettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="f98ef-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f98ef-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f98ef-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f98ef-109">Properties</span></span>

<span data-ttu-id="f98ef-110">La **clase \_ SettingData de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f98ef-110">The **CIM\_SettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f98ef-111">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f98ef-111">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f98ef-112">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f98ef-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f98ef-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f98ef-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f98ef-114">Calificadores: [**obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="f98ef-114">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="f98ef-115">Nombre descriptivo de una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="f98ef-115">The user-friendly name for an instance of this class.</span></span> <span data-ttu-id="f98ef-116">Además, el nombre descriptivo se puede usar como índice para una búsqueda o consulta.</span><span class="sxs-lookup"><span data-stu-id="f98ef-116">In addition, the user-friendly name can be used as an index for a search or query.</span></span> <span data-ttu-id="f98ef-117">El nombre no tiene que ser único dentro de un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="f98ef-117">The name does not have to be unique within a namespace.</span></span>

</dd> <dt>

<span data-ttu-id="f98ef-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f98ef-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f98ef-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f98ef-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f98ef-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f98ef-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f98ef-121">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span><span class="sxs-lookup"><span data-stu-id="f98ef-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="f98ef-122">Identifica de forma única una instancia de esta clase dentro del ámbito del espacio de nombres contenedor.</span><span class="sxs-lookup"><span data-stu-id="f98ef-122">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="f98ef-123">Con el fin de garantizar la unicidad dentro del espacio de nombres, el valor de la propiedad **InstanceID** debe construirse en el patrón siguiente: *OrgID*:*LocalID*</span><span class="sxs-lookup"><span data-stu-id="f98ef-123">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> -   <span data-ttu-id="f98ef-124">*OrgID* debe incluir un nombre con copyright, marca registrada o de otro tipo que sea propiedad de la entidad empresarial que define la propiedad **InstanceID** , o bien un identificador registrado asignado por una entidad global reconocida.</span><span class="sxs-lookup"><span data-stu-id="f98ef-124">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID** property, or be a registered ID that is assigned by a recognized global authority.</span></span>
> -   <span data-ttu-id="f98ef-125">*OrgID* no debe contener un signo de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="f98ef-125">*OrgID* must not contain a colon.</span></span> <span data-ttu-id="f98ef-126">Los primeros dos puntos de **InstanceID** deben estar entre el *OrgID* y *LocalID*.</span><span class="sxs-lookup"><span data-stu-id="f98ef-126">The first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span>
> -   <span data-ttu-id="f98ef-127">La entidad de negocio elige *LocalID* y no se debe volver a usar para identificar distintos elementos del mundo real subyacentes.</span><span class="sxs-lookup"><span data-stu-id="f98ef-127">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
> -   <span data-ttu-id="f98ef-128">Si no se usa el patrón anterior, la entidad de definición debe asegurarse de que el valor **InstanceID** resultante no se vuelva a usar en las propiedades **InstanceID** producidas por este proveedor u otros proveedores para este espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="f98ef-128">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
> -   <span data-ttu-id="f98ef-129">En el caso de las instancias definidas por DMTF, el patrón debe usarse con el valor de *OrgID* establecido en "CIM".</span><span class="sxs-lookup"><span data-stu-id="f98ef-129">For DMTF defined instances, the pattern must be used with the *OrgID* set to "CIM".</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f98ef-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f98ef-130">Requirements</span></span>



| <span data-ttu-id="f98ef-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f98ef-131">Requirement</span></span> | <span data-ttu-id="f98ef-132">Value</span><span class="sxs-lookup"><span data-stu-id="f98ef-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f98ef-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f98ef-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f98ef-134">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f98ef-134">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f98ef-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f98ef-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f98ef-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f98ef-136">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f98ef-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f98ef-137">Namespace</span></span><br/>                | <span data-ttu-id="f98ef-138">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f98ef-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f98ef-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f98ef-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f98ef-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f98ef-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f98ef-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f98ef-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f98ef-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f98ef-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f98ef-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="f98ef-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f98ef-144">**ManagedElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="f98ef-144">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

