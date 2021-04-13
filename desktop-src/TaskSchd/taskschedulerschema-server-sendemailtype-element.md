---
title: Server (sendEmailType) (elemento)
description: Contiene el servidor de correo electrónico que se usa para enviar el mensaje de correo electrónico.
ms.assetid: 4c6084d1-70c5-4d8b-8fcb-ab4cd8aab441
keywords:
- Programador de tareas del elemento Server
topic_type:
- apiref
api_name:
- Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5fc57ddf5deee52ff9b118a8267eec4069108030
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422032"
---
# <a name="server-sendemailtype-element"></a><span data-ttu-id="6b156-104">Server (sendEmailType) (elemento)</span><span class="sxs-lookup"><span data-stu-id="6b156-104">Server (sendEmailType) Element</span></span>

<span data-ttu-id="6b156-105">Contiene el servidor de correo electrónico que se usa para enviar el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="6b156-105">Contains the email server used to send the email message.</span></span>

``` syntax
<xs:element name="Server"
    type="nonEmptyString"
 />
```

<span data-ttu-id="6b156-106">El elemento **Server** se define mediante el tipo complejo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6b156-106">The **Server** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6b156-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="6b156-107">Parent element</span></span>



| <span data-ttu-id="6b156-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="6b156-108">Element</span></span>                                                                              | <span data-ttu-id="6b156-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="6b156-109">Derived from</span></span>                                                           | <span data-ttu-id="6b156-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b156-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="6b156-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="6b156-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="6b156-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="6b156-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="6b156-113">Representa una acción que envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="6b156-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6b156-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b156-114">Remarks</span></span>

<span data-ttu-id="6b156-115">Para el desarrollo de C++, vea [**Server Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server).</span><span class="sxs-lookup"><span data-stu-id="6b156-115">For C++ development, see [**Server Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server).</span></span>

<span data-ttu-id="6b156-116">Para el desarrollo de scripts, vea [**EmailAction. Server**](emailaction-server.md).</span><span class="sxs-lookup"><span data-stu-id="6b156-116">For script development, see [**EmailAction.Server**](emailaction-server.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b156-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b156-117">Requirements</span></span>



| <span data-ttu-id="6b156-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b156-118">Requirement</span></span> | <span data-ttu-id="6b156-119">Value</span><span class="sxs-lookup"><span data-stu-id="6b156-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6b156-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b156-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6b156-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6b156-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6b156-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b156-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6b156-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6b156-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





