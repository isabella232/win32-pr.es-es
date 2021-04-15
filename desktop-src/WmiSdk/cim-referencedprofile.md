---
description: Se usa para asociar una instancia \_ de CIM RegisteredProfile con una instancia de \_ REGISTEREDPROFILE de CIM de otro perfil que hace referencia al perfil dependiente como perfil relacionado.
ms.assetid: 631003de-477b-4447-9633-1601a7f8eadb
ms.tgt_platform: multiple
title: CIM_ReferencedProfile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReferencedProfile
- CIM_ReferencedProfile.Antecedent
- CIM_ReferencedProfile.Dependent
api_type:
- Schema
api_location:
- Root\interop
ms.openlocfilehash: 8fdc0d8dccd325ae7e13de971e09cce6faf93455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648595"
---
# <a name="cim_referencedprofile-class"></a><span data-ttu-id="eb0dd-103">\_Clase ReferencedProfile de CIM</span><span class="sxs-lookup"><span data-stu-id="eb0dd-103">CIM\_ReferencedProfile class</span></span>

<span data-ttu-id="eb0dd-104">Se usa para asociar una instancia de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) con una instancia de **\_ RegisteredProfile de CIM** de otro perfil que hace referencia al perfil dependiente como perfil relacionado.</span><span class="sxs-lookup"><span data-stu-id="eb0dd-104">Used to associate an instance [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) with an instance of **CIM\_RegisteredProfile** of another profile that references the dependent profile as a related profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eb0dd-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="eb0dd-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="eb0dd-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="eb0dd-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="eb0dd-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="eb0dd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb0dd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb0dd-108">Syntax</span></span>

``` syntax
[Association, Version("2.8.0"), UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_ReferencedProfile : CIM_Dependency
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="eb0dd-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="eb0dd-109">Members</span></span>

<span data-ttu-id="eb0dd-110">La clase **CIM \_ ReferencedProfile** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="eb0dd-110">The **CIM\_ReferencedProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="eb0dd-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eb0dd-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb0dd-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eb0dd-112">Properties</span></span>

<span data-ttu-id="eb0dd-113">La clase **CIM \_ ReferencedProfile** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="eb0dd-113">The **CIM\_ReferencedProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb0dd-114">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="eb0dd-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb0dd-115">Tipo de datos: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="eb0dd-115">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="eb0dd-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb0dd-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb0dd-117">Especifica la instancia de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) a la que hace referencia el perfil **dependiente** .</span><span class="sxs-lookup"><span data-stu-id="eb0dd-117">Specifies the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) instance that is referenced by the **Dependent** profile.</span></span>

</dd> <dt>

<span data-ttu-id="eb0dd-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="eb0dd-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb0dd-119">Tipo de datos: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="eb0dd-119">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="eb0dd-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb0dd-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb0dd-121">Especifica una instancia de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) que hace referencia a otros perfiles.</span><span class="sxs-lookup"><span data-stu-id="eb0dd-121">Specifies a [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) instance that references other profiles.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb0dd-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb0dd-122">Remarks</span></span>

<span data-ttu-id="eb0dd-123">El uso de las propiedades **dependent** y **Antecedent** de la **Asociación \_ ReferencedProfile de CIM** se define de tal forma que el perfil al que se hace referencia es el antecedente y el perfil que hace referencia es el dependiente.</span><span class="sxs-lookup"><span data-stu-id="eb0dd-123">The use of the **Dependent** and **Antecedent** properties in the **CIM\_ReferencedProfile** association is defined such that the profile being referenced is the antecedent and the profile doing the referencing is the dependent.</span></span>

<span data-ttu-id="eb0dd-124">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="eb0dd-124">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="eb0dd-125">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="eb0dd-125">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb0dd-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb0dd-126">Requirements</span></span>



| <span data-ttu-id="eb0dd-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb0dd-127">Requirement</span></span> | <span data-ttu-id="eb0dd-128">Value</span><span class="sxs-lookup"><span data-stu-id="eb0dd-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb0dd-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb0dd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="eb0dd-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="eb0dd-130">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="eb0dd-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb0dd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="eb0dd-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eb0dd-132">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="eb0dd-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eb0dd-133">Namespace</span></span><br/>                | <span data-ttu-id="eb0dd-134">\\Interoperabilidad raíz</span><span class="sxs-lookup"><span data-stu-id="eb0dd-134">Root\\interop</span></span><br/>                                                               |
| <span data-ttu-id="eb0dd-135">MOF</span><span class="sxs-lookup"><span data-stu-id="eb0dd-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb0dd-136"><dt>Interop. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb0dd-136"><dt>Interop.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb0dd-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb0dd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb0dd-138">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="eb0dd-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

