---
description: La \_ clase CIM ElementSetting representa la asociación entre los elementos del sistema administrados y la clase de configuración definida para ellos.
ms.assetid: e9b7c43f-7539-48c3-8679-568fb4b036bb
ms.tgt_platform: multiple
title: CIM_ElementSetting (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSetting
- CIM_ElementSetting.Element
- CIM_ElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c1ea52648728397e811cfae35e7a83e272ab8d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659605"
---
# <a name="cim_elementsetting-class-cimwin32-wmi-providers"></a><span data-ttu-id="a188e-103">CIM_ElementSetting (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="a188e-103">CIM_ElementSetting class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="a188e-104">La clase **CIM \_ ElementSetting** representa la asociación entre los elementos del sistema administrados y la clase de configuración definida para ellos.</span><span class="sxs-lookup"><span data-stu-id="a188e-104">The **CIM\_ElementSetting** class represents the association between managed system elements and the setting class defined for them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a188e-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="a188e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a188e-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a188e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a188e-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a188e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a188e-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="a188e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a188e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a188e-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{8502C577-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ElementSetting
{
  CIM_ManagedSystemElement REF Element;
  CIM_Setting              REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="a188e-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="a188e-110">Members</span></span>

<span data-ttu-id="a188e-111">La clase **CIM \_ ElementSetting** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a188e-111">The **CIM\_ElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="a188e-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a188e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a188e-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a188e-113">Properties</span></span>

<span data-ttu-id="a188e-114">La clase **CIM \_ ElementSetting** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a188e-114">The **CIM\_ElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a188e-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="a188e-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a188e-116">Tipo de datos **: \_ ManagedSystemElement de CIM**</span><span class="sxs-lookup"><span data-stu-id="a188e-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="a188e-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a188e-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a188e-118">Referencia al rol del objeto [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) de la Asociación **\_ ElementSetting de CIM** .</span><span class="sxs-lookup"><span data-stu-id="a188e-118">Reference to the role of the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) object of the **CIM\_ElementSetting** association.</span></span> <span data-ttu-id="a188e-119">El elemento del sistema administrado asociado proporciona el elemento que implementa la configuración del elemento.</span><span class="sxs-lookup"><span data-stu-id="a188e-119">The associated managed system element provides the element that implements the element setting.</span></span>

</dd> <dt>

<span data-ttu-id="a188e-120">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="a188e-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a188e-121">Tipo de datos **: \_ configuración de CIM**</span><span class="sxs-lookup"><span data-stu-id="a188e-121">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="a188e-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a188e-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a188e-123">Referencia al rol del objeto de [**\_ configuración de CIM**](cim-setting.md) de la Asociación **\_ ElementSetting de CIM** .</span><span class="sxs-lookup"><span data-stu-id="a188e-123">Reference to the role of the [**CIM\_Setting**](cim-setting.md) object of the **CIM\_ElementSetting** association.</span></span> <span data-ttu-id="a188e-124">La configuración asociada proporciona la configuración que implementa la configuración del elemento.</span><span class="sxs-lookup"><span data-stu-id="a188e-124">The associated setting provides the setting that implements the element setting.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a188e-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a188e-125">Remarks</span></span>

<span data-ttu-id="a188e-126">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="a188e-126">WMI does not implement this class.</span></span> <span data-ttu-id="a188e-127">Para las clases derivadas de **CIM \_ ElementSetting**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a188e-127">For classes derived from **CIM\_ElementSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a188e-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="a188e-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a188e-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="a188e-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a188e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a188e-130">Requirements</span></span>



| <span data-ttu-id="a188e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a188e-131">Requirement</span></span> | <span data-ttu-id="a188e-132">Value</span><span class="sxs-lookup"><span data-stu-id="a188e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a188e-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a188e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a188e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a188e-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a188e-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a188e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a188e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a188e-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a188e-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a188e-137">Namespace</span></span><br/>                | <span data-ttu-id="a188e-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a188e-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a188e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="a188e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a188e-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a188e-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a188e-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a188e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a188e-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a188e-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




