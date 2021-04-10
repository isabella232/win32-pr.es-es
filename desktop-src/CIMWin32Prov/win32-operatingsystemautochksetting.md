---
description: Esta clase representa la asociación entre un sistema operativo y la configuración de AUTOCHK que se aplica a los discos de la máquina. Tenga en cuenta que la configuración está asociada a un sistema operativo en lugar de a un equipo dado que puede haber uno o más sistemas operativos instalados en el equipo, cada uno con su propia configuración de Autochk.
ms.assetid: 11178459-85c2-41c0-83b3-5b967e3311cf
ms.tgt_platform: multiple
title: Win32_OperatingSystemAutochkSetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 905ffc92273b46bb36b7b3e2909afea32e6baeff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153420"
---
# <a name="win32_operatingsystemautochksetting-class"></a><span data-ttu-id="72a13-103">\_Clase Win32 OperatingSystemAutochkSetting</span><span class="sxs-lookup"><span data-stu-id="72a13-103">Win32\_OperatingSystemAutochkSetting class</span></span>

<span data-ttu-id="72a13-104">Esta clase representa la asociación entre un sistema operativo y la configuración de AUTOCHK que se aplica a los discos de la máquina. Tenga en cuenta que la configuración está asociada a un sistema operativo en lugar de a un equipo dado que puede haber uno o más sistemas operativos instalados en el equipo, cada uno con su propia configuración de Autochk.</span><span class="sxs-lookup"><span data-stu-id="72a13-104">This class represents the association between an operating system and the autochk settings that apply to the disks on the machine.Note that the setting is associated to operating system rather than computer system since there can be one or more operating systems installed on the machine, each with its own autochk settings.</span></span>

<span data-ttu-id="72a13-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="72a13-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="72a13-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72a13-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_OperatingSystemAutochkSetting : CIM_ElementSetting
{
  Win32_OperatingSystem REF Element;
  Win32_AutochkSetting  REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="72a13-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="72a13-107">Members</span></span>

<span data-ttu-id="72a13-108">La **clase \_ OperatingSystemAutochkSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="72a13-108">The **Win32\_OperatingSystemAutochkSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="72a13-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="72a13-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72a13-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="72a13-110">Properties</span></span>

<span data-ttu-id="72a13-111">La **clase \_ OperatingSystemAutochkSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="72a13-111">The **Win32\_OperatingSystemAutochkSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72a13-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="72a13-112">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a13-113">Tipo de datos: **Win32 \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="72a13-113">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="72a13-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72a13-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72a13-115">Calificadores: [**invalidar**](../wmisdk/standard-qualifiers.md) ("elemento"), [**clave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="72a13-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="72a13-116">TBD</span><span class="sxs-lookup"><span data-stu-id="72a13-116">TBD</span></span>

</dd> <dt>

<span data-ttu-id="72a13-117">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="72a13-117">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72a13-118">Tipo de datos: **Win32 \_ AutochkSetting**</span><span class="sxs-lookup"><span data-stu-id="72a13-118">Data type: **Win32\_AutochkSetting**</span></span>
</dt> <dt>

<span data-ttu-id="72a13-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72a13-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72a13-120">Calificadores: [**invalidación**](../wmisdk/standard-qualifiers.md) ("configuración"), [**clave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="72a13-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="72a13-121">TBD</span><span class="sxs-lookup"><span data-stu-id="72a13-121">TBD</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72a13-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72a13-122">Requirements</span></span>



| <span data-ttu-id="72a13-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="72a13-123">Requirement</span></span> | <span data-ttu-id="72a13-124">Value</span><span class="sxs-lookup"><span data-stu-id="72a13-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72a13-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72a13-125">Minimum supported client</span></span><br/> | <span data-ttu-id="72a13-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72a13-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="72a13-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72a13-127">Minimum supported server</span></span><br/> | <span data-ttu-id="72a13-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72a13-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="72a13-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="72a13-129">Namespace</span></span><br/>                | <span data-ttu-id="72a13-130">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="72a13-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="72a13-131">MOF</span><span class="sxs-lookup"><span data-stu-id="72a13-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72a13-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72a13-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="72a13-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="72a13-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72a13-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72a13-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72a13-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="72a13-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72a13-136">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="72a13-136">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

 
