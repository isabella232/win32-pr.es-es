---
description: Asocia dos elementos administrados que representan distintos aspectos de la misma entidad subyacente.
ms.assetid: 107A2B15-09F2-490A-8AB2-F9FE5F6FEE60
title: Msvm_LogicalIdentity (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalIdentity
- Msvm_LogicalIdentity.SameElement
- Msvm_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2f8d2ee522fde3769c08bcbb78611b99eed8e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545422"
---
# <a name="msvm_logicalidentity-class"></a><span data-ttu-id="6acfb-103">MSVM \_ LogicalIdentity (clase)</span><span class="sxs-lookup"><span data-stu-id="6acfb-103">Msvm\_LogicalIdentity class</span></span>

<span data-ttu-id="6acfb-104">Asocia dos elementos administrados que representan distintos aspectos de la misma entidad subyacente.</span><span class="sxs-lookup"><span data-stu-id="6acfb-104">Associates two managed elements that represent different aspects of the same underlying entity.</span></span> <span data-ttu-id="6acfb-105">Esta clase deriva de [**\_ LogicalIdentity CIM**](/windows/desktop/CIMWin32Prov/cim-logicalidentity).</span><span class="sxs-lookup"><span data-stu-id="6acfb-105">This class derives from [**CIM\_LogicalIdentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity).</span></span>

<span data-ttu-id="6acfb-106">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6acfb-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6acfb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6acfb-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalIdentity : CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="6acfb-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6acfb-108">Members</span></span>

<span data-ttu-id="6acfb-109">La clase **MSVM \_ LogicalIdentity** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6acfb-109">The **Msvm\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="6acfb-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6acfb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6acfb-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6acfb-111">Properties</span></span>

<span data-ttu-id="6acfb-112">La clase **MSVM \_ LogicalIdentity** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6acfb-112">The **Msvm\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6acfb-113">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="6acfb-113">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6acfb-114">Tipo de datos: **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="6acfb-114">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="6acfb-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6acfb-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6acfb-116">Referencia a un aspecto alternativo de la entidad del sistema.</span><span class="sxs-lookup"><span data-stu-id="6acfb-116">Reference to an alternate aspect of the system entity.</span></span>

</dd> <dt>

<span data-ttu-id="6acfb-117">**SystemElement**</span><span class="sxs-lookup"><span data-stu-id="6acfb-117">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6acfb-118">Tipo de datos: **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="6acfb-118">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="6acfb-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6acfb-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6acfb-120">Referencia a un aspecto del elemento lógico.</span><span class="sxs-lookup"><span data-stu-id="6acfb-120">Reference to one aspect of the logical element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6acfb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6acfb-121">Requirements</span></span>



| <span data-ttu-id="6acfb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6acfb-122">Requirement</span></span> | <span data-ttu-id="6acfb-123">Value</span><span class="sxs-lookup"><span data-stu-id="6acfb-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6acfb-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6acfb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6acfb-125">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="6acfb-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="6acfb-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6acfb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6acfb-127">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6acfb-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6acfb-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6acfb-128">Namespace</span></span><br/>                | <span data-ttu-id="6acfb-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="6acfb-129">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6acfb-130">MOF</span><span class="sxs-lookup"><span data-stu-id="6acfb-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6acfb-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6acfb-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6acfb-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6acfb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6acfb-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6acfb-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6acfb-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="6acfb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6acfb-135">**\_LOGICALIDENTITY CIM**</span><span class="sxs-lookup"><span data-stu-id="6acfb-135">**CIM\_LogicalIdentity**</span></span>](cim-logicalidentity.md)
</dt> <dt>

[<span data-ttu-id="6acfb-136">**\_LOGICALIDENTITY CIM**</span><span class="sxs-lookup"><span data-stu-id="6acfb-136">**CIM\_LogicalIdentity**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalidentity)
</dt> </dl>

 

