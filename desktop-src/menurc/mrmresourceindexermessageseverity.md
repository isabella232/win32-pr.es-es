---
title: Enumeración MrmResourceIndexerMessageSeverity (MrmResourceIndexer. h)
description: Define constantes que especifican la gravedad de un mensaje del indexador de recursos. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: A4734256-94BD-43BE-B93C-55B98DF8A9BF
keywords:
- Menús de enumeración de MrmResourceIndexerMessageSeverity y otros recursos
topic_type:
- apiref
api_name:
- MrmResourceIndexerMessageSeverity
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdcbb42291ab88e91eca6c16c0a6c95c3e89fd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665937"
---
# <a name="mrmresourceindexermessageseverity-enumeration"></a><span data-ttu-id="6bfe0-105">Enumeración MrmResourceIndexerMessageSeverity</span><span class="sxs-lookup"><span data-stu-id="6bfe0-105">MrmResourceIndexerMessageSeverity enumeration</span></span>

<span data-ttu-id="6bfe0-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="6bfe0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6bfe0-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="6bfe0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6bfe0-108">Define constantes que especifican la gravedad de un mensaje del indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="6bfe0-108">Defines constants that specify the severity of an resource indexer message.</span></span> <span data-ttu-id="6bfe0-109">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="6bfe0-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="6bfe0-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6bfe0-110">Syntax</span></span>


```C++
typedef enum _MrmResourceIndexerMessageSeverity { 
  MrmResourceIndexerMessageSeverityVerbose  = 1,
  MrmResourceIndexerMessageSeverityInfo     = 2,
  MrmResourceIndexerMessageSeverityWarning  = 3,
  MrmResourceIndexerMessageSeverityError    = 4
} MrmResourceIndexerMessageSeverity;
```



## <a name="constants"></a><span data-ttu-id="6bfe0-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="6bfe0-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6bfe0-112"><span id="MrmResourceIndexerMessageSeverityVerbose"></span><span id="mrmresourceindexermessageseverityverbose"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYVERBOSE"></span>**MrmResourceIndexerMessageSeverityVerbose**</span><span class="sxs-lookup"><span data-stu-id="6bfe0-112"><span id="MrmResourceIndexerMessageSeverityVerbose"></span><span id="mrmresourceindexermessageseverityverbose"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYVERBOSE"></span>**MrmResourceIndexerMessageSeverityVerbose**</span></span>
</dt> <dd>

<span data-ttu-id="6bfe0-113">Indica que el mensaje es detallado.</span><span class="sxs-lookup"><span data-stu-id="6bfe0-113">Indicates that the message is verbose.</span></span>

</dd> <dt>

<span data-ttu-id="6bfe0-114"><span id="MrmResourceIndexerMessageSeverityInfo"></span><span id="mrmresourceindexermessageseverityinfo"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYINFO"></span>**MrmResourceIndexerMessageSeverityInfo**</span><span class="sxs-lookup"><span data-stu-id="6bfe0-114"><span id="MrmResourceIndexerMessageSeverityInfo"></span><span id="mrmresourceindexermessageseverityinfo"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYINFO"></span>**MrmResourceIndexerMessageSeverityInfo**</span></span>
</dt> <dd>

<span data-ttu-id="6bfe0-115">Indica que el mensaje es informativo.</span><span class="sxs-lookup"><span data-stu-id="6bfe0-115">Indicates that the message is informational.</span></span>

</dd> <dt>

<span data-ttu-id="6bfe0-116"><span id="MrmResourceIndexerMessageSeverityWarning"></span><span id="mrmresourceindexermessageseveritywarning"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYWARNING"></span>**MrmResourceIndexerMessageSeverityWarning**</span><span class="sxs-lookup"><span data-stu-id="6bfe0-116"><span id="MrmResourceIndexerMessageSeverityWarning"></span><span id="mrmresourceindexermessageseveritywarning"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYWARNING"></span>**MrmResourceIndexerMessageSeverityWarning**</span></span>
</dt> <dd>

<span data-ttu-id="6bfe0-117">Indica que el mensaje es una advertencia.</span><span class="sxs-lookup"><span data-stu-id="6bfe0-117">Indicates that the message is a warning.</span></span>

</dd> <dt>

<span data-ttu-id="6bfe0-118"><span id="MrmResourceIndexerMessageSeverityError"></span><span id="mrmresourceindexermessageseverityerror"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYERROR"></span>**MrmResourceIndexerMessageSeverityError**</span><span class="sxs-lookup"><span data-stu-id="6bfe0-118"><span id="MrmResourceIndexerMessageSeverityError"></span><span id="mrmresourceindexermessageseverityerror"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYERROR"></span>**MrmResourceIndexerMessageSeverityError**</span></span>
</dt> <dd>

<span data-ttu-id="6bfe0-119">Indica que el mensaje es un error.</span><span class="sxs-lookup"><span data-stu-id="6bfe0-119">Indicates that the message is an error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6bfe0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bfe0-120">Requirements</span></span>



| <span data-ttu-id="6bfe0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bfe0-121">Requirement</span></span> | <span data-ttu-id="6bfe0-122">Value</span><span class="sxs-lookup"><span data-stu-id="6bfe0-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bfe0-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bfe0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6bfe0-124">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="6bfe0-124">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6bfe0-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bfe0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6bfe0-126">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="6bfe0-126">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6bfe0-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6bfe0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bfe0-128"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bfe0-128"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bfe0-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="6bfe0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bfe0-130">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="6bfe0-130">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

