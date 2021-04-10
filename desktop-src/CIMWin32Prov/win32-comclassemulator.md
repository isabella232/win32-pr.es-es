---
description: La \_ clase WMI ComClassEmulator Association de Win32 relaciona dos versiones de una clase de modelo de objetos componentes (com).
ms.assetid: 33899c1e-911d-49ad-be25-355dcdb8f0c7
ms.tgt_platform: multiple
title: Win32_ComClassEmulator (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassEmulator
- Win32_ComClassEmulator.NewVersion
- Win32_ComClassEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9966ed85b0e0b4eeb25073e13ad679759f1d460b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152865"
---
# <a name="win32_comclassemulator-class"></a><span data-ttu-id="5f0b8-103">\_Clase Win32 ComClassEmulator</span><span class="sxs-lookup"><span data-stu-id="5f0b8-103">Win32\_ComClassEmulator class</span></span>

<span data-ttu-id="5f0b8-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ComClassEmulator** Association de Win32 relaciona dos versiones de una clase de modelo de objetos componentes (com).</span><span class="sxs-lookup"><span data-stu-id="5f0b8-104">The **Win32\_ComClassEmulator** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates two versions of a Component Object Model (COM) class.</span></span>

<span data-ttu-id="5f0b8-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5f0b8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5f0b8-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="5f0b8-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f0b8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f0b8-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5C-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a><span data-ttu-id="5f0b8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5f0b8-108">Members</span></span>

<span data-ttu-id="5f0b8-109">La **clase \_ ComClassEmulator de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5f0b8-109">The **Win32\_ComClassEmulator** class has these types of members:</span></span>

-   [<span data-ttu-id="5f0b8-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5f0b8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f0b8-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5f0b8-111">Properties</span></span>

<span data-ttu-id="5f0b8-112">La **clase \_ ComClassEmulator de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5f0b8-112">The **Win32\_ComClassEmulator** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f0b8-113">**NewVersion**</span><span class="sxs-lookup"><span data-stu-id="5f0b8-113">**NewVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f0b8-114">Tipo de datos: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="5f0b8-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="5f0b8-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5f0b8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f0b8-116">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="5f0b8-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="5f0b8-117">Referencia a la instancia de que representa el componente COM que contiene interfaces emulando la versión anterior del componente.</span><span class="sxs-lookup"><span data-stu-id="5f0b8-117">Reference to the instance representing the COM component that contains interfaces emulating the older version of the component.</span></span>

</dd> <dt>

<span data-ttu-id="5f0b8-118">**OldVersion**</span><span class="sxs-lookup"><span data-stu-id="5f0b8-118">**OldVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f0b8-119">Tipo de datos: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="5f0b8-119">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="5f0b8-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5f0b8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f0b8-121">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="5f0b8-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="5f0b8-122">Referencia a la instancia de que representa el componente COM con interfaces que se pueden emular mediante la nueva versión del componente.</span><span class="sxs-lookup"><span data-stu-id="5f0b8-122">Reference to the instance representing the COM component with interfaces that can be emulated by the new version of the component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f0b8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f0b8-123">Requirements</span></span>



| <span data-ttu-id="5f0b8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f0b8-124">Requirement</span></span> | <span data-ttu-id="5f0b8-125">Value</span><span class="sxs-lookup"><span data-stu-id="5f0b8-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f0b8-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f0b8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5f0b8-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f0b8-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5f0b8-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f0b8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5f0b8-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f0b8-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5f0b8-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5f0b8-130">Namespace</span></span><br/>                | <span data-ttu-id="5f0b8-131">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5f0b8-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5f0b8-132">MOF</span><span class="sxs-lookup"><span data-stu-id="5f0b8-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f0b8-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f0b8-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f0b8-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5f0b8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f0b8-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f0b8-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f0b8-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f0b8-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f0b8-137">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5f0b8-137">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

