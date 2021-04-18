---
description: En la lista siguiente se enumeran los posibles valores del campo Flags en una entrada de Access Control WMI (ACE).
ms.assetid: bd09691d-e285-40e0-8686-edd5a132a06e
ms.tgt_platform: multiple
title: Constantes de marca ACE de espacio de nombres (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OBJECT_INHERIT_ACE
- CONTAINER_INHERIT_ACE
- NO_PROPAGATE_INHERIT_ACE
- INHERIT_ONLY_ACE
- INHERITED_ACE
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 053d4166882b6254dec313cb10fbf10588ba0071
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650086"
---
# <a name="namespace-ace-flag-constants"></a><span data-ttu-id="20fef-103">Constantes de marca ACE de espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="20fef-103">Namespace ACE Flag Constants</span></span>

<span data-ttu-id="20fef-104">En la lista siguiente se enumeran los posibles valores del campo **Flags** en una entrada de Access Control WMI (ACE).</span><span class="sxs-lookup"><span data-stu-id="20fef-104">The following list lists the possible values of the **Flags** field in a WMI Access Control Entry (ACE).</span></span>

<dl> <dt>

<span data-ttu-id="20fef-105"><span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**\_ACE de herencia de objeto \_**</span><span class="sxs-lookup"><span data-stu-id="20fef-105"><span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**OBJECT\_INHERIT\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20fef-106">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="20fef-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="20fef-107">Los objetos secundarios que no son de contenedor heredan la ACE como una ACE efectiva.</span><span class="sxs-lookup"><span data-stu-id="20fef-107">Non-container child objects inherit the ACE as an effective ACE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20fef-108"><span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**\_ACE de herencia de contenedor \_**</span><span class="sxs-lookup"><span data-stu-id="20fef-108"><span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**CONTAINER\_INHERIT\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20fef-109">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="20fef-109">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="20fef-110">La ACE tiene un efecto en los espacios de nombres secundarios, así como en el espacio de nombres actual.</span><span class="sxs-lookup"><span data-stu-id="20fef-110">The ACE has an effect on child namespaces as well as the current namespace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20fef-111"><span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**NO \_ propagar \_ ACE de herencia \_**</span><span class="sxs-lookup"><span data-stu-id="20fef-111"><span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**NO\_PROPAGATE\_INHERIT\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20fef-112">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="20fef-112">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="20fef-113">La ACE solo se aplica al espacio de nombres actual y a los elementos secundarios inmediatos.</span><span class="sxs-lookup"><span data-stu-id="20fef-113">The ACE applies only to the current namespace and immediate children .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20fef-114"><span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**solo HEREDAr \_ \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="20fef-114"><span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**INHERIT\_ONLY\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20fef-115">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="20fef-115">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="20fef-116">La ACE solo se aplica a los espacios de nombres secundarios.</span><span class="sxs-lookup"><span data-stu-id="20fef-116">The ACE applies only to child namespaces.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20fef-117"><span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**ACE HEREDAda \_**</span><span class="sxs-lookup"><span data-stu-id="20fef-117"><span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**INHERITED\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20fef-118">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="20fef-118">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="20fef-119">No lo establecen los clientes, pero se envía a los clientes cuando el origen de una ACE es un espacio de nombres primario.</span><span class="sxs-lookup"><span data-stu-id="20fef-119">This is not set by clients, but is reported to clients when the source of an ACE is a parent namespace.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20fef-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20fef-120">Requirements</span></span>



| <span data-ttu-id="20fef-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="20fef-121">Requirement</span></span> | <span data-ttu-id="20fef-122">Value</span><span class="sxs-lookup"><span data-stu-id="20fef-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="20fef-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20fef-123">Header</span></span><br/> | <dl> <span data-ttu-id="20fef-124"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="20fef-124"><dt>Winnt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20fef-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="20fef-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20fef-126">Constantes de seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="20fef-126">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="20fef-127">Configuración de descriptores de seguridad de espacio</span><span class="sxs-lookup"><span data-stu-id="20fef-127">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="20fef-128">Establecer la herencia de la seguridad del espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="20fef-128">Establishing Inheritance of Namespace Security</span></span>](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[<span data-ttu-id="20fef-129">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="20fef-129">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

 




