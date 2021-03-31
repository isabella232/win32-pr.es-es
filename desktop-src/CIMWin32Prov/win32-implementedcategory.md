---
description: La \_ clase WMI ImplementedCategory Association de Win32 relaciona una categoría de componente y la clase del modelo de objetos componentes (com) mediante sus interfaces.
ms.assetid: 7cf32b50-9ae6-44e5-b364-bc74dea3dc17
ms.tgt_platform: multiple
title: Win32_ImplementedCategory (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ImplementedCategory
- Win32_ImplementedCategory.Category
- Win32_ImplementedCategory.Component
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d885c8c8e92ea661e06b46f338924355438ff9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807910"
---
# <a name="win32_implementedcategory-class"></a><span data-ttu-id="27751-103">\_Clase Win32 ImplementedCategory</span><span class="sxs-lookup"><span data-stu-id="27751-103">Win32\_ImplementedCategory class</span></span>

<span data-ttu-id="27751-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ImplementedCategory** Association de Win32 relaciona una categoría de componente y la clase del modelo de objetos componentes (com) mediante sus interfaces.</span><span class="sxs-lookup"><span data-stu-id="27751-104">The **Win32\_ImplementedCategory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a component category and the Component Object Model (COM) class using its interfaces.</span></span>

<span data-ttu-id="27751-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="27751-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="27751-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="27751-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="27751-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27751-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5B-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ImplementedCategory
{
  Win32_ComponentCategory REF Category;
  Win32_ClassicCOMClass   REF Component;
};
```

## <a name="members"></a><span data-ttu-id="27751-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="27751-108">Members</span></span>

<span data-ttu-id="27751-109">La **clase \_ ImplementedCategory de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="27751-109">The **Win32\_ImplementedCategory** class has these types of members:</span></span>

-   [<span data-ttu-id="27751-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="27751-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="27751-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="27751-111">Properties</span></span>

<span data-ttu-id="27751-112">La **clase \_ ImplementedCategory de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="27751-112">The **Win32\_ImplementedCategory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="27751-113">**Categoría**</span><span class="sxs-lookup"><span data-stu-id="27751-113">**Category**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27751-114">Tipo de datos: **Win32 \_ ComponentCategory**</span><span class="sxs-lookup"><span data-stu-id="27751-114">Data type: **Win32\_ComponentCategory**</span></span>
</dt> <dt>

<span data-ttu-id="27751-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27751-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27751-116">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ComponentCategory")</span><span class="sxs-lookup"><span data-stu-id="27751-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ComponentCategory")</span></span>
</dt> </dl>

<span data-ttu-id="27751-117">Referencia a la instancia de que representa la categoría de componentes utilizada por la clase COM.</span><span class="sxs-lookup"><span data-stu-id="27751-117">Reference to the instance representing the component category being used by the COM class.</span></span>

</dd> <dt>

<span data-ttu-id="27751-118">**Componente**</span><span class="sxs-lookup"><span data-stu-id="27751-118">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27751-119">Tipo de datos: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="27751-119">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="27751-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27751-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27751-121">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="27751-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="27751-122">Referencia a la instancia de que representa la clase COM mediante la categoría asociada.</span><span class="sxs-lookup"><span data-stu-id="27751-122">Reference to the instance representing the COM class using the associated category.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27751-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27751-123">Requirements</span></span>



| <span data-ttu-id="27751-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="27751-124">Requirement</span></span> | <span data-ttu-id="27751-125">Value</span><span class="sxs-lookup"><span data-stu-id="27751-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27751-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27751-126">Minimum supported client</span></span><br/> | <span data-ttu-id="27751-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27751-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="27751-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27751-128">Minimum supported server</span></span><br/> | <span data-ttu-id="27751-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27751-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="27751-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="27751-130">Namespace</span></span><br/>                | <span data-ttu-id="27751-131">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="27751-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="27751-132">MOF</span><span class="sxs-lookup"><span data-stu-id="27751-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27751-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27751-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="27751-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="27751-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27751-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27751-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27751-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="27751-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="27751-137">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="27751-137">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

