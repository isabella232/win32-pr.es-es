---
description: Describe el tipo de datos del valor asociado a una etiqueta.
ms.assetid: 009ad522-35da-4053-a7f6-61d7d240b98c
title: Tipos de etiquetas
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ab53b9c3b85263ddcdbe80e3979d576685bd73
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274873"
---
# <a name="tag-types"></a><span data-ttu-id="ba430-103">Tipos de etiquetas</span><span class="sxs-lookup"><span data-stu-id="ba430-103">TAG Types</span></span>

<span data-ttu-id="ba430-104">Describe el tipo de datos del valor asociado a una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="ba430-104">Describes the data type of the value associated with a TAG.</span></span>



| <span data-ttu-id="ba430-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="ba430-105">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="ba430-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba430-106">Description</span></span>                                           |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| <span id="TAG_TYPE_NULL"></span><span id="tag_type_null"></span><dl> <span data-ttu-id="ba430-107"><dt>**Etiqueta \_ de TIPO \_ null**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="ba430-107"><dt>**TAG\_TYPE\_NULL**</dt> <dt>0x1000</dt></span></span> </dl>                | <span data-ttu-id="ba430-108">No hay ningún valor asociado a la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="ba430-108">There is no value associated with the TAG.</span></span><br/> |
| <span id="TAG_TYPE_BYTE"></span><span id="tag_type_byte"></span><dl> <span data-ttu-id="ba430-109"><dt>**Etiqueta \_ de TIPO \_ byte**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="ba430-109"><dt>**TAG\_TYPE\_BYTE**</dt> <dt>0x2000</dt></span></span> </dl>                | <span data-ttu-id="ba430-110">Valor de **byte** .</span><span class="sxs-lookup"><span data-stu-id="ba430-110">A **BYTE** value.</span></span><br/>                          |
| <span id="TAG_TYPE_WORD"></span><span id="tag_type_word"></span><dl> <span data-ttu-id="ba430-111"><dt>**Etiqueta \_ de ESCRIBIR \_ palabra**</dt> <dt>0x3000</dt></span><span class="sxs-lookup"><span data-stu-id="ba430-111"><dt>**TAG\_TYPE\_WORD**</dt> <dt>0x3000</dt></span></span> </dl>                | <span data-ttu-id="ba430-112">Valor de **palabra** .</span><span class="sxs-lookup"><span data-stu-id="ba430-112">A **WORD** value.</span></span><br/>                          |
| <span id="TAG_TYPE_DWORD"></span><span id="tag_type_dword"></span><dl> <span data-ttu-id="ba430-113"><dt>**Etiqueta \_ de Escriba \_ DWORD**</dt> <dt>0x4000</dt></span><span class="sxs-lookup"><span data-stu-id="ba430-113"><dt>**TAG\_TYPE\_DWORD**</dt> <dt>0x4000</dt></span></span> </dl>             | <span data-ttu-id="ba430-114">Valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="ba430-114">A **DWORD** value.</span></span><br/>                         |
| <span id="TAG_TYPE_QWORD"></span><span id="tag_type_qword"></span><dl> <span data-ttu-id="ba430-115"><dt>**Etiqueta \_ de Escriba \_ QWord**</dt> <dt>0x5000</dt></span><span class="sxs-lookup"><span data-stu-id="ba430-115"><dt>**TAG\_TYPE\_QWORD**</dt> <dt>0x5000</dt></span></span> </dl>             | <span data-ttu-id="ba430-116">Valor de **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="ba430-116">A **ULONGLONG** value.</span></span><br/>                     |
| <span id="TAG_TYPE_STRINGREF"></span><span id="tag_type_stringref"></span><dl> <span data-ttu-id="ba430-117"><dt>**Etiqueta \_ de Escriba \_ STRINGREF**</dt> <dt>0x6000</dt></span><span class="sxs-lookup"><span data-stu-id="ba430-117"><dt>**TAG\_TYPE\_STRINGREF**</dt> <dt>0x6000</dt></span></span> </dl> | <span data-ttu-id="ba430-118">Valor de cadena con tokens.</span><span class="sxs-lookup"><span data-stu-id="ba430-118">A tokenized string value.</span></span><br/>                  |
| <span id="TAG_TYPE_LIST"></span><span id="tag_type_list"></span><dl> <span data-ttu-id="ba430-119"><dt>**Etiqueta \_ de TYPE \_ List**</dt> <dt>0x7000</dt></span><span class="sxs-lookup"><span data-stu-id="ba430-119"><dt>**TAG\_TYPE\_LIST**</dt> <dt>0x7000</dt></span></span> </dl>                | <span data-ttu-id="ba430-120">Una lista de valores de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="ba430-120">A list of TAG values.</span></span><br/>                      |
| <span id="TAG_TYPE_STRING"></span><span id="tag_type_string"></span><dl> <span data-ttu-id="ba430-121"><dt>**Etiqueta \_ de TIPO \_ String**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="ba430-121"><dt>**TAG\_TYPE\_STRING**</dt> <dt>0x8000</dt></span></span> </dl>          | <span data-ttu-id="ba430-122">Valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="ba430-122">A string value.</span></span><br/>                            |
| <span id="TAG_TYPE_BINARY"></span><span id="tag_type_binary"></span><dl> <span data-ttu-id="ba430-123"><dt>**Etiqueta \_ de TIPO \_ binario**</dt> <dt>0x9000</dt></span><span class="sxs-lookup"><span data-stu-id="ba430-123"><dt>**TAG\_TYPE\_BINARY**</dt> <dt>0x9000</dt></span></span> </dl>          | <span data-ttu-id="ba430-124">Valor binario.</span><span class="sxs-lookup"><span data-stu-id="ba430-124">A binary value.</span></span><br/>                            |



## <a name="requirements"></a><span data-ttu-id="ba430-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba430-125">Requirements</span></span>



| <span data-ttu-id="ba430-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba430-126">Requirement</span></span> | <span data-ttu-id="ba430-127">Value</span><span class="sxs-lookup"><span data-stu-id="ba430-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ba430-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba430-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ba430-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ba430-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ba430-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba430-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ba430-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ba430-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ba430-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba430-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba430-133">**ETIQUETA**</span><span class="sxs-lookup"><span data-stu-id="ba430-133">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="ba430-134">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="ba430-134">**TAGID**</span></span>](tagid.md)
</dt> <dt>

[<span data-ttu-id="ba430-135">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="ba430-135">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




