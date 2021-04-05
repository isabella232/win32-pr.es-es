---
description: La \_ Asociación ElementConfiguration de CIM relaciona un objeto de \_ configuración de CIM con uno o más elementos del sistema administrados. El objeto de configuración de CIM \_ representa un comportamiento determinado o un estado funcional deseado para el ManagedSystemElement de CIM asociado \_ .
ms.assetid: 4d2af009-7466-4394-af42-72c8d96e0786
ms.tgt_platform: multiple
title: CIM_ElementConfiguration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConfiguration
- CIM_ElementConfiguration.Configuration
- CIM_ElementConfiguration.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7707338a3c2268cba51146aa8462b3b244b149ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080216"
---
# <a name="cim_elementconfiguration-class"></a><span data-ttu-id="f2784-104">\_Clase ElementConfiguration de CIM</span><span class="sxs-lookup"><span data-stu-id="f2784-104">CIM\_ElementConfiguration class</span></span>

<span data-ttu-id="f2784-105">La **Asociación \_ ElementConfiguration de CIM** relaciona un objeto de [**\_ configuración de CIM**](cim-configuration.md) con uno o más elementos del sistema administrados.</span><span class="sxs-lookup"><span data-stu-id="f2784-105">The **CIM\_ElementConfiguration** association relates a [**CIM\_Configuration**](cim-configuration.md) object to one or more managed system elements.</span></span> <span data-ttu-id="f2784-106">El objeto de **\_ configuración de CIM** representa un comportamiento determinado o un estado funcional deseado para el [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md)asociado.</span><span class="sxs-lookup"><span data-stu-id="f2784-106">The **CIM\_Configuration** object represents a certain behavior, or a desired functional state for the associated [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f2784-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="f2784-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f2784-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f2784-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f2784-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f2784-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f2784-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="f2784-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2784-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2784-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FC049DCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ElementConfiguration
{
  CIM_Configuration        REF Configuration;
  CIM_ManagedSystemElement REF Element;
};
```

## <a name="members"></a><span data-ttu-id="f2784-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="f2784-112">Members</span></span>

<span data-ttu-id="f2784-113">La clase **CIM \_ ElementConfiguration** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f2784-113">The **CIM\_ElementConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="f2784-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f2784-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2784-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f2784-115">Properties</span></span>

<span data-ttu-id="f2784-116">La clase **CIM \_ ElementConfiguration** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f2784-116">The **CIM\_ElementConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f2784-117">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="f2784-117">**Configuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2784-118">Tipo de datos **: \_ configuración de CIM**</span><span class="sxs-lookup"><span data-stu-id="f2784-118">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="f2784-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f2784-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2784-120">Referencia al objeto [**de \_ configuración de CIM**](cim-configuration.md) que agrupa la configuración y las dependencias asociadas al elemento de sistema administrado.</span><span class="sxs-lookup"><span data-stu-id="f2784-120">Reference to the [**CIM\_Configuration**](cim-configuration.md) object that groups the settings and dependencies associated with the managed system element.</span></span>

</dd> <dt>

<span data-ttu-id="f2784-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="f2784-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2784-122">Tipo de datos **: \_ ManagedSystemElement de CIM**</span><span class="sxs-lookup"><span data-stu-id="f2784-122">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="f2784-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f2784-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2784-124">Referencia al elemento del sistema administrado.</span><span class="sxs-lookup"><span data-stu-id="f2784-124">Reference to the managed system element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2784-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2784-125">Remarks</span></span>

<span data-ttu-id="f2784-126">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="f2784-126">WMI does not implement this class.</span></span>

<span data-ttu-id="f2784-127">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="f2784-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f2784-128">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="f2784-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2784-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2784-129">Requirements</span></span>



| <span data-ttu-id="f2784-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2784-130">Requirement</span></span> | <span data-ttu-id="f2784-131">Value</span><span class="sxs-lookup"><span data-stu-id="f2784-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2784-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2784-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f2784-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2784-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f2784-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2784-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f2784-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2784-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f2784-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f2784-136">Namespace</span></span><br/>                | <span data-ttu-id="f2784-137">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f2784-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f2784-138">MOF</span><span class="sxs-lookup"><span data-stu-id="f2784-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2784-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2784-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2784-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f2784-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2784-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2784-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




