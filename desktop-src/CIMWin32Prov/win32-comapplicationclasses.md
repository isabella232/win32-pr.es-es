---
description: La \_ clase WMI COMApplicationClasses Abstract Association de Win32 relaciona un componente del modelo de objetos componentes (com) y la aplicación com donde reside.
ms.assetid: 7c188199-86fb-45ba-b318-9d9529b831b8
ms.tgt_platform: multiple
title: Win32_COMApplicationClasses (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationClasses
- Win32_COMApplicationClasses.PartComponent
- Win32_COMApplicationClasses.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 01413128f7457049a4383c1148938e2136645337
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153361"
---
# <a name="win32_comapplicationclasses-class"></a><span data-ttu-id="9e17f-103">\_Clase Win32 COMApplicationClasses</span><span class="sxs-lookup"><span data-stu-id="9e17f-103">Win32\_COMApplicationClasses class</span></span>

<span data-ttu-id="9e17f-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ COMApplicationClasses** Abstract Association de Win32 relaciona un componente del modelo de objetos componentes (COM) y la aplicación com donde reside.</span><span class="sxs-lookup"><span data-stu-id="9e17f-104">The **Win32\_COMApplicationClasses** abstract association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) component and the COM application where it resides.</span></span>

<span data-ttu-id="9e17f-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9e17f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9e17f-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9e17f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e17f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e17f-107">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED51-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationClasses : CIM_Component
{
  Win32_COMClass       REF PartComponent;
  Win32_COMApplication REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="9e17f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9e17f-108">Members</span></span>

<span data-ttu-id="9e17f-109">La **clase \_ COMApplicationClasses de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9e17f-109">The **Win32\_COMApplicationClasses** class has these types of members:</span></span>

-   [<span data-ttu-id="9e17f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9e17f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e17f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9e17f-111">Properties</span></span>

<span data-ttu-id="9e17f-112">La **clase \_ COMApplicationClasses de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9e17f-112">The **Win32\_COMApplicationClasses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e17f-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="9e17f-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e17f-114">Tipo de datos **: \_ Comaplicación Win32**</span><span class="sxs-lookup"><span data-stu-id="9e17f-114">Data type: **Win32\_COMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="9e17f-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e17f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e17f-116">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ comapplication")</span><span class="sxs-lookup"><span data-stu-id="9e17f-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_COMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="9e17f-117">Una [**\_ aplicación de Win32**](win32-comapplication.md) que representa la aplicación com que contiene el componente com.</span><span class="sxs-lookup"><span data-stu-id="9e17f-117">A [**Win32\_COMApplication**](win32-comapplication.md) that represents the COM application containing the COM component.</span></span>

</dd> <dt>

<span data-ttu-id="9e17f-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9e17f-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e17f-119">Tipo de datos **: \_ Comclase Win32**</span><span class="sxs-lookup"><span data-stu-id="9e17f-119">Data type: **Win32\_COMClass**</span></span>
</dt> <dt>

<span data-ttu-id="9e17f-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e17f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e17f-121">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ comClass")</span><span class="sxs-lookup"><span data-stu-id="9e17f-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_COMClass")</span></span>
</dt> </dl>

<span data-ttu-id="9e17f-122">[**Comclase \_ de Win32**](win32-comclass.md) que representa el componente com agrupado en la aplicación com.</span><span class="sxs-lookup"><span data-stu-id="9e17f-122">A [**Win32\_COMClass**](win32-comclass.md) that represents the COM component grouped under the COM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e17f-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e17f-123">Remarks</span></span>

<span data-ttu-id="9e17f-124">La **clase \_ COMApplicationClasses de Win32** se deriva [**del \_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="9e17f-124">The **Win32\_COMApplicationClasses** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e17f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e17f-125">Requirements</span></span>



| <span data-ttu-id="9e17f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e17f-126">Requirement</span></span> | <span data-ttu-id="9e17f-127">Value</span><span class="sxs-lookup"><span data-stu-id="9e17f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e17f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e17f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9e17f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e17f-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9e17f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e17f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9e17f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e17f-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9e17f-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9e17f-132">Namespace</span></span><br/>                | <span data-ttu-id="9e17f-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9e17f-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9e17f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9e17f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e17f-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e17f-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e17f-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9e17f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e17f-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e17f-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e17f-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e17f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e17f-139">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="9e17f-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="9e17f-140">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9e17f-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

