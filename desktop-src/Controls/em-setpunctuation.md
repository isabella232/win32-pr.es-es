---
title: Mensaje EM_SETPUNCTUATION (RichEdit. h)
description: Establece los caracteres de puntuación para un control Rich Edit.
ms.assetid: c0c8ad14-63e2-4be8-8fc0-6b8ef9be4522
keywords:
- EM_SETPUNCTUATION controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710392cee7f7a1fb04fce59d6549134255499172
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150915"
---
# <a name="em_setpunctuation-message"></a><span data-ttu-id="06615-104">\_Mensaje SETPUNCTUATION em</span><span class="sxs-lookup"><span data-stu-id="06615-104">EM\_SETPUNCTUATION message</span></span>

<span data-ttu-id="06615-105">Establece los caracteres de puntuación para un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="06615-105">Sets the punctuation characters for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="06615-106">Este mensaje solo se admite en las versiones en idioma asiático de Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="06615-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="06615-107">No se admite en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="06615-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="06615-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06615-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06615-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06615-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06615-110">Especifica el tipo de puntuación, que puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="06615-110">Specifies the punctuation type, which can be one of the following values.</span></span>



| <span data-ttu-id="06615-111">Value</span><span class="sxs-lookup"><span data-stu-id="06615-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="06615-112">Significado</span><span class="sxs-lookup"><span data-stu-id="06615-112">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <span data-ttu-id="06615-113"><dt>**EQUIPOS \_ líderes**</dt></span><span class="sxs-lookup"><span data-stu-id="06615-113"><dt>**PC\_LEADING**</dt></span></span> </dl>       | <span data-ttu-id="06615-114">Caracteres de puntuación iniciales.</span><span class="sxs-lookup"><span data-stu-id="06615-114">Leading punctuation characters.</span></span><br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <span data-ttu-id="06615-115"><dt>**PC \_ después**</dt></span><span class="sxs-lookup"><span data-stu-id="06615-115"><dt>**PC\_FOLLOWING**</dt></span></span> </dl> | <span data-ttu-id="06615-116">Siguientes caracteres de puntuación.</span><span class="sxs-lookup"><span data-stu-id="06615-116">Following punctuation characters.</span></span><br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <span data-ttu-id="06615-117"><dt>**delimitador de PC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="06615-117"><dt>**PC\_DELIMITER**</dt></span></span> </dl> | <span data-ttu-id="06615-118">Delimitador.</span><span class="sxs-lookup"><span data-stu-id="06615-118">Delimiter.</span></span><br/>                        |
| <span id="PC_OVERFLOW_"></span><span id="pc_overflow_"></span><dl> <span data-ttu-id="06615-119"><dt>**PC \_ de DESBORDAMIENTO** de</dt></span><span class="sxs-lookup"><span data-stu-id="06615-119"><dt>**PC\_OVERFLOW** </dt></span></span> </dl> | <span data-ttu-id="06615-120">No se admite.</span><span class="sxs-lookup"><span data-stu-id="06615-120">Not supported.</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="06615-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06615-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06615-122">Puntero a una estructura de [**puntuación**](/windows/desktop/api/Richedit/ns-richedit-punctuation) que contiene los caracteres de puntuación.</span><span class="sxs-lookup"><span data-stu-id="06615-122">Pointer to a [**PUNCTUATION**](/windows/desktop/api/Richedit/ns-richedit-punctuation) structure that contains the punctuation characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06615-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06615-123">Return value</span></span>

<span data-ttu-id="06615-124">Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="06615-124">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="06615-125">Si se produce un error en la operación, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="06615-125">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="06615-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06615-126">Requirements</span></span>



| <span data-ttu-id="06615-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="06615-127">Requirement</span></span> | <span data-ttu-id="06615-128">Value</span><span class="sxs-lookup"><span data-stu-id="06615-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06615-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06615-129">Minimum supported client</span></span><br/> | <span data-ttu-id="06615-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="06615-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="06615-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06615-131">Minimum supported server</span></span><br/> | <span data-ttu-id="06615-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="06615-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06615-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06615-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="06615-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="06615-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06615-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="06615-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="06615-136">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="06615-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="06615-137">**\_GETPUNCTUATION em**</span><span class="sxs-lookup"><span data-stu-id="06615-137">**EM\_GETPUNCTUATION**</span></span>](em-getpunctuation.md)
</dt> <dt>

[<span data-ttu-id="06615-138">**PUNTUACIÓN**</span><span class="sxs-lookup"><span data-stu-id="06615-138">**PUNCTUATION**</span></span>](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





