---
title: Valores de sintaxis simple SNMP (SNMP. h)
description: Los valores de sintaxis simple de SNMP se utilizan para indicar un tipo de variable SNMP.
ms.assetid: 42b681e5-721d-4d41-bc1a-c9f0005cde87
topic_type:
- apiref
api_name:
- ASN_INTEGER
- ASN_BITS
- ASN_OCTETSTRING
- ASN_NULL
- ASN_OBJECTIDENTIFIER
- ASN_INTEGER32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee6a40b4f63b7ce701b8232b310b2f73bac42d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150517"
---
# <a name="snmp-simple-syntax-values"></a><span data-ttu-id="2b36b-103">Valores de sintaxis simple de SNMP</span><span class="sxs-lookup"><span data-stu-id="2b36b-103">SNMP Simple Syntax Values</span></span>

<span data-ttu-id="2b36b-104">\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="2b36b-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2b36b-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="2b36b-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="2b36b-106">En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]</span><span class="sxs-lookup"><span data-stu-id="2b36b-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="2b36b-107">Los valores de sintaxis simple de SNMP se utilizan para indicar un tipo de variable SNMP.</span><span class="sxs-lookup"><span data-stu-id="2b36b-107">The SNMP Simple Syntax Values are used to indicate an SNMP variable type.</span></span>



| <span data-ttu-id="2b36b-108">Constante</span><span class="sxs-lookup"><span data-stu-id="2b36b-108">Constant</span></span>                                                                                                                                                                           | <span data-ttu-id="2b36b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b36b-109">Description</span></span>                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="ASN_INTEGER"></span><span id="asn_integer"></span><dl> <span data-ttu-id="2b36b-110"><dt>**\_entero ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="2b36b-110"><dt>**ASN\_INTEGER**</dt></span></span> </dl>                            | <span data-ttu-id="2b36b-111">Indica una variable de entero con signo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2b36b-111">Indicates a 32-bit signed integer variable.</span></span><br/>                |
| <span id="ASN_BITS"></span><span id="asn_bits"></span><dl> <span data-ttu-id="2b36b-112"><dt>**\_bits ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="2b36b-112"><dt>**ASN\_BITS**</dt></span></span> </dl>                                     | <span data-ttu-id="2b36b-113">Indica una variable que es una enumeración de bits con nombre.</span><span class="sxs-lookup"><span data-stu-id="2b36b-113">Indicates a variable that is an enumeration of named bits.</span></span><br/> |
| <span id="ASN_OCTETSTRING"></span><span id="asn_octetstring"></span><dl> <span data-ttu-id="2b36b-114"><dt>**\_OCTETSTRING ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="2b36b-114"><dt>**ASN\_OCTETSTRING**</dt></span></span> </dl>                | <span data-ttu-id="2b36b-115">Indica una variable de cadena de octeto.</span><span class="sxs-lookup"><span data-stu-id="2b36b-115">Indicates an octet string variable.</span></span><br/>                        |
| <span id="ASN_NULL"></span><span id="asn_null"></span><dl> <span data-ttu-id="2b36b-116"><dt>**\_nulo ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="2b36b-116"><dt>**ASN\_NULL**</dt></span></span> </dl>                                     | <span data-ttu-id="2b36b-117">Indica un valor **null** .</span><span class="sxs-lookup"><span data-stu-id="2b36b-117">Indicates a **NULL** value.</span></span><br/>                                |
| <span id="ASN_OBJECTIDENTIFIER"></span><span id="asn_objectidentifier"></span><dl> <span data-ttu-id="2b36b-118"><dt>**\_OBJECTIDENTIFIER ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="2b36b-118"><dt>**ASN\_OBJECTIDENTIFIER**</dt></span></span> </dl> | <span data-ttu-id="2b36b-119">Indica una variable de identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="2b36b-119">Indicates an object identifier variable.</span></span><br/>                   |
| <span id="ASN_INTEGER32"></span><span id="asn_integer32"></span><dl> <span data-ttu-id="2b36b-120"><dt>**\_INTEGER32 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="2b36b-120"><dt>**ASN\_INTEGER32**</dt></span></span> </dl>                      | <span data-ttu-id="2b36b-121">Indica un valor entero con signo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2b36b-121">Indicates a 32-bit signed integer value.</span></span><br/>                   |



## <a name="requirements"></a><span data-ttu-id="2b36b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b36b-122">Requirements</span></span>



| <span data-ttu-id="2b36b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b36b-123">Requirement</span></span> | <span data-ttu-id="2b36b-124">Value</span><span class="sxs-lookup"><span data-stu-id="2b36b-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2b36b-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b36b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2b36b-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2b36b-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="2b36b-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b36b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2b36b-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2b36b-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2b36b-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b36b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b36b-130"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b36b-130"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b36b-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b36b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b36b-132">Introducción al Protocolo simple de administración de redes (SNMP)</span><span class="sxs-lookup"><span data-stu-id="2b36b-132">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="2b36b-133">Referencia de SNMP</span><span class="sxs-lookup"><span data-stu-id="2b36b-133">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="2b36b-134">Constantes de SNMP</span><span class="sxs-lookup"><span data-stu-id="2b36b-134">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

