---
title: Elemento Attachments (sendEmailType)
description: Contiene una lista de datos adjuntos en el mensaje de correo electrónico.
ms.assetid: 5ae22481-af70-42eb-a964-e63d800be17d
keywords:
- Elemento Attachments Programador de tareas
topic_type:
- apiref
api_name:
- Attachments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67eed8f82f0caa27f44070bd109d4fa4560472eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803229"
---
# <a name="attachments-sendemailtype-element"></a><span data-ttu-id="4c8da-104">Elemento Attachments (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="4c8da-104">Attachments (sendEmailType) Element</span></span>

<span data-ttu-id="4c8da-105">Contiene una lista de datos adjuntos en el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4c8da-105">Contains a list of attachments in the email message.</span></span>

``` syntax
<xs:element name="Attachments"
    type="attachmentsType"
 />
```

<span data-ttu-id="4c8da-106">El elemento **Attachments** se define mediante el tipo complejo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4c8da-106">The **Attachments** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4c8da-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="4c8da-107">Parent element</span></span>



| <span data-ttu-id="4c8da-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="4c8da-108">Element</span></span>                                                                              | <span data-ttu-id="4c8da-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="4c8da-109">Derived from</span></span>                                                           | <span data-ttu-id="4c8da-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c8da-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="4c8da-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="4c8da-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="4c8da-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="4c8da-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="4c8da-113">Representa una acción que envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4c8da-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="4c8da-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4c8da-114">Child elements</span></span>



| <span data-ttu-id="4c8da-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="4c8da-115">Element</span></span>                                                          | <span data-ttu-id="4c8da-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="4c8da-116">Type</span></span>                                                                    | <span data-ttu-id="4c8da-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c8da-117">Description</span></span>                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c8da-118">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="4c8da-118">**File**</span></span>](taskschedulerschema-file-attachmentstype-element.md) | [<span data-ttu-id="4c8da-119">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="4c8da-119">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="4c8da-120">Especifica la ruta de acceso a un archivo que se envía como datos adjuntos en un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4c8da-120">Specifies the path to a file that is sent as an attachment in an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4c8da-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c8da-121">Remarks</span></span>

<span data-ttu-id="4c8da-122">Para el desarrollo de C++, vea la [**propiedad Attachments de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span><span class="sxs-lookup"><span data-stu-id="4c8da-122">For C++ development, see [**Attachments Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span></span>

<span data-ttu-id="4c8da-123">Para el desarrollo de scripts, vea [**EmailAction. Attachments**](emailaction-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="4c8da-123">For script development, see [**EmailAction.Attachments**](emailaction-attachments.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c8da-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c8da-124">Requirements</span></span>



| <span data-ttu-id="4c8da-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c8da-125">Requirement</span></span> | <span data-ttu-id="4c8da-126">Value</span><span class="sxs-lookup"><span data-stu-id="4c8da-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4c8da-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c8da-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4c8da-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4c8da-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4c8da-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c8da-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4c8da-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4c8da-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





