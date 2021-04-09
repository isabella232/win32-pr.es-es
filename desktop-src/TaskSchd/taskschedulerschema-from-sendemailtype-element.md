---
title: Elemento from (sendEmailType)
description: Contiene la dirección de correo electrónico del remitente de correo electrónico.
ms.assetid: b80733de-e050-4026-a2fe-f63833ec2660
keywords:
- Del elemento Programador de tareas
topic_type:
- apiref
api_name:
- From
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f50704212fe6a4fec7ce0fc21bacd7ea33e402c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079158"
---
# <a name="from-sendemailtype-element"></a><span data-ttu-id="6f2cb-104">Elemento from (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="6f2cb-104">From (sendEmailType) Element</span></span>

<span data-ttu-id="6f2cb-105">Contiene la dirección de correo electrónico del remitente de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="6f2cb-105">Contains the email address of the email sender.</span></span>

``` syntax
<xs:element name="From"
    type="string"
 />
```

<span data-ttu-id="6f2cb-106">El elemento **from** se define mediante el tipo complejo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6f2cb-106">The **From** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6f2cb-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="6f2cb-107">Parent element</span></span>



| <span data-ttu-id="6f2cb-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="6f2cb-108">Element</span></span>                                                                              | <span data-ttu-id="6f2cb-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="6f2cb-109">Derived from</span></span>                                                           | <span data-ttu-id="6f2cb-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f2cb-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="6f2cb-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="6f2cb-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="6f2cb-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="6f2cb-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="6f2cb-113">Representa una acción que envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="6f2cb-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6f2cb-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f2cb-114">Remarks</span></span>

<span data-ttu-id="6f2cb-115">Para el desarrollo de C++, vea [**from (propiedad de IEmailAction)**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from).</span><span class="sxs-lookup"><span data-stu-id="6f2cb-115">For C++ development, see [**From Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from).</span></span>

<span data-ttu-id="6f2cb-116">Para el desarrollo de scripts, vea [**EmailAction. from**](emailaction-from.md).</span><span class="sxs-lookup"><span data-stu-id="6f2cb-116">For script development, see [**EmailAction.From**](emailaction-from.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f2cb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f2cb-117">Requirements</span></span>



| <span data-ttu-id="6f2cb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f2cb-118">Requirement</span></span> | <span data-ttu-id="6f2cb-119">Value</span><span class="sxs-lookup"><span data-stu-id="6f2cb-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6f2cb-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f2cb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6f2cb-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6f2cb-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6f2cb-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f2cb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6f2cb-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f2cb-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





