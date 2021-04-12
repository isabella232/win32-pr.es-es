---
title: Elemento BODY (showMessageType)
description: Contiene el texto que se va a mostrar en el cuerpo del cuadro de mensaje.
ms.assetid: 69ea872a-7ca1-4464-9380-b35f74c9cb8e
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
ms.openlocfilehash: 3486601153f8e9dd7dac14f83800dae00a79a9f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491362"
---
# <a name="body-showmessagetype-element"></a><span data-ttu-id="35cea-104">Elemento BODY (showMessageType)</span><span class="sxs-lookup"><span data-stu-id="35cea-104">Body (showMessageType) Element</span></span>

<span data-ttu-id="35cea-105">Contiene el texto que se va a mostrar en el cuerpo del cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="35cea-105">Contains the text to display in the body of the message box.</span></span>

``` syntax
<xs:element name="Body"
    type="nonEmptyString"
 />
```

<span data-ttu-id="35cea-106">El elemento **Body** se define mediante el tipo complejo de [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="35cea-106">The **Body** element is defined by the [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="35cea-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="35cea-107">Parent element</span></span>



| <span data-ttu-id="35cea-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="35cea-108">Element</span></span>                                                                                  | <span data-ttu-id="35cea-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="35cea-109">Derived from</span></span>                                                               | <span data-ttu-id="35cea-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="35cea-110">Description</span></span>                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="35cea-111">**ShowMessage (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="35cea-111">**ShowMessage (actionGroup)**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="35cea-112">**showMessageType**</span><span class="sxs-lookup"><span data-stu-id="35cea-112">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="35cea-113">Representa una acción que muestra un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="35cea-113">Represents an action that shows a message box.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="35cea-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35cea-114">Remarks</span></span>

<span data-ttu-id="35cea-115">Para el desarrollo de C++, consulte la [**propiedad MessageBody de IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).</span><span class="sxs-lookup"><span data-stu-id="35cea-115">For C++ development, see [**MessageBody Property of IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).</span></span>

<span data-ttu-id="35cea-116">Para el desarrollo de scripts, vea [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md).</span><span class="sxs-lookup"><span data-stu-id="35cea-116">For script development, see [**ShowMessageAction.MessageBody**](showmessageaction-messagebody.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35cea-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35cea-117">Requirements</span></span>



| <span data-ttu-id="35cea-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="35cea-118">Requirement</span></span> | <span data-ttu-id="35cea-119">Value</span><span class="sxs-lookup"><span data-stu-id="35cea-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="35cea-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35cea-120">Minimum supported client</span></span><br/> | <span data-ttu-id="35cea-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="35cea-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="35cea-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35cea-122">Minimum supported server</span></span><br/> | <span data-ttu-id="35cea-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="35cea-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





