---
description: Coloca el formulario de Word original en el objeto IWordFormSink.
ms.assetid: 333A3109-6C0A-42AE-9E10-87F53C7F737C
title: IWordFormSink::P método utWord (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 438cb41e50f264bd373ae2ef8e84598b651b0352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696279"
---
# <a name="iwordformsinkputword-method"></a><span data-ttu-id="505bf-103">IWordFormSink::P método utWord</span><span class="sxs-lookup"><span data-stu-id="505bf-103">IWordFormSink::PutWord method</span></span>

<span data-ttu-id="505bf-104">Coloca el formulario de Word original en el objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .</span><span class="sxs-lookup"><span data-stu-id="505bf-104">Puts the original word form in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="505bf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="505bf-105">Syntax</span></span>


```C++
HRESULT PutWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a><span data-ttu-id="505bf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="505bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="505bf-107">*pwcInBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="505bf-107">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="505bf-108">Puntero a un búfer que contiene la forma alternativa final de una palabra, que siempre es la palabra original.</span><span class="sxs-lookup"><span data-stu-id="505bf-108">A pointer to a buffer that contains the final alternative form of a word, which is always the original word.</span></span>

</dd> <dt>

<span data-ttu-id="505bf-109">*CWC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="505bf-109">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="505bf-110">Número de caracteres de *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="505bf-110">The number of characters in *pwcInBuf*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="505bf-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="505bf-111">Return value</span></span>

<span data-ttu-id="505bf-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="505bf-112">This method can return one of these values.</span></span>



| <span data-ttu-id="505bf-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="505bf-113">Return code</span></span>                                                                          | <span data-ttu-id="505bf-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="505bf-114">Description</span></span>                                           |
|--------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="505bf-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="505bf-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="505bf-116">La operación se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="505bf-116">The operation was completed successfully.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="505bf-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="505bf-117">Remarks</span></span>

<span data-ttu-id="505bf-118">Se llama a **PutWord** desde el método [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) de la implementación de [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) .</span><span class="sxs-lookup"><span data-stu-id="505bf-118">**PutWord** is called from the [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) method of the [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) implementation.</span></span> <span data-ttu-id="505bf-119">Este método controla el formato original de una palabra y se llama último.</span><span class="sxs-lookup"><span data-stu-id="505bf-119">This method handles the original form of a word and is called last.</span></span> <span data-ttu-id="505bf-120">Todas las formas alternativas anteriores de una palabra se colocan en el objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) mediante una llamada a [**IWordFormSink::P utaltword**](iwordformsink-putphrase.md).</span><span class="sxs-lookup"><span data-stu-id="505bf-120">All preceding alternative forms for a word are put in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object by calling [**IWordFormSink::PutAltWord**](iwordformsink-putphrase.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="505bf-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="505bf-121">Requirements</span></span>



| <span data-ttu-id="505bf-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="505bf-122">Requirement</span></span> | <span data-ttu-id="505bf-123">Value</span><span class="sxs-lookup"><span data-stu-id="505bf-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="505bf-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="505bf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="505bf-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="505bf-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="505bf-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="505bf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="505bf-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="505bf-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="505bf-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="505bf-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="505bf-129"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="505bf-129"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="505bf-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="505bf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="505bf-131">**IWordFormSink**</span><span class="sxs-lookup"><span data-stu-id="505bf-131">**IWordFormSink**</span></span>](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
