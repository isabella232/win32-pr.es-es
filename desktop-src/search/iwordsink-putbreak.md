---
description: Coloca un salto después de la palabra anterior.
ms.assetid: C8622067-D8CE-4099-8B9F-941720F4706B
title: IWordSink::P método utBreak (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutBreak
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: c6407f1307b4860960c5202af13de736c7921139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360185"
---
# <a name="iwordsinkputbreak-method"></a><span data-ttu-id="3594a-103">IWordSink::P método utBreak</span><span class="sxs-lookup"><span data-stu-id="3594a-103">IWordSink::PutBreak method</span></span>

<span data-ttu-id="3594a-104">Coloca un salto después de la palabra anterior.</span><span class="sxs-lookup"><span data-stu-id="3594a-104">Puts a break after the preceding word.</span></span>

## <a name="syntax"></a><span data-ttu-id="3594a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3594a-105">Syntax</span></span>


```C++
HRESULT PutBreak(
  [in] WORDREP_BREAK_TYPE breakType
);
```



## <a name="parameters"></a><span data-ttu-id="3594a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3594a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3594a-107">*breakType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3594a-107">*breakType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3594a-108">Un valor del [**\_ \_ tipo de interrupción WORDREP**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) que indica el tipo de interrupción que el WordSink inserta después de la palabra anterior.</span><span class="sxs-lookup"><span data-stu-id="3594a-108">A value from [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) that indicates the type of break that the WordSink inserts after the preceding word.</span></span> <span data-ttu-id="3594a-109">Cada salto ocupa una posición única en el índice.</span><span class="sxs-lookup"><span data-stu-id="3594a-109">Each break occupies a unique position in the index.</span></span> <span data-ttu-id="3594a-110">Por lo tanto, la inserción de saltos entre palabras cambia la distancia relativa entre palabras.</span><span class="sxs-lookup"><span data-stu-id="3594a-110">Therefore, inserting breaks between words changes the relative distance between words.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3594a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3594a-111">Return value</span></span>

<span data-ttu-id="3594a-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="3594a-112">This method can return one of these values.</span></span>



| <span data-ttu-id="3594a-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3594a-113">Return code</span></span>                                                                          | <span data-ttu-id="3594a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="3594a-114">Description</span></span>                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="3594a-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3594a-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3594a-116">La operación se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3594a-116">The operation was completed successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3594a-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3594a-117">Remarks</span></span>

<span data-ttu-id="3594a-118">Los métodos [**IWordSinkPutWord**](iwordsink-putword.md) y [**IWordSink::P utaltword**](iwordsink-putaltword.md) insertan automáticamente un salto de final de palabra (EOW, indicado por el \_ elemento WORDREP break \_ EOW del tipo de [**\_ interrupción \_ WORDREP**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) tipo enumerado) después de cada palabra.</span><span class="sxs-lookup"><span data-stu-id="3594a-118">The [**IWordSinkPutWord**](iwordsink-putword.md) and [**IWordSink::PutAltWord**](iwordsink-putaltword.md) methods automatically insert an end-of-word break (EOW, indicated by the WORDREP\_BREAK\_EOW element of the [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) enumerated type) after each word.</span></span> <span data-ttu-id="3594a-119">Llame al método **PutBreak** para insertar un tipo de interrupción que no sea el final de la palabra.</span><span class="sxs-lookup"><span data-stu-id="3594a-119">Call the **PutBreak** method to insert a break type other than end of word.</span></span> <span data-ttu-id="3594a-120">Este método no cambia el búfer de texto de origen (*pSourceText*) ni incrementa el recuento de caracteres (*CWC*).</span><span class="sxs-lookup"><span data-stu-id="3594a-120">This method does not change the source text buffer (*pSourceText*) or increment the character count (*cwc*).</span></span> <span data-ttu-id="3594a-121">Sin embargo, incrementa la posición actual en el índice y afecta a los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="3594a-121">However, it does increment the current position in the index and affects query results.</span></span>

## <a name="requirements"></a><span data-ttu-id="3594a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3594a-122">Requirements</span></span>



| <span data-ttu-id="3594a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3594a-123">Requirement</span></span> | <span data-ttu-id="3594a-124">Value</span><span class="sxs-lookup"><span data-stu-id="3594a-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3594a-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3594a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3594a-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3594a-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3594a-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3594a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3594a-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3594a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3594a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3594a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3594a-130"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="3594a-130"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3594a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="3594a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3594a-132">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="3594a-132">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
