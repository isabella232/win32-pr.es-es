---
title: Elemento Subject (sendEmailType)
description: Contiene el asunto del mensaje de correo electrónico.
ms.assetid: 2ccaa983-4dca-4e45-ba8d-2a93e23f7e8c
keywords:
- Elemento Subject Programador de tareas
topic_type:
- apiref
api_name:
- Subject
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3b4871f8d61603ea77c7699a9993d29e2fc0187
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535488"
---
# <a name="subject-sendemailtype-element"></a><span data-ttu-id="ea99a-104">Elemento Subject (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="ea99a-104">Subject (sendEmailType) Element</span></span>

<span data-ttu-id="ea99a-105">Contiene el asunto del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ea99a-105">Contains the subject of the email message.</span></span>

``` syntax
<xs:element name="Subject"
    type="string"
 />
```

<span data-ttu-id="ea99a-106">El elemento de **asunto** se define mediante el tipo complejo de [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ea99a-106">The **Subject** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ea99a-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="ea99a-107">Parent element</span></span>



| <span data-ttu-id="ea99a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ea99a-108">Element</span></span>                                                                              | <span data-ttu-id="ea99a-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="ea99a-109">Derived from</span></span>                                                           | <span data-ttu-id="ea99a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea99a-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="ea99a-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="ea99a-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="ea99a-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="ea99a-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="ea99a-113">Representa una acción que envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ea99a-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ea99a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea99a-114">Remarks</span></span>

<span data-ttu-id="ea99a-115">Para el desarrollo de C++, vea la [**propiedad Subject de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject).</span><span class="sxs-lookup"><span data-stu-id="ea99a-115">For C++ development, see [**Subject Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject).</span></span>

<span data-ttu-id="ea99a-116">Para el desarrollo de scripts, vea [**EmailAction. Subject**](emailaction-subject.md).</span><span class="sxs-lookup"><span data-stu-id="ea99a-116">For script development, see [**EmailAction.Subject**](emailaction-subject.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea99a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea99a-117">Requirements</span></span>



| <span data-ttu-id="ea99a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea99a-118">Requirement</span></span> | <span data-ttu-id="ea99a-119">Value</span><span class="sxs-lookup"><span data-stu-id="ea99a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ea99a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea99a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ea99a-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ea99a-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ea99a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea99a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ea99a-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ea99a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





