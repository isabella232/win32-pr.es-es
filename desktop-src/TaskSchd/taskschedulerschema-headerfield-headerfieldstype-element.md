---
title: Elemento HeaderField (headerFieldsType)
description: Contiene un campo para un encabezado en un mensaje de correo electrónico.
ms.assetid: ec6fc593-8798-4dd0-b589-48657b7cdeb1
keywords:
- Programador de tareas del elemento HeaderField
topic_type:
- apiref
api_name:
- HeaderField
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f7ac79a16bb0464f6e81d90eba38384a3c2b483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686229"
---
# <a name="headerfield-headerfieldstype-element"></a><span data-ttu-id="2c21f-104">Elemento HeaderField (headerFieldsType)</span><span class="sxs-lookup"><span data-stu-id="2c21f-104">HeaderField (headerFieldsType) Element</span></span>

<span data-ttu-id="2c21f-105">Contiene un campo para un encabezado en un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="2c21f-105">Contains a field for a header in an email message.</span></span>

``` syntax
<xs:element name="HeaderField"
    type="headerFieldType"
 />
```

<span data-ttu-id="2c21f-106">El elemento **HeaderField** se define mediante el tipo complejo de [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2c21f-106">The **HeaderField** element is defined by the [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="2c21f-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="2c21f-107">Parent element</span></span>



| <span data-ttu-id="2c21f-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="2c21f-108">Element</span></span>                                                                        | <span data-ttu-id="2c21f-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="2c21f-109">Derived from</span></span>                                                                 | <span data-ttu-id="2c21f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c21f-110">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c21f-111">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="2c21f-111">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="2c21f-112">**headerFieldsType**</span><span class="sxs-lookup"><span data-stu-id="2c21f-112">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="2c21f-113">Especifica los campos de encabezado y sus valores utilizados en el encabezado del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="2c21f-113">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="2c21f-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2c21f-114">Child elements</span></span>



| <span data-ttu-id="2c21f-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="2c21f-115">Element</span></span>                                                            | <span data-ttu-id="2c21f-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="2c21f-116">Type</span></span>                                                                    | <span data-ttu-id="2c21f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c21f-117">Description</span></span>                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="2c21f-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="2c21f-118">**Name**</span></span>](taskschedulerschema-name-headerfieldtype-element.md)   | [<span data-ttu-id="2c21f-119">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="2c21f-119">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="2c21f-120">Especifica el nombre del campo de encabezado en un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="2c21f-120">Specifies the name of the header field in an email message.</span></span><br/> |
| [<span data-ttu-id="2c21f-121">**Value**</span><span class="sxs-lookup"><span data-stu-id="2c21f-121">**Value**</span></span>](taskschedulerschema-value-headerfieldtype-element.md) | <span data-ttu-id="2c21f-122">**string**</span><span class="sxs-lookup"><span data-stu-id="2c21f-122">**string**</span></span>                                                              | <span data-ttu-id="2c21f-123">Especifica el valor de un campo de encabezado en un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="2c21f-123">Specifies the value of a header field in an email message.</span></span><br/>  |



## <a name="remarks"></a><span data-ttu-id="2c21f-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c21f-124">Remarks</span></span>

<span data-ttu-id="2c21f-125">Para el desarrollo de C++, consulte la [**propiedad HeaderFields de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span><span class="sxs-lookup"><span data-stu-id="2c21f-125">For C++ development, see [**HeaderFields Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span></span>

<span data-ttu-id="2c21f-126">Para el desarrollo de scripts, vea [**EmailAction. HeaderFields**](emailaction-headerfields.md).</span><span class="sxs-lookup"><span data-stu-id="2c21f-126">For script development, see [**EmailAction.HeaderFields**](emailaction-headerfields.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c21f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c21f-127">Requirements</span></span>



| <span data-ttu-id="2c21f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c21f-128">Requirement</span></span> | <span data-ttu-id="2c21f-129">Value</span><span class="sxs-lookup"><span data-stu-id="2c21f-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2c21f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c21f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2c21f-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2c21f-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2c21f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c21f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2c21f-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2c21f-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





