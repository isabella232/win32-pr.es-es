---
title: BCC (sendEmailType), elemento
description: Contiene las direcciones de correo electrónico utilizadas en la línea CCO de un mensaje de correo electrónico.
ms.assetid: c80407d0-3b3f-4efe-91de-7a3a7abc996f
keywords:
- Elemento BCC Programador de tareas
topic_type:
- apiref
api_name:
- Bcc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f262b8f5d74018a4622f915def85df5e16108cdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150509"
---
# <a name="bcc-sendemailtype-element"></a><span data-ttu-id="81bde-104">BCC (sendEmailType), elemento</span><span class="sxs-lookup"><span data-stu-id="81bde-104">Bcc (sendEmailType) Element</span></span>

<span data-ttu-id="81bde-105">Contiene las direcciones de correo electrónico utilizadas en la línea CCO de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="81bde-105">Contains the email addresses used on the Bcc line of an email message.</span></span>

``` syntax
<xs:element name="Bcc"
    type="string"
 />
```

<span data-ttu-id="81bde-106">El elemento **BCC** se define mediante el tipo complejo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="81bde-106">The **Bcc** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="81bde-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="81bde-107">Parent element</span></span>



| <span data-ttu-id="81bde-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="81bde-108">Element</span></span>                                                                              | <span data-ttu-id="81bde-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="81bde-109">Derived from</span></span>                                                           | <span data-ttu-id="81bde-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="81bde-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="81bde-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="81bde-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="81bde-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="81bde-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="81bde-113">Representa una acción que envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="81bde-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="81bde-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81bde-114">Remarks</span></span>

<span data-ttu-id="81bde-115">Para el desarrollo de C++, vea la [**propiedad BCC de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).</span><span class="sxs-lookup"><span data-stu-id="81bde-115">For C++ development, see [**Bcc Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).</span></span>

<span data-ttu-id="81bde-116">Para el desarrollo de scripts, vea [**EmailAction. BCC**](emailaction-bcc.md).</span><span class="sxs-lookup"><span data-stu-id="81bde-116">For script development, see [**EmailAction.Bcc**](emailaction-bcc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81bde-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81bde-117">Requirements</span></span>



| <span data-ttu-id="81bde-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="81bde-118">Requirement</span></span> | <span data-ttu-id="81bde-119">Value</span><span class="sxs-lookup"><span data-stu-id="81bde-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="81bde-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81bde-120">Minimum supported client</span></span><br/> | <span data-ttu-id="81bde-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="81bde-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="81bde-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81bde-122">Minimum supported server</span></span><br/> | <span data-ttu-id="81bde-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="81bde-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





