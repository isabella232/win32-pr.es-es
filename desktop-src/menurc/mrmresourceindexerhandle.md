---
title: Estructura MrmResourceIndexerHandle (MrmResourceIndexer. h)
description: Representa un identificador opaco para un objeto de indexador de recursos. El sistema operativo administra el identificador. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: E3ED8AB8-39B8-419C-9570-1CC6B2CFE8D0
keywords:
- Menús de la estructura MrmResourceIndexerHandle y otros recursos
- PMrmResourceIndexerHandle menús de puntero de estructura y otros recursos
topic_type:
- apiref
api_name:
- MrmResourceIndexerHandle
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5786585597b5d23a6f6c0cd6842b655727c3ffe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422609"
---
# <a name="mrmresourceindexerhandle-structure"></a><span data-ttu-id="5ce1a-107">Estructura MrmResourceIndexerHandle</span><span class="sxs-lookup"><span data-stu-id="5ce1a-107">MrmResourceIndexerHandle structure</span></span>

<span data-ttu-id="5ce1a-108">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="5ce1a-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5ce1a-109">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="5ce1a-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5ce1a-110">Representa un identificador opaco para un objeto de indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="5ce1a-110">Represents an opaque handle to a resource indexer object.</span></span> <span data-ttu-id="5ce1a-111">El sistema operativo administra el identificador.</span><span class="sxs-lookup"><span data-stu-id="5ce1a-111">The handle is managed by the operating system.</span></span> <span data-ttu-id="5ce1a-112">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="5ce1a-112">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="5ce1a-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ce1a-113">Syntax</span></span>


```C++
typedef struct _MrmResourceIndexerHandle {
  PVOID handle;
} MrmResourceIndexerHandle, *PMrmResourceIndexerHandle;
```



## <a name="members"></a><span data-ttu-id="5ce1a-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="5ce1a-114">Members</span></span>

<dl> <dt>

<span data-ttu-id="5ce1a-115">**asa**</span><span class="sxs-lookup"><span data-stu-id="5ce1a-115">**handle**</span></span>
</dt> <dd>

<span data-ttu-id="5ce1a-116">Tipo: **PVOID**</span><span class="sxs-lookup"><span data-stu-id="5ce1a-116">Type: **PVOID**</span></span>

</dd> <dd>

<span data-ttu-id="5ce1a-117">Un identificador opaco para un objeto de indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="5ce1a-117">An opaque handle to a resource indexer object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ce1a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ce1a-118">Requirements</span></span>



| <span data-ttu-id="5ce1a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ce1a-119">Requirement</span></span> | <span data-ttu-id="5ce1a-120">Value</span><span class="sxs-lookup"><span data-stu-id="5ce1a-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ce1a-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ce1a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5ce1a-122">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="5ce1a-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5ce1a-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ce1a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5ce1a-124">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="5ce1a-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5ce1a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ce1a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ce1a-126"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ce1a-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ce1a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ce1a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ce1a-128">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="5ce1a-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

