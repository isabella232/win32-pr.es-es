---
description: La \_ clase WMI SystemDriverPNPEntity Association de Win32 relaciona un dispositivo Plug and Play en el equipo que ejecuta Windows y el controlador que admite el dispositivo Plug and Play.
ms.assetid: 2696c8e5-3bc3-42e3-807b-a387607c7c09
ms.tgt_platform: multiple
title: Win32_SystemDriverPNPEntity (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriverPNPEntity
- Win32_SystemDriverPNPEntity.Antecedent
- Win32_SystemDriverPNPEntity.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b5a7eedfbd7a545e37cb9cda38c19cf61308761
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538914"
---
# <a name="win32_systemdriverpnpentity-class"></a><span data-ttu-id="9bf52-103">\_Clase Win32 SystemDriverPNPEntity</span><span class="sxs-lookup"><span data-stu-id="9bf52-103">Win32\_SystemDriverPNPEntity class</span></span>

<span data-ttu-id="9bf52-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemDriverPNPEntity** Association de Win32 relaciona un dispositivo Plug and Play en el equipo que ejecuta Windows y el controlador que admite el dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="9bf52-104">The **Win32\_SystemDriverPNPEntity** association [WMI class](../wmisdk/retrieving-a-class.md) relates a Plug and Play device on the computer system running Windows and the driver that supports the Plug and Play device.</span></span>

<span data-ttu-id="9bf52-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9bf52-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9bf52-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9bf52-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bf52-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9bf52-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0800F074-CB98-11d2-B35D-00104BC97924}"), AMENDMENT]
class Win32_SystemDriverPNPEntity : CIM_Dependency
{
  Win32_PNPEntity    REF Antecedent;
  Win32_SystemDriver REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="9bf52-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9bf52-108">Members</span></span>

<span data-ttu-id="9bf52-109">La **clase \_ SystemDriverPNPEntity de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9bf52-109">The **Win32\_SystemDriverPNPEntity** class has these types of members:</span></span>

-   [<span data-ttu-id="9bf52-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9bf52-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9bf52-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9bf52-111">Properties</span></span>

<span data-ttu-id="9bf52-112">La **clase \_ SystemDriverPNPEntity de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9bf52-112">The **Win32\_SystemDriverPNPEntity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9bf52-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="9bf52-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bf52-114">Tipo de datos: **Win32 \_ PNPEntity**</span><span class="sxs-lookup"><span data-stu-id="9bf52-114">Data type: **Win32\_PNPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="9bf52-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9bf52-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bf52-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("antecedente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PNPEntity")</span><span class="sxs-lookup"><span data-stu-id="9bf52-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PNPEntity")</span></span>
</dt> </dl>

<span data-ttu-id="9bf52-117">Representa el dispositivo Plug and Play controlado por el controlador.</span><span class="sxs-lookup"><span data-stu-id="9bf52-117">Represents the Plug and Play device controlled by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="9bf52-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="9bf52-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bf52-119">Tipo de datos: **Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="9bf52-119">Data type: **Win32\_SystemDriver**</span></span>
</dt> <dt>

<span data-ttu-id="9bf52-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9bf52-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bf52-121">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("dependiente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")</span><span class="sxs-lookup"><span data-stu-id="9bf52-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SystemDriver")</span></span>
</dt> </dl>

<span data-ttu-id="9bf52-122">[**\_ SystemDriver de Win32**](win32-systemdriver.md) que representa el controlador que admite el dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="9bf52-122">A [**Win32\_SystemDriver**](win32-systemdriver.md) that represents the driver that supports the Plug and Play device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9bf52-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9bf52-123">Remarks</span></span>

<span data-ttu-id="9bf52-124">La **clase \_ SystemDriverPNPEntity de Win32** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="9bf52-124">The **Win32\_SystemDriverPNPEntity** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9bf52-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bf52-125">Requirements</span></span>



| <span data-ttu-id="9bf52-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bf52-126">Requirement</span></span> | <span data-ttu-id="9bf52-127">Value</span><span class="sxs-lookup"><span data-stu-id="9bf52-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bf52-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9bf52-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9bf52-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9bf52-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9bf52-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9bf52-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9bf52-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9bf52-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9bf52-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9bf52-132">Namespace</span></span><br/>                | <span data-ttu-id="9bf52-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9bf52-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9bf52-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9bf52-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9bf52-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9bf52-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9bf52-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9bf52-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bf52-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bf52-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bf52-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="9bf52-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bf52-139">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="9bf52-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="9bf52-140">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="9bf52-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
