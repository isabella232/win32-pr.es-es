---
title: Otros atributos predefinidos (TsAttrid. h)
description: Los valores siguientes identifican los atributos varios obtenidos con el método ITfContext GetAppProperty. Se incluyen el formato de datos y el contenido de cada tipo de propiedad.
ms.assetid: 8536938b-98a1-415b-b5f2-45b90215c270
keywords:
- Otros atributos predefinidos plataforma de servicios de texto
topic_type:
- apiref
api_name:
- Other Predefined Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0d0a3ff72a5ea84a6b9e5b47106012a945dbf45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686142"
---
# <a name="other-predefined-attributes"></a><span data-ttu-id="f51d3-105">Otros atributos predefinidos</span><span class="sxs-lookup"><span data-stu-id="f51d3-105">Other Predefined Attributes</span></span>

<span data-ttu-id="f51d3-106">Los valores siguientes identifican los atributos varios obtenidos con el método [ITfContext:: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) .</span><span class="sxs-lookup"><span data-stu-id="f51d3-106">The following values identify miscellaneous attributes obtained with the [ITfContext::GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) method.</span></span> <span data-ttu-id="f51d3-107">Se incluyen el formato de datos y el contenido de cada tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="f51d3-107">The data format and contents of each property type are included.</span></span>

## <a name="properties"></a><span data-ttu-id="f51d3-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f51d3-108">Properties</span></span>



| <span data-ttu-id="f51d3-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f51d3-109">Property</span></span>                             | <span data-ttu-id="f51d3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f51d3-110">Description</span></span>                                                                       |
|--------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f51d3-111">**\_Aplicación TSATTRID**</span><span class="sxs-lookup"><span data-stu-id="f51d3-111">**TSATTRID\_App**</span></span>                    | <span data-ttu-id="f51d3-112">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f51d3-112">Not used.</span></span>                                                                         |
| <span data-ttu-id="f51d3-113">**IncorrectGrammar de la \_ aplicación TSATTRID \_**</span><span class="sxs-lookup"><span data-stu-id="f51d3-113">**TSATTRID\_App\_IncorrectGrammar**</span></span>  | <span data-ttu-id="f51d3-114">Contiene un valor distinto de cero si el texto contiene un error gramatical o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="f51d3-114">Contains a nonzero value if the text contains a grammar error or zero otherwise.</span></span>  |
| <span data-ttu-id="f51d3-115">**IncorrectSpelling de la \_ aplicación TSATTRID \_**</span><span class="sxs-lookup"><span data-stu-id="f51d3-115">**TSATTRID\_App\_IncorrectSpelling**</span></span> | <span data-ttu-id="f51d3-116">Contiene un valor distinto de cero si el texto contiene un error ortográfico o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="f51d3-116">Contains a nonzero value if the text contains a spelling error or zero otherwise.</span></span> |
| <span data-ttu-id="f51d3-117">**TSATTRID \_ otros**</span><span class="sxs-lookup"><span data-stu-id="f51d3-117">**TSATTRID\_OTHERS**</span></span>                 | <span data-ttu-id="f51d3-118">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f51d3-118">Not used.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="f51d3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f51d3-119">Requirements</span></span>



| <span data-ttu-id="f51d3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f51d3-120">Requirement</span></span> | <span data-ttu-id="f51d3-121">Value</span><span class="sxs-lookup"><span data-stu-id="f51d3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f51d3-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f51d3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f51d3-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f51d3-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f51d3-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f51d3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f51d3-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f51d3-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f51d3-126">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f51d3-126">Redistributable</span></span><br/>          | <span data-ttu-id="f51d3-127">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f51d3-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="f51d3-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f51d3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f51d3-129"><dt>TsAttrid. h</dt></span><span class="sxs-lookup"><span data-stu-id="f51d3-129"><dt>TsAttrid.h</dt></span></span> </dl> |



 

