---
description: Coloca una palabra y su posición en el objeto IWordSink.
ms.assetid: 3D645BF6-895E-46E2-92A3-3E301CD228D8
title: IWordSink::P método utWord (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 5f622e09c2b82bc8de986dafcc83247617caec75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696275"
---
# <a name="iwordsinkputword-method"></a><span data-ttu-id="39460-103">IWordSink::P método utWord</span><span class="sxs-lookup"><span data-stu-id="39460-103">IWordSink::PutWord method</span></span>

<span data-ttu-id="39460-104">Coloca una palabra y su posición en el objeto [**IWordSink**](iwordsink.md) .</span><span class="sxs-lookup"><span data-stu-id="39460-104">Puts a word and its position in the [**IWordSink**](iwordsink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="39460-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39460-105">Syntax</span></span>


```C++
HRESULT PutWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a><span data-ttu-id="39460-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39460-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39460-107">*CWC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="39460-107">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39460-108">Número de caracteres de *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="39460-108">The number of characters in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="39460-109">*pwcInBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="39460-109">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39460-110">Un puntero a un búfer que contiene una forma alternativa de una palabra del texto de origen.</span><span class="sxs-lookup"><span data-stu-id="39460-110">A pointer to a buffer that contains an alternative form of a word from the source text.</span></span> <span data-ttu-id="39460-111">**PutWord** no modifica este parámetro.</span><span class="sxs-lookup"><span data-stu-id="39460-111">This parameter is not modified by **PutWord**.</span></span> <span data-ttu-id="39460-112">Puede pasar el parámetro *pTextSource* de [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) según corresponda.</span><span class="sxs-lookup"><span data-stu-id="39460-112">You can pass the *pTextSource* parameter from [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) as appropriate.</span></span>

</dd> <dt>

<span data-ttu-id="39460-113">*cwcSrcLen* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="39460-113">*cwcSrcLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39460-114">Número de caracteres del búfer de texto de origen (indicado por el parámetro *pTextSource* en [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) que corresponden a la palabra contenida en *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="39460-114">The number of characters in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) that correspond to the word contained in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="39460-115">*cwcSrcPos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="39460-115">*cwcSrcPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39460-116">Posición inicial de la palabra en *pwcInBuf* en el búfer de texto de origen (indicado por el parámetro *pTextSource* a [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span><span class="sxs-lookup"><span data-stu-id="39460-116">The starting position of the word in *pwcInBuf* in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39460-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39460-117">Return value</span></span>

<span data-ttu-id="39460-118">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="39460-118">This method can return one of these values.</span></span>



| <span data-ttu-id="39460-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="39460-119">Return code</span></span>                                                                                              | <span data-ttu-id="39460-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="39460-120">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="39460-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="39460-121"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="39460-122">La operación se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="39460-122">The operation was completed successfully.</span></span> <span data-ttu-id="39460-123">También indica que no hay más texto disponible para rellenar el búfer.</span><span class="sxs-lookup"><span data-stu-id="39460-123">Also indicates that no more text is available to refill the buffer.</span></span><br/>                                  |
| <dl> <span data-ttu-id="39460-124"><dt>**Idioma \_ de \_ \_ palabra S grande**</dt></span><span class="sxs-lookup"><span data-stu-id="39460-124"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="39460-125">El valor de *CWC* es mayor que el valor de *ulMaxTokenSize* que se especifica en [**IWordBreaker:: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span><span class="sxs-lookup"><span data-stu-id="39460-125">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IWordBreaker::Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="39460-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39460-126">Remarks</span></span>

<span data-ttu-id="39460-127">Se recomienda que el método **IWordSink::P utword** contenga siempre la palabra original como se encuentra en *pTextSource*.</span><span class="sxs-lookup"><span data-stu-id="39460-127">We recommend that the **IWordSink::PutWord** method always contain the original word as found in *pTextSource*.</span></span> <span data-ttu-id="39460-128">Las formas alternativas de la palabra se pasan a WordSink mediante [**IWordSink::P utaltword**](iwordsink-putaltword.md).</span><span class="sxs-lookup"><span data-stu-id="39460-128">Alternative forms of the word are passed to WordSink by using [**IWordSink::PutAltWord**](iwordsink-putaltword.md).</span></span> <span data-ttu-id="39460-129">También se recomienda que las palabras de *pwcInBuf* coincidan con el texto de origen lo más cerca posible.</span><span class="sxs-lookup"><span data-stu-id="39460-129">We also recommend that the words in *pwcInBuf* match the source text as closely as possible.</span></span> <span data-ttu-id="39460-130">Por ejemplo, conserve las mayúsculas y los acentos siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="39460-130">For example, retain capitalization and accents where possible.</span></span>

<span data-ttu-id="39460-131">Esta llamada se debe realizar para cada palabra recuperada de *pTextSource* , excepto aquellas para las que se realizó la llamada a [**utaltword de IWordSink::P**](iwordsink-putaltword.md) .</span><span class="sxs-lookup"><span data-stu-id="39460-131">This call must be made for every word retrieved from *pTextSource* except those for which the [**IWordSink::PutAltWord**](iwordsink-putaltword.md) call was made.</span></span> <span data-ttu-id="39460-132">La palabra se termina con un carácter EOW cuando se guarda en WordSink.</span><span class="sxs-lookup"><span data-stu-id="39460-132">The word is terminated with an EOW character when it is saved to the WordSink.</span></span>

## <a name="requirements"></a><span data-ttu-id="39460-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39460-133">Requirements</span></span>



| <span data-ttu-id="39460-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="39460-134">Requirement</span></span> | <span data-ttu-id="39460-135">Value</span><span class="sxs-lookup"><span data-stu-id="39460-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="39460-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39460-136">Minimum supported client</span></span><br/> | <span data-ttu-id="39460-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="39460-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="39460-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39460-138">Minimum supported server</span></span><br/> | <span data-ttu-id="39460-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="39460-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="39460-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39460-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="39460-141"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="39460-141"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39460-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="39460-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39460-143">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="39460-143">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
