---
title: En (sendEmailType) (elemento)
description: Contiene las direcciones de correo electrónico a las que se enviará el correo electrónico.
ms.assetid: bf3aa878-967b-4ebd-9397-a2a499686a9f
keywords:
- Al elemento Programador de tareas
topic_type:
- apiref
api_name:
- To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9e0643220915ecb1c8f2cd1fe842e0dc3f21d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676621"
---
# <a name="to-sendemailtype-element"></a><span data-ttu-id="cc2b3-104">En (sendEmailType) (elemento)</span><span class="sxs-lookup"><span data-stu-id="cc2b3-104">To (sendEmailType) Element</span></span>

<span data-ttu-id="cc2b3-105">Contiene las direcciones de correo electrónico a las que se enviará el correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="cc2b3-105">Contains the email addresses to which the email will be sent.</span></span>

``` syntax
<xs:element name="To"
    type="string"
 />
```

<span data-ttu-id="cc2b3-106">El elemento **to** se define mediante el tipo complejo de [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cc2b3-106">The **To** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="cc2b3-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="cc2b3-107">Parent element</span></span>



| <span data-ttu-id="cc2b3-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="cc2b3-108">Element</span></span>                                                                              | <span data-ttu-id="cc2b3-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="cc2b3-109">Derived from</span></span>                                                           | <span data-ttu-id="cc2b3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc2b3-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="cc2b3-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="cc2b3-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="cc2b3-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="cc2b3-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="cc2b3-113">Representa una acción que envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="cc2b3-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cc2b3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc2b3-114">Remarks</span></span>

<span data-ttu-id="cc2b3-115">Para el desarrollo de C++, vea [**to (propiedad) de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).</span><span class="sxs-lookup"><span data-stu-id="cc2b3-115">For C++ development, see [**To Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).</span></span>

<span data-ttu-id="cc2b3-116">Para el desarrollo de scripts, vea [**EmailAction.to**](emailaction-to.md).</span><span class="sxs-lookup"><span data-stu-id="cc2b3-116">For script development, see [**EmailAction.To**](emailaction-to.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc2b3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc2b3-117">Requirements</span></span>



| <span data-ttu-id="cc2b3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc2b3-118">Requirement</span></span> | <span data-ttu-id="cc2b3-119">Value</span><span class="sxs-lookup"><span data-stu-id="cc2b3-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cc2b3-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc2b3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cc2b3-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cc2b3-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cc2b3-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc2b3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cc2b3-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cc2b3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





