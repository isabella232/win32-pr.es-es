---
description: La \_ clase WMI LoggedOnUser Association de Win32 relaciona una sesión y una cuenta de usuario.
ms.assetid: b1233f90-4898-4ced-84d2-0858027e935a
ms.tgt_platform: multiple
title: Win32_LoggedOnUser (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoggedOnUser
- Win32_LoggedOnUser.Dependent
- Win32_LoggedOnUser.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f851c85563095a66197b0dde8e6cbddc9581f07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907461"
---
# <a name="win32_loggedonuser-class"></a><span data-ttu-id="01a01-103">\_Clase Win32 LoggedOnUser</span><span class="sxs-lookup"><span data-stu-id="01a01-103">Win32\_LoggedOnUser class</span></span>

<span data-ttu-id="01a01-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ LoggedOnUser** Association de Win32 relaciona una sesión y una cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="01a01-104">The **Win32\_LoggedOnUser** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a session and a user account.</span></span>

<span data-ttu-id="01a01-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="01a01-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="01a01-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="01a01-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="01a01-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01a01-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8BB5B3EC-E1F7-4b39-942A-605D5F55789A}"), AMENDMENT]
class Win32_LoggedOnUser : CIM_Dependency
{
  Win32_LogonSession REF Dependent;
  Win32_Account      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="01a01-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="01a01-108">Members</span></span>

<span data-ttu-id="01a01-109">La **clase \_ LoggedOnUser de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="01a01-109">The **Win32\_LoggedOnUser** class has these types of members:</span></span>

-   [<span data-ttu-id="01a01-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01a01-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01a01-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01a01-111">Properties</span></span>

<span data-ttu-id="01a01-112">La **clase \_ LoggedOnUser de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="01a01-112">The **Win32\_LoggedOnUser** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01a01-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="01a01-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a01-114">Tipo de datos **: \_ cuenta de Win32**</span><span class="sxs-lookup"><span data-stu-id="01a01-114">Data type: **Win32\_Account**</span></span>
</dt> <dt>

<span data-ttu-id="01a01-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01a01-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01a01-116">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) (antecedente), [**clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="01a01-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="01a01-117">[**\_ Cuenta de Win32**](win32-account.md) que describe la cuenta utilizada en el inicio de esta sesión.</span><span class="sxs-lookup"><span data-stu-id="01a01-117">A [**Win32\_Account**](win32-account.md) that describes the account used in the initiation of this session.</span></span> <span data-ttu-id="01a01-118">La cuenta puede ser una cuenta de usuario o una cuenta del sistema.</span><span class="sxs-lookup"><span data-stu-id="01a01-118">The account could be either a user account or a system account.</span></span>

</dd> <dt>

<span data-ttu-id="01a01-119">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="01a01-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01a01-120">Tipo de datos: **Win32 \_ LogonSession**</span><span class="sxs-lookup"><span data-stu-id="01a01-120">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="01a01-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01a01-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01a01-122">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) (dependiente), [**clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="01a01-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Dependent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="01a01-123">[**\_ LogonSession de Win32**](win32-logonsessionmappeddisk.md) que describe la sesión que la cuenta está usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="01a01-123">A [**Win32\_LogonSession**](win32-logonsessionmappeddisk.md) that describes the session that the account is currently using.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01a01-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01a01-124">Remarks</span></span>

<span data-ttu-id="01a01-125">La **clase \_ LoggedOnUser de Win32** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="01a01-125">The **Win32\_LoggedOnUser** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="examples"></a><span data-ttu-id="01a01-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="01a01-126">Examples</span></span>

<span data-ttu-id="01a01-127">El ejemplo de PowerShell de la [función get-loggedonuser](https://Gallery.TechNet.Microsoft.Com/scriptcenter/0e43993a-895a-4afe-a2b2-045a5146048a) obtiene los usuarios que han iniciado sesión en un equipo local o remoto, con información de la sesión.</span><span class="sxs-lookup"><span data-stu-id="01a01-127">The [get-loggedonuser function](https://Gallery.TechNet.Microsoft.Com/scriptcenter/0e43993a-895a-4afe-a2b2-045a5146048a) PowerShell sample gets the logged on users on a local or remote computer, with session information.</span></span>

## <a name="requirements"></a><span data-ttu-id="01a01-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01a01-128">Requirements</span></span>



| <span data-ttu-id="01a01-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="01a01-129">Requirement</span></span> | <span data-ttu-id="01a01-130">Value</span><span class="sxs-lookup"><span data-stu-id="01a01-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01a01-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01a01-131">Minimum supported client</span></span><br/> | <span data-ttu-id="01a01-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01a01-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01a01-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01a01-133">Minimum supported server</span></span><br/> | <span data-ttu-id="01a01-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01a01-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01a01-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="01a01-135">Namespace</span></span><br/>                | <span data-ttu-id="01a01-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="01a01-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="01a01-137">MOF</span><span class="sxs-lookup"><span data-stu-id="01a01-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01a01-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01a01-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="01a01-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="01a01-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01a01-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01a01-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01a01-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="01a01-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a01-142">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="01a01-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="01a01-143">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="01a01-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

