---
description: La \_ clase WMI ClassicCOMApplicationClasses Association de Win32 relaciona una aplicación com y un componente com agrupados en él.
ms.assetid: 77f24461-9ca0-4fc3-8728-4a4b9a1edbc3
ms.tgt_platform: multiple
title: Win32_ClassicCOMApplicationClasses (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMApplicationClasses
- Win32_ClassicCOMApplicationClasses.PartComponent
- Win32_ClassicCOMApplicationClasses.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dfd451c1c5d4819f1ec1d21f890b207a06d6fb82
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907425"
---
# <a name="win32_classiccomapplicationclasses-class"></a><span data-ttu-id="6dfc1-103">\_Clase Win32 ClassicCOMApplicationClasses</span><span class="sxs-lookup"><span data-stu-id="6dfc1-103">Win32\_ClassicCOMApplicationClasses class</span></span>

<span data-ttu-id="6dfc1-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ClassicCOMApplicationClasses** Association de Win32 relaciona una aplicación com y un componente com agrupados en él.</span><span class="sxs-lookup"><span data-stu-id="6dfc1-104">The **Win32\_ClassicCOMApplicationClasses** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a COM application and a COM component grouped under it.</span></span>

<span data-ttu-id="6dfc1-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6dfc1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6dfc1-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="6dfc1-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dfc1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6dfc1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED54-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMApplicationClasses : Win32_COMApplicationClasses
{
  Win32_ClassicCOMClass REF PartComponent;
  Win32_DCOMApplication REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="6dfc1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6dfc1-108">Members</span></span>

<span data-ttu-id="6dfc1-109">La **clase \_ ClassicCOMApplicationClasses de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6dfc1-109">The **Win32\_ClassicCOMApplicationClasses** class has these types of members:</span></span>

-   [<span data-ttu-id="6dfc1-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6dfc1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6dfc1-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6dfc1-111">Properties</span></span>

<span data-ttu-id="6dfc1-112">La **clase \_ ClassicCOMApplicationClasses de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6dfc1-112">The **Win32\_ClassicCOMApplicationClasses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6dfc1-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="6dfc1-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dfc1-114">Tipo de datos: **Win32 \_ DCOMApplication**</span><span class="sxs-lookup"><span data-stu-id="6dfc1-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="6dfc1-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6dfc1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6dfc1-116">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")</span><span class="sxs-lookup"><span data-stu-id="6dfc1-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="6dfc1-117">[**\_ DCOMApplication de Win32**](win32-dcomapplication.md) que representa una aplicación DCOM que contiene o usa el componente com.</span><span class="sxs-lookup"><span data-stu-id="6dfc1-117">A [**Win32\_DCOMApplication**](win32-dcomapplication.md) that represents a DCOM application containing or using the COM component.</span></span>

</dd> <dt>

<span data-ttu-id="6dfc1-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="6dfc1-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6dfc1-119">Tipo de datos: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="6dfc1-119">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="6dfc1-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6dfc1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6dfc1-121">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="6dfc1-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="6dfc1-122">[**\_ ClassicCOMClass de Win32**](win32-classiccomclass.md) que representa el componente com existente o utilizado por la aplicación DCOM.</span><span class="sxs-lookup"><span data-stu-id="6dfc1-122">A [**Win32\_ClassicCOMClass**](win32-classiccomclass.md) that represents the COM component existing in or used by the DCOM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6dfc1-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6dfc1-123">Remarks</span></span>

<span data-ttu-id="6dfc1-124">La **clase \_ ClassicCOMApplicationClasses de Win32** se deriva de [**\_ COMApplicationClasses de Win32**](win32-comapplicationclasses.md).</span><span class="sxs-lookup"><span data-stu-id="6dfc1-124">The **Win32\_ClassicCOMApplicationClasses** class is derived from [**Win32\_COMApplicationClasses**](win32-comapplicationclasses.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6dfc1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6dfc1-125">Requirements</span></span>



| <span data-ttu-id="6dfc1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dfc1-126">Requirement</span></span> | <span data-ttu-id="6dfc1-127">Value</span><span class="sxs-lookup"><span data-stu-id="6dfc1-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6dfc1-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6dfc1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6dfc1-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6dfc1-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6dfc1-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6dfc1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6dfc1-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6dfc1-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6dfc1-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6dfc1-132">Namespace</span></span><br/>                | <span data-ttu-id="6dfc1-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6dfc1-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6dfc1-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6dfc1-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6dfc1-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6dfc1-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6dfc1-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6dfc1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dfc1-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dfc1-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dfc1-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="6dfc1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dfc1-139">**Win32 \_ COMApplicationClasses**</span><span class="sxs-lookup"><span data-stu-id="6dfc1-139">**Win32\_COMApplicationClasses**</span></span>](win32-comapplicationclasses.md)
</dt> <dt>

<span data-ttu-id="6dfc1-140">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6dfc1-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

