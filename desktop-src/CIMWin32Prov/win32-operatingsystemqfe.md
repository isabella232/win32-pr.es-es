---
description: La \_ clase WMI OperatingSystemQFE Association de Win32 relaciona un sistema operativo y las actualizaciones del producto aplicadas tal y como se representan en Win32 \_ QuickFixEngineering.
ms.assetid: 71985759-7e45-44df-82a9-f9a93e3b923e
ms.tgt_platform: multiple
title: Win32_OperatingSystemQFE (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystemQFE
- Win32_OperatingSystemQFE.Antecedent
- Win32_OperatingSystemQFE.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3b357e3c6efb62217c137bc6c785185154ed984
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000756"
---
# <a name="win32_operatingsystemqfe-class"></a><span data-ttu-id="9494e-103">\_Clase Win32 OperatingSystemQFE</span><span class="sxs-lookup"><span data-stu-id="9494e-103">Win32\_OperatingSystemQFE class</span></span>

<span data-ttu-id="9494e-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ OperatingSystemQFE** Association de Win32 relaciona un sistema operativo y las actualizaciones del producto aplicadas tal y como se representan en [**Win32 \_ QuickFixEngineering**](win32-quickfixengineering.md).</span><span class="sxs-lookup"><span data-stu-id="9494e-104">The **Win32\_OperatingSystemQFE** association [WMI class](../wmisdk/retrieving-a-class.md) relates an operating system and the product updates applied as represented in [**Win32\_QuickFixEngineering**](win32-quickfixengineering.md).</span></span>

<span data-ttu-id="9494e-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9494e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9494e-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9494e-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9494e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9494e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{2CB2C452-C516-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_OperatingSystemQFE : CIM_Dependency
{
  Win32_OperatingSystem     REF Antecedent;
  Win32_QuickFixEngineering REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="9494e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9494e-108">Members</span></span>

<span data-ttu-id="9494e-109">La **clase \_ OperatingSystemQFE de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9494e-109">The **Win32\_OperatingSystemQFE** class has these types of members:</span></span>

-   [<span data-ttu-id="9494e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9494e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9494e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9494e-111">Properties</span></span>

<span data-ttu-id="9494e-112">La **clase \_ OperatingSystemQFE de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9494e-112">The **Win32\_OperatingSystemQFE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9494e-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="9494e-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9494e-114">Tipo de datos: **Win32 \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="9494e-114">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="9494e-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9494e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9494e-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("antecedente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ OperatingSystem")</span><span class="sxs-lookup"><span data-stu-id="9494e-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_OperatingSystem")</span></span>
</dt> </dl>

<span data-ttu-id="9494e-117">Referencia a la instancia de que representa el sistema afectado por la actualización del producto en esta asociación.</span><span class="sxs-lookup"><span data-stu-id="9494e-117">Reference to the instance representing the system affected by the product update in this association.</span></span>

</dd> <dt>

<span data-ttu-id="9494e-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="9494e-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9494e-119">Tipo de datos: **Win32 \_ QuickFixEngineering**</span><span class="sxs-lookup"><span data-stu-id="9494e-119">Data type: **Win32\_QuickFixEngineering**</span></span>
</dt> <dt>

<span data-ttu-id="9494e-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9494e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9494e-121">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**débil**](../wmisdk/standard-qualifiers.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("dependiente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ QuickFixEngineering")</span><span class="sxs-lookup"><span data-stu-id="9494e-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Weak**](../wmisdk/standard-qualifiers.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_QuickFixEngineering")</span></span>
</dt> </dl>

<span data-ttu-id="9494e-122">Referencia a la instancia de que representa la instancia del objeto que se aplica al sistema operativo en esta asociación.</span><span class="sxs-lookup"><span data-stu-id="9494e-122">Reference to the instance representing the object instance applied to the operating system in this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9494e-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9494e-123">Remarks</span></span>

<span data-ttu-id="9494e-124">La **clase \_ OperatingSystemQFE de Win32** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="9494e-124">The **Win32\_OperatingSystemQFE** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9494e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9494e-125">Requirements</span></span>



| <span data-ttu-id="9494e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9494e-126">Requirement</span></span> | <span data-ttu-id="9494e-127">Value</span><span class="sxs-lookup"><span data-stu-id="9494e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9494e-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9494e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9494e-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9494e-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9494e-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9494e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9494e-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9494e-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9494e-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9494e-132">Namespace</span></span><br/>                | <span data-ttu-id="9494e-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9494e-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9494e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9494e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9494e-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9494e-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9494e-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9494e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9494e-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9494e-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9494e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="9494e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9494e-139">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="9494e-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="9494e-140">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="9494e-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
