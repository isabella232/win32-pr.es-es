---
description: Describe un perfil al que hace referencia otro perfil registrado.
ms.assetid: 36FC0161-C57F-488A-9B4A-C86C6EB481D7
title: Msvm_ReferencedProfile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencedProfile
- Msvm_ReferencedProfile.Antecedent
- Msvm_ReferencedProfile.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbe95658556be8a15bed0e7e5b5b32dda23ff21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687638"
---
# <a name="msvm_referencedprofile-class"></a><span data-ttu-id="391d4-103">MSVM \_ ReferencedProfile (clase)</span><span class="sxs-lookup"><span data-stu-id="391d4-103">Msvm\_ReferencedProfile class</span></span>

<span data-ttu-id="391d4-104">Describe un perfil al que hace referencia otro perfil registrado.</span><span class="sxs-lookup"><span data-stu-id="391d4-104">Describes a profile that is referenced by another registered profile.</span></span>

<span data-ttu-id="391d4-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="391d4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="391d4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="391d4-106">Syntax</span></span>

``` syntax
class Msvm_ReferencedProfile : CIM_ReferencedProfile
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="391d4-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="391d4-107">Members</span></span>

<span data-ttu-id="391d4-108">La clase **MSVM \_ ReferencedProfile** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="391d4-108">The **Msvm\_ReferencedProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="391d4-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="391d4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="391d4-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="391d4-110">Properties</span></span>

<span data-ttu-id="391d4-111">La clase **MSVM \_ ReferencedProfile** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="391d4-111">The **Msvm\_ReferencedProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="391d4-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="391d4-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="391d4-113">Tipo de datos: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="391d4-113">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="391d4-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="391d4-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="391d4-115">Perfil registrado al que hace referencia el perfil **dependiente** .</span><span class="sxs-lookup"><span data-stu-id="391d4-115">The registered profile that is referenced by the **Dependent** profile.</span></span>

</dd> <dt>

<span data-ttu-id="391d4-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="391d4-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="391d4-117">Tipo de datos: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="391d4-117">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="391d4-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="391d4-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="391d4-119">Perfil registrado que hace referencia a otros perfiles.</span><span class="sxs-lookup"><span data-stu-id="391d4-119">A registered profile that references other profiles.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="391d4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="391d4-120">Requirements</span></span>



| <span data-ttu-id="391d4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="391d4-121">Requirement</span></span> | <span data-ttu-id="391d4-122">Value</span><span class="sxs-lookup"><span data-stu-id="391d4-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="391d4-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="391d4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="391d4-124">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="391d4-124">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="391d4-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="391d4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="391d4-126">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="391d4-126">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="391d4-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="391d4-127">Namespace</span></span><br/>                | <span data-ttu-id="391d4-128">\\Interoperabilidad raíz</span><span class="sxs-lookup"><span data-stu-id="391d4-128">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="391d4-129">MOF</span><span class="sxs-lookup"><span data-stu-id="391d4-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="391d4-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="391d4-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="391d4-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="391d4-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="391d4-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="391d4-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

