---
title: Elemento BODY (sendEmailType)
description: Contiene el texto en el cuerpo del mensaje de correo electrónico.
ms.assetid: fac6ddd5-6f73-427b-b213-ab946512c87a
keywords:
- Elemento BODY Programador de tareas
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4659f2ff03f69b6bba40d9cd16e9b68515cc8889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686042"
---
# <a name="body-sendemailtype-element"></a><span data-ttu-id="4470f-104">Elemento BODY (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="4470f-104">Body (sendEmailType) Element</span></span>

<span data-ttu-id="4470f-105">Contiene el texto en el cuerpo del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4470f-105">Contains the text in the body of the email message.</span></span>

``` syntax
<xs:element name="Body"
    type="string"
 />
```

<span data-ttu-id="4470f-106">El elemento **Body** se define mediante el tipo complejo de [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4470f-106">The **Body** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4470f-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="4470f-107">Parent element</span></span>



| <span data-ttu-id="4470f-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="4470f-108">Element</span></span>                                                                              | <span data-ttu-id="4470f-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="4470f-109">Derived from</span></span>                                                           | <span data-ttu-id="4470f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4470f-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="4470f-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="4470f-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="4470f-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="4470f-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="4470f-113">Representa una acción que envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4470f-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4470f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4470f-114">Remarks</span></span>

<span data-ttu-id="4470f-115">Para el desarrollo de C++, vea [**Body (propiedad) de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).</span><span class="sxs-lookup"><span data-stu-id="4470f-115">For C++ development, see [**Body Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).</span></span>

<span data-ttu-id="4470f-116">Para el desarrollo de scripts, vea [**EmailAction. Body**](emailaction-body.md).</span><span class="sxs-lookup"><span data-stu-id="4470f-116">For script development, see [**EmailAction.Body**](emailaction-body.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4470f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4470f-117">Requirements</span></span>



| <span data-ttu-id="4470f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4470f-118">Requirement</span></span> | <span data-ttu-id="4470f-119">Value</span><span class="sxs-lookup"><span data-stu-id="4470f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4470f-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4470f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4470f-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4470f-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4470f-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4470f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4470f-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4470f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





