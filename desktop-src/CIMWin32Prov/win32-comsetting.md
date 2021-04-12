---
description: La \_ clase WMI abstracta Comsetting de Win32 representa la configuración asociada a un componente del modelo de objetos componentes (com) o a una aplicación com.
ms.assetid: e8cdbee8-41ab-4aff-b17b-707667138411
ms.tgt_platform: multiple
title: Win32_COMSetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMSetting
- Win32_COMSetting.Caption
- Win32_COMSetting.Description
- Win32_COMSetting.SettingID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5ec7932117d1ff0bc058d2b9a131f77ff9e040bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274882"
---
# <a name="win32_comsetting-class"></a><span data-ttu-id="3d1db-103">\_Clase de Comsetting Win32</span><span class="sxs-lookup"><span data-stu-id="3d1db-103">Win32\_COMSetting class</span></span>

<span data-ttu-id="3d1db-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) abstracta **\_ comsetting de Win32** representa la configuración asociada a un componente del modelo de objetos componentes (com) o a una aplicación com.</span><span class="sxs-lookup"><span data-stu-id="3d1db-104">The **Win32\_COMSetting** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings associated with a Component Object Model (COM) component or COM application.</span></span>

<span data-ttu-id="3d1db-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3d1db-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3d1db-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="3d1db-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d1db-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d1db-107">Syntax</span></span>

``` syntax
[abstract, UUID("{E5D8A560-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_COMSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
};
```

## <a name="members"></a><span data-ttu-id="3d1db-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3d1db-108">Members</span></span>

<span data-ttu-id="3d1db-109">La clase de **\_ comsetting Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3d1db-109">The **Win32\_COMSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="3d1db-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3d1db-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3d1db-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3d1db-111">Properties</span></span>

<span data-ttu-id="3d1db-112">La clase de **\_ establecimiento de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3d1db-112">The **Win32\_COMSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3d1db-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3d1db-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d1db-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3d1db-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d1db-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3d1db-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d1db-116">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3d1db-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3d1db-117">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="3d1db-117">Short textual description of the current object.</span></span>

<span data-ttu-id="3d1db-118">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="3d1db-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d1db-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3d1db-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d1db-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3d1db-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d1db-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3d1db-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d1db-122">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="3d1db-122">Textual description of the current object.</span></span>

<span data-ttu-id="3d1db-123">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="3d1db-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d1db-124">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="3d1db-124">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d1db-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3d1db-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d1db-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3d1db-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d1db-127">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3d1db-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3d1db-128">Identificador por el que se conoce el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="3d1db-128">Identifier by which the current object is known.</span></span>

<span data-ttu-id="3d1db-129">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="3d1db-129">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d1db-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d1db-130">Remarks</span></span>

<span data-ttu-id="3d1db-131">La clase de establecimiento de **Win32 \_** se deriva de la [**\_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="3d1db-131">The **Win32\_COMSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d1db-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d1db-132">Requirements</span></span>



| <span data-ttu-id="3d1db-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d1db-133">Requirement</span></span> | <span data-ttu-id="3d1db-134">Value</span><span class="sxs-lookup"><span data-stu-id="3d1db-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d1db-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d1db-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3d1db-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d1db-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d1db-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d1db-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3d1db-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d1db-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d1db-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3d1db-139">Namespace</span></span><br/>                | <span data-ttu-id="3d1db-140">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3d1db-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3d1db-141">MOF</span><span class="sxs-lookup"><span data-stu-id="3d1db-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d1db-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d1db-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d1db-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3d1db-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d1db-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d1db-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d1db-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d1db-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d1db-146">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="3d1db-146">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="3d1db-147">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3d1db-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

