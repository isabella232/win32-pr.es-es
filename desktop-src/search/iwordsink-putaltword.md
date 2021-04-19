---
description: Coloca una palabra alternativa y su posición en el objeto IWordSink.
ms.assetid: 5C8A9B30-F9B5-42E9-ADAC-A11230F0C2FA
title: IWordSink::P método utAltWord (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 21fd9eb9ac5a1bf0f52d6574595dc495432d7ec9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696276"
---
# <a name="iwordsinkputaltword-method"></a><span data-ttu-id="37f1b-103">IWordSink::P método utAltWord</span><span class="sxs-lookup"><span data-stu-id="37f1b-103">IWordSink::PutAltWord method</span></span>

<span data-ttu-id="37f1b-104">Coloca una palabra alternativa y su posición en el objeto [**IWordSink**](iwordsink.md) .</span><span class="sxs-lookup"><span data-stu-id="37f1b-104">Puts an alternative word and its position in the [**IWordSink**](iwordsink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="37f1b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37f1b-105">Syntax</span></span>


```C++
HRESULT PutAltWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a><span data-ttu-id="37f1b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37f1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37f1b-107">*CWC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="37f1b-107">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37f1b-108">Número de caracteres de *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="37f1b-108">The number of characters in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="37f1b-109">*pwcInBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="37f1b-109">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37f1b-110">Un puntero a un búfer que contiene una forma alternativa de una palabra del texto de origen.</span><span class="sxs-lookup"><span data-stu-id="37f1b-110">A pointer to a buffer that contains an alternative form of a word from the source text.</span></span> <span data-ttu-id="37f1b-111">**PutAltWord** no modifica este parámetro.</span><span class="sxs-lookup"><span data-stu-id="37f1b-111">This parameter is not modified by **PutAltWord**.</span></span> <span data-ttu-id="37f1b-112">Puede pasar el parámetro *pTextSource* de [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) según corresponda.</span><span class="sxs-lookup"><span data-stu-id="37f1b-112">You can pass the *pTextSource* parameter from [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) as appropriate.</span></span>

</dd> <dt>

<span data-ttu-id="37f1b-113">*cwcSrcLen* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="37f1b-113">*cwcSrcLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37f1b-114">Número de caracteres del búfer de texto de origen (indicado por el parámetro *pTextSource* en [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) que corresponden a la palabra contenida en *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="37f1b-114">The number of characters in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) that correspond to the word contained in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="37f1b-115">*cwcSrcPos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="37f1b-115">*cwcSrcPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37f1b-116">Posición inicial de la palabra en *pwcInBuf* en el búfer de texto de origen (indicado por el parámetro *pTextSource* a [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span><span class="sxs-lookup"><span data-stu-id="37f1b-116">The starting position of the word in *pwcInBuf* in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37f1b-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37f1b-117">Return value</span></span>

<span data-ttu-id="37f1b-118">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="37f1b-118">This method can return one of these values.</span></span>



| <span data-ttu-id="37f1b-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="37f1b-119">Return code</span></span>                                                                                              | <span data-ttu-id="37f1b-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="37f1b-120">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="37f1b-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="37f1b-121"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="37f1b-122">La operación se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="37f1b-122">The operation was completed successfully.</span></span> <span data-ttu-id="37f1b-123">También indica que no queda más texto para procesarse.</span><span class="sxs-lookup"><span data-stu-id="37f1b-123">Also indicates that no more text remains to be processed.</span></span><br/>                                            |
| <dl> <span data-ttu-id="37f1b-124"><dt>**Idioma \_ de \_ \_ palabra S grande**</dt></span><span class="sxs-lookup"><span data-stu-id="37f1b-124"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="37f1b-125">El valor de *CWC* es mayor que el valor de *ulMaxTokenSize* que se especifica en [**IWordBreaker:: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span><span class="sxs-lookup"><span data-stu-id="37f1b-125">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IWordBreaker::Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="37f1b-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37f1b-126">Remarks</span></span>

<span data-ttu-id="37f1b-127">**PutAltWord** coloca una forma alternativa de una palabra en el [**IWordSink**](iwordsink.md).</span><span class="sxs-lookup"><span data-stu-id="37f1b-127">**PutAltWord** puts an alternative form of a word in the [**IWordSink**](iwordsink.md).</span></span> <span data-ttu-id="37f1b-128">La palabra se coloca en la misma posición que la palabra original en el origen del texto (*pTextSource* en [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span><span class="sxs-lookup"><span data-stu-id="37f1b-128">The word is put in the same position as the original word in the text source (*pTextSource* in [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span> <span data-ttu-id="37f1b-129">De forma predeterminada, **PutAltWord** finaliza las palabras con un tipo de interrupción **WORDREP \_ break \_ EOW** en el tipo enumerado [**\_ \_ tipo de interrupción WORDREP**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="37f1b-129">By default, **PutAltWord** terminates words with a **WORDREP\_BREAK\_EOW** break type from the [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) enumerated type.</span></span>

## <a name="requirements"></a><span data-ttu-id="37f1b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37f1b-130">Requirements</span></span>



| <span data-ttu-id="37f1b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="37f1b-131">Requirement</span></span> | <span data-ttu-id="37f1b-132">Value</span><span class="sxs-lookup"><span data-stu-id="37f1b-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="37f1b-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37f1b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="37f1b-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="37f1b-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="37f1b-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37f1b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="37f1b-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="37f1b-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="37f1b-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37f1b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="37f1b-138"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="37f1b-138"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37f1b-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="37f1b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37f1b-140">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="37f1b-140">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
