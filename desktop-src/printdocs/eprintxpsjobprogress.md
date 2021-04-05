---
description: Especifica lo que está haciendo el administrador de trabajos de impresión actualmente mientras procesa un trabajo de impresión XPS.
ms.assetid: 4fa5b749-e4f9-4f08-97b5-e58f82d0b485
title: Enumeración EPrintXPSJobProgress (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobProgress
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2a09b55ed72a6276a1a9d224cc08e03546f887d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546083"
---
# <a name="eprintxpsjobprogress-enumeration"></a><span data-ttu-id="a89d7-103">Enumeración EPrintXPSJobProgress</span><span class="sxs-lookup"><span data-stu-id="a89d7-103">EPrintXPSJobProgress enumeration</span></span>

<span data-ttu-id="a89d7-104">Especifica lo que está haciendo el administrador de trabajos de impresión actualmente mientras procesa un trabajo de impresión XPS.</span><span class="sxs-lookup"><span data-stu-id="a89d7-104">Specifies what the spooler is currently doing as it processes an XPS print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="a89d7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a89d7-105">Syntax</span></span>


```C++
typedef enum tagEPrintXPSJobProgress { 
  kAddingDocumentSequence,
  kDocumentSequenceAdded,
  kAddingFixedDocument,
  kFixedDocumentAdded,
  kAddingFixedPage,
  kFixedPageAdded,
  kResourceAdded,
  kFontAdded,
  kImageAdded,
  kXpsDocumentCommitted
} EPrintXPSJobProgress;
```



## <a name="constants"></a><span data-ttu-id="a89d7-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="a89d7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a89d7-107"><span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**kAddingDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="a89d7-107"><span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**kAddingDocumentSequence**</span></span>
</dt> <dd>

<span data-ttu-id="a89d7-108">Se va a agregar una secuencia de documento al trabajo XPS.</span><span class="sxs-lookup"><span data-stu-id="a89d7-108">A document sequence is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="a89d7-109"><span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**kDocumentSequenceAdded**</span><span class="sxs-lookup"><span data-stu-id="a89d7-109"><span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**kDocumentSequenceAdded**</span></span>
</dt> <dd>

<span data-ttu-id="a89d7-110">Se ha agregado una secuencia de documento al trabajo XPS.</span><span class="sxs-lookup"><span data-stu-id="a89d7-110">A document sequence has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="a89d7-111"><span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**kAddingFixedDocument**</span><span class="sxs-lookup"><span data-stu-id="a89d7-111"><span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**kAddingFixedDocument**</span></span>
</dt> <dd>

<span data-ttu-id="a89d7-112">Un documento fijo está a punto de agregarse al trabajo XPS.</span><span class="sxs-lookup"><span data-stu-id="a89d7-112">A fixed document is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="a89d7-113"><span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**kFixedDocumentAdded**</span><span class="sxs-lookup"><span data-stu-id="a89d7-113"><span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**kFixedDocumentAdded**</span></span>
</dt> <dd>

<span data-ttu-id="a89d7-114">Se ha agregado un documento fijo al trabajo XPS.</span><span class="sxs-lookup"><span data-stu-id="a89d7-114">A fixed document has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="a89d7-115"><span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**kAddingFixedPage**</span><span class="sxs-lookup"><span data-stu-id="a89d7-115"><span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**kAddingFixedPage**</span></span>
</dt> <dd>

<span data-ttu-id="a89d7-116">Se va a agregar una página al trabajo XPS.</span><span class="sxs-lookup"><span data-stu-id="a89d7-116">A page is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="a89d7-117"><span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**kFixedPageAdded**</span><span class="sxs-lookup"><span data-stu-id="a89d7-117"><span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**kFixedPageAdded**</span></span>
</dt> <dd>

<span data-ttu-id="a89d7-118">Se ha agregado una página al trabajo XPS.</span><span class="sxs-lookup"><span data-stu-id="a89d7-118">A page has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="a89d7-119"><span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**kResourceAdded**</span><span class="sxs-lookup"><span data-stu-id="a89d7-119"><span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**kResourceAdded**</span></span>
</dt> <dd>

<span data-ttu-id="a89d7-120">Se ha agregado un recurso al trabajo XPS.</span><span class="sxs-lookup"><span data-stu-id="a89d7-120">A resource had been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="a89d7-121"><span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**kFontAdded**</span><span class="sxs-lookup"><span data-stu-id="a89d7-121"><span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**kFontAdded**</span></span>
</dt> <dd>

<span data-ttu-id="a89d7-122">Se ha agregado una fuente al trabajo XPS.</span><span class="sxs-lookup"><span data-stu-id="a89d7-122">A font has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="a89d7-123"><span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**kImageAdded**</span><span class="sxs-lookup"><span data-stu-id="a89d7-123"><span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**kImageAdded**</span></span>
</dt> <dd>

<span data-ttu-id="a89d7-124">Se ha agregado una imagen al trabajo XPS.</span><span class="sxs-lookup"><span data-stu-id="a89d7-124">An image has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="a89d7-125"><span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**kXpsDocumentCommitted**</span><span class="sxs-lookup"><span data-stu-id="a89d7-125"><span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**kXpsDocumentCommitted**</span></span>
</dt> <dd>

<span data-ttu-id="a89d7-126">Se han confirmado los datos para el trabajo XPS.</span><span class="sxs-lookup"><span data-stu-id="a89d7-126">The data for the XPS job has been committed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a89d7-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a89d7-127">Remarks</span></span>

<span data-ttu-id="a89d7-128">Esta enumeración se usa principalmente como parámetro para la función [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) .</span><span class="sxs-lookup"><span data-stu-id="a89d7-128">This enumeration is primarily used as a parameter for the [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) function.</span></span>

<span data-ttu-id="a89d7-129">Estos valores pueden hacer referencia a la fase de puesta en cola o a la fase de representación de un trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="a89d7-129">These values can refer to either the spooling or the rendering phase of a print job.</span></span>

## <a name="requirements"></a><span data-ttu-id="a89d7-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a89d7-130">Requirements</span></span>



| <span data-ttu-id="a89d7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a89d7-131">Requirement</span></span> | <span data-ttu-id="a89d7-132">Value</span><span class="sxs-lookup"><span data-stu-id="a89d7-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a89d7-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a89d7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a89d7-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a89d7-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="a89d7-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a89d7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a89d7-136">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a89d7-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a89d7-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a89d7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="a89d7-138"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a89d7-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




