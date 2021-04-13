---
description: La \_ clase LogonSessionMappedDisk de Win32 representa una asociación entre una sesión de inicio de sesión y los discos lógicos asignados definidos dentro de la sesión.
ms.assetid: 013ae55e-6dd1-42fb-bcba-74d6afa1b905
ms.tgt_platform: multiple
title: Win32_LogonSessionMappedDisk (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogonSessionMappedDisk
- Win32_LogonSessionMappedDisk.Antecedent
- Win32_LogonSessionMappedDisk.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 203c9dd783dece52fa19905d51ece3bc26584dc6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539352"
---
# <a name="win32_logonsessionmappeddisk-class"></a><span data-ttu-id="b6427-103">\_Clase Win32 LogonSessionMappedDisk</span><span class="sxs-lookup"><span data-stu-id="b6427-103">Win32\_LogonSessionMappedDisk class</span></span>

<span data-ttu-id="b6427-104">La \_ clase LogonSessionMappedDisk de Win32 representa una asociación entre una sesión de inicio de sesión y los discos lógicos asignados definidos dentro de la sesión.</span><span class="sxs-lookup"><span data-stu-id="b6427-104">The Win32\_LogonSessionMappedDisk class represents an association between a logon session and the mapped logical disks defined within the session.</span></span>

<span data-ttu-id="b6427-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b6427-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6427-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6427-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_LogonSessionMappedDisk : CIM_Dependency
{
  Win32_LogonSession      REF Antecedent;
  Win32_MappedLogicalDisk REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b6427-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b6427-107">Members</span></span>

<span data-ttu-id="b6427-108">La **clase \_ LogonSessionMappedDisk de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b6427-108">The **Win32\_LogonSessionMappedDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="b6427-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b6427-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6427-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b6427-110">Properties</span></span>

<span data-ttu-id="b6427-111">La **clase \_ LogonSessionMappedDisk de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b6427-111">The **Win32\_LogonSessionMappedDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b6427-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="b6427-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6427-113">Tipo de datos: **Win32 \_ LogonSession**</span><span class="sxs-lookup"><span data-stu-id="b6427-113">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="b6427-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6427-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6427-115">Calificadores: [**invalidar**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b6427-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b6427-116">La propiedad antecedente hace referencia a una sesión de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="b6427-116">The Antecedent property references a logon session.</span></span>

</dd> <dt>

<span data-ttu-id="b6427-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="b6427-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6427-118">Tipo de datos: **Win32 \_ MappedLogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="b6427-118">Data type: **Win32\_MappedLogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="b6427-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6427-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6427-120">Calificadores: [**invalidar**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b6427-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b6427-121">La propiedad dependent hace referencia a un disco lógico asignado definido dentro de la sesión a la que hace referencia la propiedad antecedente.</span><span class="sxs-lookup"><span data-stu-id="b6427-121">The Dependent property references a mapped logical disk defined within the session referenced by the Antecedent property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6427-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6427-122">Requirements</span></span>



| <span data-ttu-id="b6427-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6427-123">Requirement</span></span> | <span data-ttu-id="b6427-124">Value</span><span class="sxs-lookup"><span data-stu-id="b6427-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6427-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6427-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b6427-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6427-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b6427-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6427-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b6427-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6427-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b6427-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b6427-129">Namespace</span></span><br/>                | <span data-ttu-id="b6427-130">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b6427-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b6427-131">MOF</span><span class="sxs-lookup"><span data-stu-id="b6427-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6427-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6427-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6427-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b6427-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6427-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6427-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6427-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6427-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6427-136">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b6427-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

