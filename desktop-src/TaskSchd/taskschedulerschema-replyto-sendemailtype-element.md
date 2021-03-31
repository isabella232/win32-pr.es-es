---
title: ReplyTo (sendEmailType) (elemento)
description: Contiene las direcciones de correo electrónico a las que se responde en el mensaje de correo electrónico.
ms.assetid: c09b72f6-de2c-41dc-942c-d6184863e33c
keywords:
- Elemento ReplyTo Programador de tareas
topic_type:
- apiref
api_name:
- ReplyTo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02055539d4557a60f182981f0d9cd7d3e1a63ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151178"
---
# <a name="replyto-sendemailtype-element"></a><span data-ttu-id="b8eff-104">ReplyTo (sendEmailType) (elemento)</span><span class="sxs-lookup"><span data-stu-id="b8eff-104">ReplyTo (sendEmailType) Element</span></span>

<span data-ttu-id="b8eff-105">Contiene las direcciones de correo electrónico a las que se responde en el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b8eff-105">Contains the email addresses that are replied to in the email message.</span></span>

``` syntax
<xs:element name="ReplyTo"
    type="string"
 />
```

<span data-ttu-id="b8eff-106">El elemento **ReplyTo** se define mediante el tipo complejo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b8eff-106">The **ReplyTo** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b8eff-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="b8eff-107">Parent element</span></span>



| <span data-ttu-id="b8eff-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b8eff-108">Element</span></span>                                                                              | <span data-ttu-id="b8eff-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="b8eff-109">Derived from</span></span>                                                           | <span data-ttu-id="b8eff-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8eff-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="b8eff-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="b8eff-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="b8eff-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="b8eff-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="b8eff-113">Representa una acción que envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b8eff-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b8eff-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8eff-114">Remarks</span></span>

<span data-ttu-id="b8eff-115">Para el desarrollo de C++, consulte la [**propiedad ReplyTo de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto).</span><span class="sxs-lookup"><span data-stu-id="b8eff-115">For C++ development, see [**ReplyTo Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto).</span></span>

<span data-ttu-id="b8eff-116">Para el desarrollo de scripts, vea [**EmailAction. ReplyTo**](emailaction-replyto.md).</span><span class="sxs-lookup"><span data-stu-id="b8eff-116">For script development, see [**EmailAction.ReplyTo**](emailaction-replyto.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8eff-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8eff-117">Requirements</span></span>



| <span data-ttu-id="b8eff-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8eff-118">Requirement</span></span> | <span data-ttu-id="b8eff-119">Value</span><span class="sxs-lookup"><span data-stu-id="b8eff-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b8eff-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8eff-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b8eff-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b8eff-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b8eff-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8eff-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b8eff-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8eff-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





