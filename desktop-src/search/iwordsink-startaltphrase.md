---
description: Indica el límite entre frases en una secuencia de frases alternativas que un separador de palabras genera durante el tiempo de índice.
ms.assetid: 3F3B6761-887B-426E-A44F-E636397180C7
title: 'IWordSink:: StartAltPhrase (método) (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.StartAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: e4e35c5ed75016292dd420e7a832c6cfb780284a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275253"
---
# <a name="iwordsinkstartaltphrase-method"></a><span data-ttu-id="956e2-103">IWordSink:: StartAltPhrase (método)</span><span class="sxs-lookup"><span data-stu-id="956e2-103">IWordSink::StartAltPhrase method</span></span>

<span data-ttu-id="956e2-104">Indica el límite entre frases en una secuencia de frases alternativas que un separador de palabras genera durante el tiempo de índice.</span><span class="sxs-lookup"><span data-stu-id="956e2-104">Indicates the boundary between phrases in a sequence of alternative phrases that a word breaker generates during index time.</span></span>

## <a name="syntax"></a><span data-ttu-id="956e2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="956e2-105">Syntax</span></span>


```C++
HRESULT StartAltPhrase();
```



## <a name="parameters"></a><span data-ttu-id="956e2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="956e2-106">Parameters</span></span>

<span data-ttu-id="956e2-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="956e2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="956e2-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="956e2-108">Return value</span></span>

<span data-ttu-id="956e2-109">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="956e2-109">This method can return one of these values.</span></span>



| <span data-ttu-id="956e2-110">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="956e2-110">Return code</span></span>                                                                                           | <span data-ttu-id="956e2-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="956e2-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="956e2-112"><dt>**WBREAK \_ E \_ \_ solo consulta**</dt></span><span class="sxs-lookup"><span data-stu-id="956e2-112"><dt>**WBREAK\_E\_QUERY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="956e2-113">Se llama a [**StartAltPhrase**](iwordsink-startaltphrase.md) durante el tiempo de la consulta.</span><span class="sxs-lookup"><span data-stu-id="956e2-113">[**StartAltPhrase**](iwordsink-startaltphrase.md) is called during query time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="956e2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="956e2-114">Remarks</span></span>

<span data-ttu-id="956e2-115">Cada frase alternativa comienza con una llamada a **StartAltPhrase** .</span><span class="sxs-lookup"><span data-stu-id="956e2-115">Each alternative phrase starts with a **StartAltPhrase** call.</span></span> <span data-ttu-id="956e2-116">La frase se coloca en el objeto [**IWordSink**](iwordsink.md) a través de las llamadas subsiguientes al método [**IWordSink::P utword**](iwordsink-putword.md) o [**IWordSink::P utaltword**](iwordsink-putaltword.md) .</span><span class="sxs-lookup"><span data-stu-id="956e2-116">The phrase is put in the [**IWordSink**](iwordsink.md) object through subsequent calls to the [**IWordSink::PutWord**](iwordsink-putword.md) or [**IWordSink::PutAltWord**](iwordsink-putaltword.md) method.</span></span> <span data-ttu-id="956e2-117">La frase alternativa final en una secuencia de frases finaliza con una llamada al método [**IWordSink:: EndAltPhrase**](iwordsink-endaltphrase.md) .</span><span class="sxs-lookup"><span data-stu-id="956e2-117">The final alternative phrase in a sequence of phrases is terminated with a call to the [**IWordSink::EndAltPhrase**](iwordsink-endaltphrase.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="956e2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="956e2-118">Requirements</span></span>



| <span data-ttu-id="956e2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="956e2-119">Requirement</span></span> | <span data-ttu-id="956e2-120">Value</span><span class="sxs-lookup"><span data-stu-id="956e2-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="956e2-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="956e2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="956e2-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="956e2-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="956e2-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="956e2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="956e2-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="956e2-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="956e2-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="956e2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="956e2-126"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="956e2-126"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="956e2-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="956e2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="956e2-128">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="956e2-128">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 




