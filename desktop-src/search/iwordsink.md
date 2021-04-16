---
description: Controla las palabras identificadas por los saltos de palabra durante el tiempo de índice y el tiempo de consulta.
ms.assetid: 220FCAE5-D22D-45ED-9689-E78C0D8E0BB3
title: Interfaz IWordSink (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 2eab8eee4f7b07b0f712e68d7ad05b970506b00b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696274"
---
# <a name="iwordsink-interface"></a><span data-ttu-id="3e213-103">Interfaz IWordSink</span><span class="sxs-lookup"><span data-stu-id="3e213-103">IWordSink interface</span></span>

<span data-ttu-id="3e213-104">Controla las palabras identificadas por los saltos de palabra durante el tiempo de índice y el tiempo de consulta.</span><span class="sxs-lookup"><span data-stu-id="3e213-104">Handles words identified by word breaks during both index time and query time.</span></span>

## <a name="members"></a><span data-ttu-id="3e213-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="3e213-105">Members</span></span>

<span data-ttu-id="3e213-106">La interfaz **IWordSink** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3e213-106">The **IWordSink** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3e213-107">**IWordSink** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3e213-107">**IWordSink** also has these types of members:</span></span>

-   [<span data-ttu-id="3e213-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="3e213-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3e213-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="3e213-109">Methods</span></span>

<span data-ttu-id="3e213-110">La interfaz **IWordSink** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3e213-110">The **IWordSink** interface has these methods.</span></span>



| <span data-ttu-id="3e213-111">Método</span><span class="sxs-lookup"><span data-stu-id="3e213-111">Method</span></span>                                             | <span data-ttu-id="3e213-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e213-112">Description</span></span>                                                                                                                             |
|:---------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e213-113">**EndAltPhrase**</span><span class="sxs-lookup"><span data-stu-id="3e213-113">**EndAltPhrase**</span></span>](iwordsink-endaltphrase.md)     | <span data-ttu-id="3e213-114">Indica el final de la frase final en una secuencia de frases alternativas que un separador de palabras genera durante el tiempo de índice.</span><span class="sxs-lookup"><span data-stu-id="3e213-114">Indicates the end of the final phrase in a sequence of alternative phrases that a word breaker generates during index time.</span></span><br/>  |
| [<span data-ttu-id="3e213-115">**PutAltWord**</span><span class="sxs-lookup"><span data-stu-id="3e213-115">**PutAltWord**</span></span>](iwordsink-putaltword.md)         | <span data-ttu-id="3e213-116">Coloca una palabra alternativa y su posición en el objeto **IWordSink** .</span><span class="sxs-lookup"><span data-stu-id="3e213-116">Puts an alternative word and its position in the **IWordSink** object.</span></span><br/>                                                       |
| [<span data-ttu-id="3e213-117">**PutBreak**</span><span class="sxs-lookup"><span data-stu-id="3e213-117">**PutBreak**</span></span>](iwordsink-putbreak.md)             | <span data-ttu-id="3e213-118">Coloca un salto después de la palabra anterior.</span><span class="sxs-lookup"><span data-stu-id="3e213-118">Puts a break after the preceding word.</span></span><br/>                                                                                       |
| [<span data-ttu-id="3e213-119">**PutWord**</span><span class="sxs-lookup"><span data-stu-id="3e213-119">**PutWord**</span></span>](iwordsink-putword.md)               | <span data-ttu-id="3e213-120">Coloca una palabra y su posición en el objeto **IWordSink** .</span><span class="sxs-lookup"><span data-stu-id="3e213-120">Puts a word and its position in the **IWordSink** object.</span></span><br/>                                                                    |
| [<span data-ttu-id="3e213-121">**StartAltPhrase**</span><span class="sxs-lookup"><span data-stu-id="3e213-121">**StartAltPhrase**</span></span>](iwordsink-startaltphrase.md) | <span data-ttu-id="3e213-122">Indica el límite entre frases en una secuencia de frases alternativas que un separador de palabras genera durante el tiempo de índice.</span><span class="sxs-lookup"><span data-stu-id="3e213-122">Indicates the boundary between phrases in a sequence of alternative phrases that a word breaker generates during index time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3e213-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e213-123">Remarks</span></span>

<span data-ttu-id="3e213-124">Windows Search crea e inicializa instancias del objeto **IWordSink** .</span><span class="sxs-lookup"><span data-stu-id="3e213-124">Windows Search creates and initializes instances of the **IWordSink** object.</span></span> <span data-ttu-id="3e213-125">El objeto **IWordSink** recibe el parámetro *fQuery* durante la inicialización y utiliza este parámetro para determinar el contexto de separación de palabras en el que se usa el objeto.</span><span class="sxs-lookup"><span data-stu-id="3e213-125">The **IWordSink** object receives the *fQuery* parameter during initialization and uses this parameter to determine the word-breaking context in which the object is used.</span></span>

<span data-ttu-id="3e213-126">Las implementaciones de [**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) reciben un puntero al objeto **IWordSink** en el método [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) .</span><span class="sxs-lookup"><span data-stu-id="3e213-126">[**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) implementations receive a pointer to the **IWordSink** object in the [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e213-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e213-127">Requirements</span></span>



| <span data-ttu-id="3e213-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e213-128">Requirement</span></span> | <span data-ttu-id="3e213-129">Value</span><span class="sxs-lookup"><span data-stu-id="3e213-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3e213-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e213-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3e213-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3e213-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3e213-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e213-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3e213-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3e213-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3e213-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e213-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e213-135"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e213-135"><dt>Search.h</dt></span></span> </dl> |



 

 
