---
description: Indica el final de la frase final en una secuencia de frases alternativas que un separador de palabras genera durante el tiempo de índice.
ms.assetid: 50E4E208-A290-42B7-9152-9472C01B20D5
title: 'IWordSink:: EndAltPhrase (método) (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.EndAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 4056357de5e3e479124e8f9a91d9b3d906300709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275254"
---
# <a name="iwordsinkendaltphrase-method"></a><span data-ttu-id="3b755-103">IWordSink:: EndAltPhrase (método)</span><span class="sxs-lookup"><span data-stu-id="3b755-103">IWordSink::EndAltPhrase method</span></span>

<span data-ttu-id="3b755-104">Indica el final de la frase final en una secuencia de frases alternativas que un separador de palabras genera durante el tiempo de índice.</span><span class="sxs-lookup"><span data-stu-id="3b755-104">Indicates the end of the final phrase in a sequence of alternative phrases that a word breaker generates during index time.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b755-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b755-105">Syntax</span></span>


```C++
HRESULT EndAltPhrase();
```



## <a name="parameters"></a><span data-ttu-id="3b755-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b755-106">Parameters</span></span>

<span data-ttu-id="3b755-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3b755-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3b755-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b755-108">Return value</span></span>

<span data-ttu-id="3b755-109">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="3b755-109">This method can return one of these values.</span></span>



| <span data-ttu-id="3b755-110">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3b755-110">Return code</span></span>                                                                                           | <span data-ttu-id="3b755-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b755-111">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3b755-112"><dt>**WBREAK \_ E \_ \_ solo consulta**</dt></span><span class="sxs-lookup"><span data-stu-id="3b755-112"><dt>**WBREAK\_E\_QUERY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="3b755-113">Se llama a [**EndAltPhrase**](iwordsink-endaltphrase.md) durante el tiempo de la consulta.</span><span class="sxs-lookup"><span data-stu-id="3b755-113">[**EndAltPhrase**](iwordsink-endaltphrase.md) is called during query time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3b755-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b755-114">Remarks</span></span>

<span data-ttu-id="3b755-115">Las implementaciones de [**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) llaman a **IWordSink:: EndAltPhrase** desde el método [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) para terminar una secuencia de frases alternativas.</span><span class="sxs-lookup"><span data-stu-id="3b755-115">[**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) implementations call **IWordSink::EndAltPhrase** from the [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) method to terminate a sequence of alternative phrases.</span></span> <span data-ttu-id="3b755-116">Se llama al método [**IWordSink:: StartAltPhrase**](iwordsink-startaltphrase.md) para indicar el final de una frase y el principio de otra en una secuencia de frases.</span><span class="sxs-lookup"><span data-stu-id="3b755-116">The [**IWordSink::StartAltPhrase**](iwordsink-startaltphrase.md) method is called to indicate the end of one phrase and the beginning of another in a sequence of phrases.</span></span> <span data-ttu-id="3b755-117">Solo la última frase de una secuencia termina con una llamada a **EndAltPhrase**.</span><span class="sxs-lookup"><span data-stu-id="3b755-117">Only the last phrase in a sequence is terminated with a call to **EndAltPhrase**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b755-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b755-118">Requirements</span></span>



| <span data-ttu-id="3b755-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b755-119">Requirement</span></span> | <span data-ttu-id="3b755-120">Value</span><span class="sxs-lookup"><span data-stu-id="3b755-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3b755-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b755-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3b755-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3b755-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3b755-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b755-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3b755-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3b755-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3b755-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b755-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b755-126"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b755-126"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b755-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b755-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b755-128">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="3b755-128">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
