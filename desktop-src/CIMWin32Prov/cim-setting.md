---
description: La \_ clase de configuración CIM representa parámetros operativos y relacionados con la configuración de uno o más elementos del sistema administrados.
ms.assetid: 57c46b00-96c4-4df1-82ad-01f7b4f75ced
ms.tgt_platform: multiple
title: CIM_Setting (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Setting
- CIM_Setting.Caption
- CIM_Setting.Description
- CIM_Setting.SettingID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f1081bd93c95dfa90b6a4dfa6a87339e8e3172a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907176"
---
# <a name="cim_setting-class-cimwin32-wmi-providers"></a><span data-ttu-id="3dddd-103">CIM_Setting (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="3dddd-103">CIM_Setting class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="3dddd-104">La clase de **\_ configuración CIM** representa parámetros operativos y relacionados con la configuración de uno o más elementos del sistema administrados.</span><span class="sxs-lookup"><span data-stu-id="3dddd-104">The **CIM\_Setting** class represents configuration-related and operational parameters for one or more managed system elements.</span></span> <span data-ttu-id="3dddd-105">Un elemento del sistema administrado puede tener varios objetos de configuración asociados.</span><span class="sxs-lookup"><span data-stu-id="3dddd-105">A managed system element can have multiple setting objects associated with it.</span></span> <span data-ttu-id="3dddd-106">Los valores operativos actuales de los parámetros de un elemento se reflejan en las propiedades del propio elemento o de las propiedades de sus asociaciones.</span><span class="sxs-lookup"><span data-stu-id="3dddd-106">The current operational values for an element's parameters are reflected by properties in the element itself or by properties in its associations.</span></span> <span data-ttu-id="3dddd-107">No es necesario que estas propiedades tengan los mismos valores presentes en el objeto de configuración.</span><span class="sxs-lookup"><span data-stu-id="3dddd-107">These properties do not have to be the same values present in the setting object.</span></span> <span data-ttu-id="3dddd-108">Por ejemplo, un módem puede tener un valor de velocidad en baudios de 56 kilobytes por segundo, pero funcionar a 19,2 kilobytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="3dddd-108">For example, a modem may have a setting baud rate of 56 kilobytes per second, but be operating at 19.2 kilobytes per second.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3dddd-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="3dddd-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3dddd-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3dddd-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3dddd-111">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3dddd-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3dddd-112">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="3dddd-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dddd-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3dddd-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C572-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
};
```

## <a name="members"></a><span data-ttu-id="3dddd-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="3dddd-114">Members</span></span>

<span data-ttu-id="3dddd-115">La clase de **\_ configuración CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3dddd-115">The **CIM\_Setting** class has these types of members:</span></span>

-   [<span data-ttu-id="3dddd-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3dddd-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3dddd-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3dddd-117">Properties</span></span>

<span data-ttu-id="3dddd-118">La clase de **\_ configuración CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3dddd-118">The **CIM\_Setting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3dddd-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3dddd-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dddd-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3dddd-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dddd-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3dddd-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dddd-122">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3dddd-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3dddd-123">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="3dddd-123">Short textual description of the current object.</span></span>

</dd> <dt>

<span data-ttu-id="3dddd-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3dddd-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dddd-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3dddd-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dddd-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3dddd-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dddd-127">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="3dddd-127">Textual description of the current object.</span></span>

</dd> <dt>

<span data-ttu-id="3dddd-128">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="3dddd-128">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dddd-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3dddd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dddd-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3dddd-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dddd-131">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3dddd-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3dddd-132">Identificador por el que se conoce el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="3dddd-132">Identifier by which the current object is known.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3dddd-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3dddd-133">Remarks</span></span>

<span data-ttu-id="3dddd-134">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="3dddd-134">WMI does not implement this class.</span></span> <span data-ttu-id="3dddd-135">Para las clases WMI derivadas de la **\_ configuración de CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="3dddd-135">For WMI classes derived from **CIM\_Setting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="3dddd-136">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="3dddd-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3dddd-137">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="3dddd-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dddd-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dddd-138">Requirements</span></span>



| <span data-ttu-id="3dddd-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dddd-139">Requirement</span></span> | <span data-ttu-id="3dddd-140">Value</span><span class="sxs-lookup"><span data-stu-id="3dddd-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3dddd-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3dddd-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3dddd-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3dddd-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3dddd-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3dddd-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3dddd-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3dddd-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3dddd-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3dddd-145">Namespace</span></span><br/>                | <span data-ttu-id="3dddd-146">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3dddd-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3dddd-147">MOF</span><span class="sxs-lookup"><span data-stu-id="3dddd-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3dddd-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3dddd-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3dddd-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3dddd-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dddd-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dddd-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

