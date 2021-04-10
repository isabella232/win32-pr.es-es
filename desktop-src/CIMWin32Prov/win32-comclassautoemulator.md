---
description: La \_ clase WMI ComClassAutoEmulator Association de Win32 relaciona una clase de modelo de objetos componentes (com) y otra clase com que emula automáticamente.
ms.assetid: e060ba26-98e7-47cb-bf21-1ca80d0e8a07
ms.tgt_platform: multiple
title: Win32_ComClassAutoEmulator (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassAutoEmulator
- Win32_ComClassAutoEmulator.NewVersion
- Win32_ComClassAutoEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9442036d43859caa5fa277109c7e85553e7d42f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153360"
---
# <a name="win32_comclassautoemulator-class"></a><span data-ttu-id="c8982-103">\_Clase Win32 ComClassAutoEmulator</span><span class="sxs-lookup"><span data-stu-id="c8982-103">Win32\_ComClassAutoEmulator class</span></span>

<span data-ttu-id="c8982-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ComClassAutoEmulator** Association de Win32 relaciona una clase de modelo de objetos componentes (COM) y otra clase com que emula automáticamente.</span><span class="sxs-lookup"><span data-stu-id="c8982-104">The **Win32\_ComClassAutoEmulator** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) class and another COM class that it automatically emulates.</span></span>

<span data-ttu-id="c8982-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c8982-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c8982-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="c8982-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8982-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8982-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5D-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassAutoEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a><span data-ttu-id="c8982-108">Members</span><span class="sxs-lookup"><span data-stu-id="c8982-108">Members</span></span>

<span data-ttu-id="c8982-109">La **clase \_ ComClassAutoEmulator de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c8982-109">The **Win32\_ComClassAutoEmulator** class has these types of members:</span></span>

-   [<span data-ttu-id="c8982-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c8982-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c8982-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c8982-111">Properties</span></span>

<span data-ttu-id="c8982-112">La **clase \_ ComClassAutoEmulator de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c8982-112">The **Win32\_ComClassAutoEmulator** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8982-113">**NewVersion**</span><span class="sxs-lookup"><span data-stu-id="c8982-113">**NewVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8982-114">Tipo de datos: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="c8982-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="c8982-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c8982-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8982-116">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="c8982-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="c8982-117">Referencia a la instancia de que representa el componente COM que puede emular automáticamente el componente COM asociado.</span><span class="sxs-lookup"><span data-stu-id="c8982-117">Reference to the instance representing the COM component that can automatically emulate the associated COM component.</span></span> <span data-ttu-id="c8982-118">Esta información se obtiene a través de la entrada del registro autotreatas.</span><span class="sxs-lookup"><span data-stu-id="c8982-118">This information is obtained through the AutoTreatAs registry entry.</span></span>

</dd> <dt>

<span data-ttu-id="c8982-119">**OldVersion**</span><span class="sxs-lookup"><span data-stu-id="c8982-119">**OldVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8982-120">Tipo de datos: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="c8982-120">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="c8982-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c8982-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8982-122">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="c8982-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="c8982-123">Referencia a la instancia de que representa el componente COM emulado automáticamente por otro componente.</span><span class="sxs-lookup"><span data-stu-id="c8982-123">Reference to the instance representing the COM component that is automatically emulated by another component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8982-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8982-124">Requirements</span></span>



| <span data-ttu-id="c8982-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8982-125">Requirement</span></span> | <span data-ttu-id="c8982-126">Value</span><span class="sxs-lookup"><span data-stu-id="c8982-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8982-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8982-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c8982-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8982-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c8982-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8982-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c8982-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8982-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c8982-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c8982-131">Namespace</span></span><br/>                | <span data-ttu-id="c8982-132">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c8982-132">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c8982-133">MOF</span><span class="sxs-lookup"><span data-stu-id="c8982-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8982-134"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8982-134"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8982-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8982-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8982-136"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8982-136"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8982-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c8982-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="c8982-138">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c8982-138">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

