---
title: Elemento HeaderFields (sendEmailType)
description: Especifica los campos de encabezado y sus valores utilizados en el encabezado del mensaje de correo electrónico.
ms.assetid: 6261f32e-3012-4ce7-b407-699374596333
keywords:
- Programador de tareas del elemento HeaderFields
topic_type:
- apiref
api_name:
- HeaderFields
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d108f1c31b8253046ccdbf09312df4f54c7335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534576"
---
# <a name="headerfields-sendemailtype-element"></a><span data-ttu-id="479f1-104">Elemento HeaderFields (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="479f1-104">HeaderFields (sendEmailType) Element</span></span>

<span data-ttu-id="479f1-105">Especifica los campos de encabezado y sus valores utilizados en el encabezado del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="479f1-105">Specifies the header fields and their values used in the header of the email message.</span></span>

``` syntax
<xs:element name="HeaderFields"
    type="headerFieldsType"
 />
```

<span data-ttu-id="479f1-106">El elemento **HeaderFields** se define mediante el tipo complejo de [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="479f1-106">The **HeaderFields** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="479f1-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="479f1-107">Parent element</span></span>



| <span data-ttu-id="479f1-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="479f1-108">Element</span></span>                                                                              | <span data-ttu-id="479f1-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="479f1-109">Derived from</span></span>                                                           | <span data-ttu-id="479f1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="479f1-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="479f1-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="479f1-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="479f1-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="479f1-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="479f1-113">Representa una acción que envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="479f1-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="479f1-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="479f1-114">Child elements</span></span>



| <span data-ttu-id="479f1-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="479f1-115">Element</span></span>                                                                         | <span data-ttu-id="479f1-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="479f1-116">Type</span></span>                                                                       | <span data-ttu-id="479f1-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="479f1-117">Description</span></span>                                                    |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="479f1-118">**HeaderField**</span><span class="sxs-lookup"><span data-stu-id="479f1-118">**HeaderField**</span></span>](taskschedulerschema-headerfield-headerfieldstype-element.md) | [<span data-ttu-id="479f1-119">**headerFieldType**</span><span class="sxs-lookup"><span data-stu-id="479f1-119">**headerFieldType**</span></span>](taskschedulerschema-headerfieldtype-complextype.md) | <span data-ttu-id="479f1-120">Contiene un campo para un encabezado en un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="479f1-120">Contains a field for a header in an email message.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="479f1-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="479f1-121">Remarks</span></span>

<span data-ttu-id="479f1-122">Para el desarrollo de C++, consulte la [**propiedad HeaderFields de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span><span class="sxs-lookup"><span data-stu-id="479f1-122">For C++ development, see [**HeaderFields Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span></span>

<span data-ttu-id="479f1-123">Para el desarrollo de scripts, vea [**EmailAction. HeaderFields**](emailaction-headerfields.md).</span><span class="sxs-lookup"><span data-stu-id="479f1-123">For script development, see [**EmailAction.HeaderFields**](emailaction-headerfields.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="479f1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="479f1-124">Requirements</span></span>



| <span data-ttu-id="479f1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="479f1-125">Requirement</span></span> | <span data-ttu-id="479f1-126">Value</span><span class="sxs-lookup"><span data-stu-id="479f1-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="479f1-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="479f1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="479f1-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="479f1-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="479f1-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="479f1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="479f1-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="479f1-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





