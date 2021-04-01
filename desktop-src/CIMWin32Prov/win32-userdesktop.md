---
description: La \_ clase WMI UserDesktop Association de Win32 relaciona una configuración de escritorio y de cuenta de usuario específica.
ms.assetid: 5ea83ad6-bd0a-4c16-85b2-e3e61ef05903
ms.tgt_platform: multiple
title: Win32_UserDesktop (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserDesktop
- Win32_UserDesktop.Element
- Win32_UserDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 39b45ee7859fea9f1068123041a87309cf40c2d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907077"
---
# <a name="win32_userdesktop-class"></a><span data-ttu-id="e190d-103">\_Clase Win32 UserDesktop</span><span class="sxs-lookup"><span data-stu-id="e190d-103">Win32\_UserDesktop class</span></span>

<span data-ttu-id="e190d-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ UserDesktop** Association de Win32 relaciona una configuración de escritorio y de cuenta de usuario específica.</span><span class="sxs-lookup"><span data-stu-id="e190d-104">The **Win32\_UserDesktop** association [WMI class](../wmisdk/retrieving-a-class.md) relates a user account and desktop settings that are specific to it.</span></span>

<span data-ttu-id="e190d-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e190d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e190d-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="e190d-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e190d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e190d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserDesktop : CIM_ElementSetting
{
  Win32_UserAccount REF Element;
  Win32_Desktop     REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="e190d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e190d-108">Members</span></span>

<span data-ttu-id="e190d-109">La **clase \_ UserDesktop de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e190d-109">The **Win32\_UserDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="e190d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e190d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e190d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e190d-111">Properties</span></span>

<span data-ttu-id="e190d-112">La **clase \_ UserDesktop de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e190d-112">The **Win32\_UserDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e190d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e190d-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e190d-114">Tipo de datos: **Win32 \_ cuentadeusuario**</span><span class="sxs-lookup"><span data-stu-id="e190d-114">Data type: **Win32\_UserAccount**</span></span>
</dt> <dt>

<span data-ttu-id="e190d-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e190d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e190d-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("elemento"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ cuentadeusuario")</span><span class="sxs-lookup"><span data-stu-id="e190d-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_UserAccount")</span></span>
</dt> </dl>

<span data-ttu-id="e190d-117">Referencia a la instancia de que representa la cuenta de usuario cuyo escritorio se puede personalizar mediante la propiedad de **configuración** de esta clase.</span><span class="sxs-lookup"><span data-stu-id="e190d-117">Reference to the instance representing the user account whose desktop can be customized by the **Settings** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="e190d-118">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="e190d-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e190d-119">Tipo de datos **: \_ escritorio Win32**</span><span class="sxs-lookup"><span data-stu-id="e190d-119">Data type: **Win32\_Desktop**</span></span>
</dt> <dt>

<span data-ttu-id="e190d-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e190d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e190d-121">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("configuración"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| escritorio Win32 de WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="e190d-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="e190d-122">Referencia a la instancia de que representa la configuración del escritorio que sirve para personalizar un escritorio de cuenta de usuario específico.</span><span class="sxs-lookup"><span data-stu-id="e190d-122">Reference to the instance representing the desktop settings that serve to customize a specific user account desktop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e190d-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e190d-123">Remarks</span></span>

<span data-ttu-id="e190d-124">La **clase \_ UserDesktop de Win32** se deriva de [**\_ ElementSetting de CIM**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="e190d-124">The **Win32\_UserDesktop** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e190d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e190d-125">Requirements</span></span>



| <span data-ttu-id="e190d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e190d-126">Requirement</span></span> | <span data-ttu-id="e190d-127">Value</span><span class="sxs-lookup"><span data-stu-id="e190d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e190d-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e190d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e190d-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e190d-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e190d-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e190d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e190d-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e190d-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e190d-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e190d-132">Namespace</span></span><br/>                | <span data-ttu-id="e190d-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e190d-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e190d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e190d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e190d-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e190d-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e190d-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e190d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e190d-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e190d-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e190d-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="e190d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e190d-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="e190d-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="e190d-140">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="e190d-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
