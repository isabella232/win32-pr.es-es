---
title: Elemento title (showMessageType)
description: Contiene el título del cuadro de mensaje.
ms.assetid: 089d2043-41ed-4050-b794-af24ab7ac8b9
keywords:
- Elemento title Programador de tareas
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca5baa7135579ff673ba9b01a672a126924d1d49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150008"
---
# <a name="title-showmessagetype-element"></a><span data-ttu-id="aa8e6-104">Elemento title (showMessageType)</span><span class="sxs-lookup"><span data-stu-id="aa8e6-104">Title (showMessageType) Element</span></span>

<span data-ttu-id="aa8e6-105">Contiene el título del cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="aa8e6-105">Contains the title of the message box.</span></span>

``` syntax
<xs:element name="Title"
    type="nonEmptyString"
 />
```

<span data-ttu-id="aa8e6-106">El elemento de **título** se define mediante el tipo complejo de [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="aa8e6-106">The **Title** element is defined by the [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="aa8e6-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="aa8e6-107">Parent element</span></span>



| <span data-ttu-id="aa8e6-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="aa8e6-108">Element</span></span>                                                                                  | <span data-ttu-id="aa8e6-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="aa8e6-109">Derived from</span></span>                                                               | <span data-ttu-id="aa8e6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa8e6-110">Description</span></span>                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="aa8e6-111">**ShowMessage (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="aa8e6-111">**ShowMessage (actionGroup)**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="aa8e6-112">**showMessageType**</span><span class="sxs-lookup"><span data-stu-id="aa8e6-112">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="aa8e6-113">Representa una acción que muestra un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="aa8e6-113">Represents an action that shows a message box.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="aa8e6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa8e6-114">Remarks</span></span>

<span data-ttu-id="aa8e6-115">Para el desarrollo de C++, vea la [**propiedad title de IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).</span><span class="sxs-lookup"><span data-stu-id="aa8e6-115">For C++ development, see [**Title Property of IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).</span></span>

<span data-ttu-id="aa8e6-116">Para el desarrollo de scripts, vea [**ShowMessageAction. title**](showmessageaction-title.md).</span><span class="sxs-lookup"><span data-stu-id="aa8e6-116">For script development, see [**ShowMessageAction.Title**](showmessageaction-title.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa8e6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa8e6-117">Requirements</span></span>



| <span data-ttu-id="aa8e6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa8e6-118">Requirement</span></span> | <span data-ttu-id="aa8e6-119">Value</span><span class="sxs-lookup"><span data-stu-id="aa8e6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aa8e6-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa8e6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aa8e6-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="aa8e6-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aa8e6-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa8e6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aa8e6-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa8e6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





