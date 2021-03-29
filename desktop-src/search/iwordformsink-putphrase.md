---
description: Coloca una forma alternativa de una palabra en el objeto IWordFormSink.
ms.assetid: 4F6A3E88-A17C-4CA3-849D-FF0DC06D5DC3
title: IWordFormSink::P método utAltWord (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 43539bbf67e23bc37ca92f6a961b945ae581e746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808918"
---
# <a name="iwordformsinkputaltword-method"></a><span data-ttu-id="00959-103">IWordFormSink::P método utAltWord</span><span class="sxs-lookup"><span data-stu-id="00959-103">IWordFormSink::PutAltWord method</span></span>

<span data-ttu-id="00959-104">Coloca una forma alternativa de una palabra en el objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .</span><span class="sxs-lookup"><span data-stu-id="00959-104">Puts an alternative form of a word in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="00959-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00959-105">Syntax</span></span>


```C++
HRESULT PutAltWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a><span data-ttu-id="00959-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00959-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00959-107">*pwcInBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="00959-107">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00959-108">Un puntero a un búfer que contiene una forma alternativa de una palabra.</span><span class="sxs-lookup"><span data-stu-id="00959-108">A pointer to a buffer that contains an alternative form of a word.</span></span>

</dd> <dt>

<span data-ttu-id="00959-109">*CWC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="00959-109">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00959-110">Número de caracteres de *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="00959-110">The number of characters in *pwcInBuf*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00959-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00959-111">Return value</span></span>

<span data-ttu-id="00959-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="00959-112">This method can return one of these values.</span></span>



| <span data-ttu-id="00959-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="00959-113">Return code</span></span>                                                                                              | <span data-ttu-id="00959-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="00959-114">Description</span></span>                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="00959-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="00959-115"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="00959-116">La operación se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="00959-116">The operation was completed successfully.</span></span> <br/>                                                                                             |
| <dl> <span data-ttu-id="00959-117"><dt>**Idioma \_ de \_ \_ palabra S grande**</dt></span><span class="sxs-lookup"><span data-stu-id="00959-117"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="00959-118">El valor de *CWC* es mayor que el valor de *ulMaxTokenSize* que se especifica en [**IStemmer:: init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init).</span><span class="sxs-lookup"><span data-stu-id="00959-118">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IStemmer::Init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="00959-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00959-119">Remarks</span></span>

<span data-ttu-id="00959-120">Se llama a este método desde el método [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) de la implementación de [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) .</span><span class="sxs-lookup"><span data-stu-id="00959-120">This method is called from the [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) method of the [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) implementation.</span></span> <span data-ttu-id="00959-121">Todas las formas alternativas para una palabra, a excepción de la última, se colocan en el objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) mediante una llamada a **IWordFormSink::P utaltword**.</span><span class="sxs-lookup"><span data-stu-id="00959-121">All alternative forms for a word, except the last, are put in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object by calling **IWordFormSink::PutAltWord**.</span></span> <span data-ttu-id="00959-122">La forma alternativa final de una palabra, que siempre es el formato original de la palabra, se controla mediante una llamada a [**IWordFormSink::P utword**](iwordformsink-putword.md).</span><span class="sxs-lookup"><span data-stu-id="00959-122">The final alternative form of a word, which is always the original form of the word, is handled by calling [**IWordFormSink::PutWord**](iwordformsink-putword.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00959-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00959-123">Requirements</span></span>



| <span data-ttu-id="00959-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="00959-124">Requirement</span></span> | <span data-ttu-id="00959-125">Value</span><span class="sxs-lookup"><span data-stu-id="00959-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="00959-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00959-126">Minimum supported client</span></span><br/> | <span data-ttu-id="00959-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="00959-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="00959-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00959-128">Minimum supported server</span></span><br/> | <span data-ttu-id="00959-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="00959-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="00959-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00959-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="00959-131"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="00959-131"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00959-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="00959-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00959-133">**IWordFormSink**</span><span class="sxs-lookup"><span data-stu-id="00959-133">**IWordFormSink**</span></span>](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
