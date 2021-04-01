---
title: Valores de sintaxis del constructor SNMP (SNMP. h)
description: Los valores de sintaxis del constructor SNMP describen tipos que son compatibles con el estándar de codificación de la notación de sintaxis abstracta uno (ASN. 1).
ms.assetid: 8e3b6e00-51cf-4e39-a68e-dcf8fbe8ab3b
topic_type:
- apiref
api_name:
- ASN_SEQUENCE
- ASN_SEQUENCEOF
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a484e58d7a92a3c75408db3160362d84e7891b76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150164"
---
# <a name="snmp-constructor-syntax-values"></a><span data-ttu-id="42fd3-103">Valores de sintaxis del constructor SNMP</span><span class="sxs-lookup"><span data-stu-id="42fd3-103">SNMP Constructor Syntax Values</span></span>

<span data-ttu-id="42fd3-104">\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="42fd3-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="42fd3-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="42fd3-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="42fd3-106">En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]</span><span class="sxs-lookup"><span data-stu-id="42fd3-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="42fd3-107">Los valores de sintaxis del constructor SNMP describen tipos que son compatibles con el estándar de codificación de la notación de sintaxis abstracta uno (ASN. 1).</span><span class="sxs-lookup"><span data-stu-id="42fd3-107">The SNMP Constructor Syntax Values describe types that are compliant with the Abstract Syntax Notation One (ASN.1) encoding standard.</span></span>



| <span data-ttu-id="42fd3-108">Constante</span><span class="sxs-lookup"><span data-stu-id="42fd3-108">Constant</span></span>                                                                                                                                                         | <span data-ttu-id="42fd3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="42fd3-109">Description</span></span>                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span id="ASN_SEQUENCE"></span><span id="asn_sequence"></span><dl> <span data-ttu-id="42fd3-110"><dt>**\_secuencia ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="42fd3-110"><dt>**ASN\_SEQUENCE**</dt></span></span> </dl>       | <span data-ttu-id="42fd3-111">Indica que el mensaje es una secuencia ASN.</span><span class="sxs-lookup"><span data-stu-id="42fd3-111">Indicates that the message is an ASN sequence.</span></span><br/> |
| <span id="ASN_SEQUENCEOF"></span><span id="asn_sequenceof"></span><dl> <span data-ttu-id="42fd3-112"><dt>**secuencia de ASN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="42fd3-112"><dt>**ASN\_SEQUENCEOF**</dt></span></span> </dl> | <span data-ttu-id="42fd3-113">Consulte secuencia de ASN \_ .</span><span class="sxs-lookup"><span data-stu-id="42fd3-113">See ASN\_SEQUENCE.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="42fd3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42fd3-114">Requirements</span></span>



| <span data-ttu-id="42fd3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="42fd3-115">Requirement</span></span> | <span data-ttu-id="42fd3-116">Value</span><span class="sxs-lookup"><span data-stu-id="42fd3-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="42fd3-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42fd3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="42fd3-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="42fd3-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="42fd3-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42fd3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="42fd3-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="42fd3-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="42fd3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42fd3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="42fd3-122"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="42fd3-122"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42fd3-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="42fd3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42fd3-124">Introducción al Protocolo simple de administración de redes (SNMP)</span><span class="sxs-lookup"><span data-stu-id="42fd3-124">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="42fd3-125">Referencia de SNMP</span><span class="sxs-lookup"><span data-stu-id="42fd3-125">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="42fd3-126">Constantes de SNMP</span><span class="sxs-lookup"><span data-stu-id="42fd3-126">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

