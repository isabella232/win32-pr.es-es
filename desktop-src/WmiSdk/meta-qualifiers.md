---
description: Los calificadores meta refinan la definición de las meta-construcciones en el modelo CIM aclarando el uso real de una declaración de clase o propiedad dentro de la sintaxis MOF.
ms.assetid: 3674a051-3756-4d09-a70e-46a57b442104
ms.tgt_platform: multiple
title: Meta (Calificadores)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8618ef8258f403a43e08be54b3acbd5bb1e923c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659916"
---
# <a name="meta-qualifiers"></a><span data-ttu-id="26098-103">Meta (Calificadores)</span><span class="sxs-lookup"><span data-stu-id="26098-103">Meta Qualifiers</span></span>

<span data-ttu-id="26098-104">Los calificadores meta refinan la definición de las meta-construcciones en el modelo CIM aclarando el uso real de una declaración de clase o propiedad dentro de la sintaxis MOF.</span><span class="sxs-lookup"><span data-stu-id="26098-104">Meta qualifiers refine the definition of meta-constructs in the CIM model by clarifying the actual usage of a class or property declaration within the MOF syntax.</span></span>

<dt>

<span data-ttu-id="26098-105"><span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Asociación**</span><span class="sxs-lookup"><span data-stu-id="26098-105"><span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Association**</span></span>
</dt> <dd>

<span data-ttu-id="26098-106">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="26098-106">Data type: **boolean**</span></span>

<span data-ttu-id="26098-107">Se aplica a: clases</span><span class="sxs-lookup"><span data-stu-id="26098-107">Applies to: classes</span></span>

<span data-ttu-id="26098-108">Indica si la clase es una clase de asociación que se utiliza para describir una relación entre otras dos clases.</span><span class="sxs-lookup"><span data-stu-id="26098-108">Indicates whether the class is an association class used to describe a relationship between two other classes.</span></span> <span data-ttu-id="26098-109">La ausencia de este calificador indica que la clase no es una clase de asociación.</span><span class="sxs-lookup"><span data-stu-id="26098-109">The absence of this qualifier indicates that the class is not an association class.</span></span> <span data-ttu-id="26098-110">Este calificador es mutuamente excluyente con **indicación**.</span><span class="sxs-lookup"><span data-stu-id="26098-110">This qualifier is mutually exclusive with **Indication**.</span></span> <span data-ttu-id="26098-111">Para obtener más información, vea [declarar una clase de asociación](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="26098-111">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="26098-112"><span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Señala**</span><span class="sxs-lookup"><span data-stu-id="26098-112"><span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Indication**</span></span>
</dt> <dd>

<span data-ttu-id="26098-113">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="26098-113">Data type: **boolean**</span></span>

<span data-ttu-id="26098-114">Se aplica a: clases</span><span class="sxs-lookup"><span data-stu-id="26098-114">Applies to: classes</span></span>

<span data-ttu-id="26098-115">Indica si la clase de objeto define una indicación.</span><span class="sxs-lookup"><span data-stu-id="26098-115">Indicates whether the object class defines an indication.</span></span> <span data-ttu-id="26098-116">Este calificador es mutuamente excluyente con la **Asociación**.</span><span class="sxs-lookup"><span data-stu-id="26098-116">This qualifier is mutually exclusive with **Association**.</span></span> <span data-ttu-id="26098-117">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="26098-117">The default is **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26098-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26098-118">Requirements</span></span>



| <span data-ttu-id="26098-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="26098-119">Requirement</span></span> | <span data-ttu-id="26098-120">Value</span><span class="sxs-lookup"><span data-stu-id="26098-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="26098-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26098-121">Minimum supported client</span></span><br/> | <span data-ttu-id="26098-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26098-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="26098-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26098-123">Minimum supported server</span></span><br/> | <span data-ttu-id="26098-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26098-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26098-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="26098-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26098-126">Calificadores WMI</span><span class="sxs-lookup"><span data-stu-id="26098-126">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="26098-127">Adición de un calificador</span><span class="sxs-lookup"><span data-stu-id="26098-127">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




