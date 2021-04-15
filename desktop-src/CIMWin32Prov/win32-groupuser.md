---
description: La \_ clase WMI GroupUser Association de Win32 relaciona un grupo y una cuenta que es miembro de ese grupo.
ms.assetid: 46dd65f0-b729-4b23-8a00-bc33d1a4868b
ms.tgt_platform: multiple
title: Win32_GroupUser (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_GroupUser
- Win32_GroupUser.GroupComponent
- Win32_GroupUser.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 79035ff3c56331a240704cf6605fdf72efa4e81c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496528"
---
# <a name="win32_groupuser-class"></a><span data-ttu-id="e000d-103">\_Clase Win32 GroupUser</span><span class="sxs-lookup"><span data-stu-id="e000d-103">Win32\_GroupUser class</span></span>

<span data-ttu-id="e000d-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ GroupUser** Association de Win32 relaciona un grupo y una cuenta que es miembro de ese grupo.</span><span class="sxs-lookup"><span data-stu-id="e000d-104">The **Win32\_GroupUser** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a group and an account that is a member of that group.</span></span>

<span data-ttu-id="e000d-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e000d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e000d-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="e000d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e000d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e000d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C508-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_GroupUser : CIM_Component
{
  Win32_Group   REF GroupComponent;
  Win32_Account REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="e000d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e000d-108">Members</span></span>

<span data-ttu-id="e000d-109">La **clase \_ GroupUser de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e000d-109">The **Win32\_GroupUser** class has these types of members:</span></span>

-   [<span data-ttu-id="e000d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e000d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e000d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e000d-111">Properties</span></span>

<span data-ttu-id="e000d-112">La **clase \_ GroupUser de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e000d-112">The **Win32\_GroupUser** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e000d-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e000d-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e000d-114">Tipo de datos **: \_ Grupo Win32**</span><span class="sxs-lookup"><span data-stu-id="e000d-114">Data type: **Win32\_Group**</span></span>
</dt> <dt>

<span data-ttu-id="e000d-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e000d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e000d-116">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| Grupo Win32 de WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="e000d-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Group")</span></span>
</dt> </dl>

<span data-ttu-id="e000d-117">Referencia a la instancia de que representa el grupo del que la cuenta es miembro.</span><span class="sxs-lookup"><span data-stu-id="e000d-117">Reference to the instance representing the group of which the account is a member.</span></span>

</dd> <dt>

<span data-ttu-id="e000d-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e000d-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e000d-119">Tipo de datos **: \_ cuenta de Win32**</span><span class="sxs-lookup"><span data-stu-id="e000d-119">Data type: **Win32\_Account**</span></span>
</dt> <dt>

<span data-ttu-id="e000d-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e000d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e000d-121">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| cuenta de Win32 de WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="e000d-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Account")</span></span>
</dt> </dl>

<span data-ttu-id="e000d-122">Referencia a la instancia de que representa la cuenta de usuario o del sistema que forma parte de un grupo de cuentas.</span><span class="sxs-lookup"><span data-stu-id="e000d-122">Reference to the instance representing the user or system account that is a part of a group of accounts.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e000d-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e000d-123">Remarks</span></span>

<span data-ttu-id="e000d-124">La **clase \_ GroupUser de Win32** se deriva [**del \_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="e000d-124">The **Win32\_GroupUser** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e000d-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e000d-125">Examples</span></span>

<span data-ttu-id="e000d-126">Para obtener un ejemplo de PowerShell sobre \_ Cómo usar Win32 GroupUser para recuperar una lista de miembros del grupo local, consulte el ejemplo de la [lista de miembros del grupo local en un equipo remoto mediante WMI y PowerShell](https://Gallery.TechNet.Microsoft.Com/List-local-group-members-762b48c5) en la galería de TechNet.</span><span class="sxs-lookup"><span data-stu-id="e000d-126">For a PowerShell example of using Win32\_GroupUser to retrieve a list of local group members, see the [List local group members on a remote computer using WMI and PowerShell sample](https://Gallery.TechNet.Microsoft.Com/List-local-group-members-762b48c5) on TechNet Gallery.</span></span>

<span data-ttu-id="e000d-127">El ejemplo de código VBScript del administrador de [información de WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) de la galería de TechNet usa la clase **Win32 \_ GroupUser** para recuperar información de usuario de varios equipos remotos.</span><span class="sxs-lookup"><span data-stu-id="e000d-127">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_GroupUser** class to retrieve user information from a number of remote computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="e000d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e000d-128">Requirements</span></span>



| <span data-ttu-id="e000d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e000d-129">Requirement</span></span> | <span data-ttu-id="e000d-130">Value</span><span class="sxs-lookup"><span data-stu-id="e000d-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e000d-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e000d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e000d-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e000d-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e000d-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e000d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e000d-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e000d-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e000d-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e000d-135">Namespace</span></span><br/>                | <span data-ttu-id="e000d-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e000d-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e000d-137">MOF</span><span class="sxs-lookup"><span data-stu-id="e000d-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e000d-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e000d-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e000d-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e000d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e000d-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e000d-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e000d-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="e000d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e000d-142">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="e000d-142">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="e000d-143">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e000d-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

