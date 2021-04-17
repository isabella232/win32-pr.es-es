---
description: Representa una entrada de control de acceso (ACE) que determina el acceso a la sesión interactiva de una máquina virtual.
ms.assetid: dfec83d6-8033-47b5-aa6f-fc7447a29f43
title: Msvm_InteractiveSessionACE (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InteractiveSessionACE
- Msvm_InteractiveSessionACE.Trustee
- Msvm_InteractiveSessionACE.AccessType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6c4b63e769b04092323cd2da7362ef6b156886b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686935"
---
# <a name="msvm_interactivesessionace-class"></a><span data-ttu-id="23dd6-103">MSVM \_ InteractiveSessionACE (clase)</span><span class="sxs-lookup"><span data-stu-id="23dd6-103">Msvm\_InteractiveSessionACE class</span></span>

<span data-ttu-id="23dd6-104">Representa una *entrada de control de acceso* (ACE) que determina el acceso a la sesión interactiva de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="23dd6-104">Represents an *access control entry* (ACE) that determines access to the interactive session of a virtual machine.</span></span>

<span data-ttu-id="23dd6-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="23dd6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="23dd6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23dd6-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InteractiveSessionACE
{
  string Trustee;
  uint16 AccessType;
};
```

## <a name="members"></a><span data-ttu-id="23dd6-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="23dd6-107">Members</span></span>

<span data-ttu-id="23dd6-108">La clase **MSVM \_ InteractiveSessionACE** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="23dd6-108">The **Msvm\_InteractiveSessionACE** class has these types of members:</span></span>

-   [<span data-ttu-id="23dd6-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="23dd6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="23dd6-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="23dd6-110">Properties</span></span>

<span data-ttu-id="23dd6-111">La clase **MSVM \_ InteractiveSessionACE** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="23dd6-111">The **Msvm\_InteractiveSessionACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23dd6-112">**AccessType**</span><span class="sxs-lookup"><span data-stu-id="23dd6-112">**AccessType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dd6-113">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23dd6-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23dd6-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23dd6-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23dd6-115">Indica si la ACE concede o deniega el acceso al administrador de confianza.</span><span class="sxs-lookup"><span data-stu-id="23dd6-115">Indicates whether the ACE grants or denies access to the trustee.</span></span>

<dt>

<span id="Access_Allowed"></span><span id="access_allowed"></span><span id="ACCESS_ALLOWED"></span>

<span data-ttu-id="23dd6-116">**Acceso permitido** (0)</span><span class="sxs-lookup"><span data-stu-id="23dd6-116">**Access Allowed** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Denied"></span><span id="access_denied"></span><span id="ACCESS_DENIED"></span>

<span data-ttu-id="23dd6-117">**Acceso denegado** (1)</span><span class="sxs-lookup"><span data-stu-id="23dd6-117">**Access Denied** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="23dd6-118">**Confianza**</span><span class="sxs-lookup"><span data-stu-id="23dd6-118">**Trustee**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23dd6-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="23dd6-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23dd6-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23dd6-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23dd6-121">Identifica la entidad de seguridad a la que la ACE concede o deniega el acceso.</span><span class="sxs-lookup"><span data-stu-id="23dd6-121">Identifies the security principal that the ACE grants or denies access to.</span></span> <span data-ttu-id="23dd6-122">Los formatos válidos para esta propiedad incluyen el formato de nombre de usuario compatible con SAM de Windows y el formato de cadena SID de Windows.</span><span class="sxs-lookup"><span data-stu-id="23dd6-122">Valid formats for this property include the Windows SAM-compatible user name format and the Windows SID string format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23dd6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23dd6-123">Requirements</span></span>



| <span data-ttu-id="23dd6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="23dd6-124">Requirement</span></span> | <span data-ttu-id="23dd6-125">Value</span><span class="sxs-lookup"><span data-stu-id="23dd6-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23dd6-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23dd6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="23dd6-127">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="23dd6-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="23dd6-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23dd6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="23dd6-129">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="23dd6-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23dd6-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="23dd6-130">Namespace</span></span><br/>                | <span data-ttu-id="23dd6-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="23dd6-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="23dd6-132">MOF</span><span class="sxs-lookup"><span data-stu-id="23dd6-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23dd6-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23dd6-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="23dd6-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="23dd6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23dd6-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="23dd6-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="23dd6-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="23dd6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23dd6-137">**GetInteractiveSessionACL**</span><span class="sxs-lookup"><span data-stu-id="23dd6-137">**GetInteractiveSessionACL**</span></span>](getinteractivesessionacl-msvm-terminalservice.md)
</dt> </dl>

 

 




