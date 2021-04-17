---
title: Elemento CC (sendEmailType)
description: Contiene las direcciones de correo electrónico utilizadas en la línea CC de un mensaje de correo electrónico.
ms.assetid: cb8bc5b3-c352-43e3-bf28-d2090a519c7f
keywords:
- Elemento CC Programador de tareas
topic_type:
- apiref
api_name:
- Cc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bc49f2d7eebc2fbb1b5818fee2efa0e54f579a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491686"
---
# <a name="cc-sendemailtype-element"></a><span data-ttu-id="bebb6-104">Elemento CC (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="bebb6-104">Cc (sendEmailType) Element</span></span>

<span data-ttu-id="bebb6-105">Contiene las direcciones de correo electrónico utilizadas en la línea CC de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="bebb6-105">Contains the email addresses used on the Cc line of an email message.</span></span>

``` syntax
<xs:element name="Cc"
    type="string"
 />
```

<span data-ttu-id="bebb6-106">El elemento **CC** se define mediante el tipo complejo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bebb6-106">The **Cc** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bebb6-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="bebb6-107">Parent element</span></span>



| <span data-ttu-id="bebb6-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="bebb6-108">Element</span></span>                                                                              | <span data-ttu-id="bebb6-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="bebb6-109">Derived from</span></span>                                                           | <span data-ttu-id="bebb6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="bebb6-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="bebb6-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="bebb6-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="bebb6-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="bebb6-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="bebb6-113">Representa una acción que envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="bebb6-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bebb6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bebb6-114">Remarks</span></span>

<span data-ttu-id="bebb6-115">Para el desarrollo de C++, vea [**propiedad CC de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc).</span><span class="sxs-lookup"><span data-stu-id="bebb6-115">For C++ development, see [**Cc Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc).</span></span>

<span data-ttu-id="bebb6-116">Para el desarrollo de scripts, vea [**EmailAction.CC**](emailaction-cc.md).</span><span class="sxs-lookup"><span data-stu-id="bebb6-116">For script development, see [**EmailAction.Cc**](emailaction-cc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bebb6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bebb6-117">Requirements</span></span>



| <span data-ttu-id="bebb6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bebb6-118">Requirement</span></span> | <span data-ttu-id="bebb6-119">Value</span><span class="sxs-lookup"><span data-stu-id="bebb6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bebb6-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bebb6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bebb6-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bebb6-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bebb6-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bebb6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bebb6-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bebb6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





