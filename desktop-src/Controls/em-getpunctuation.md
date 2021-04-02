---
title: Mensaje EM_GETPUNCTUATION (RichEdit. h)
description: Obtiene los caracteres de puntuación actuales para el control Rich Edit.
ms.assetid: 1c04967b-d75e-4f54-b35b-cd50bac9cdfa
keywords:
- EM_GETPUNCTUATION controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158c26deca3328d9cdbed7ffe7cf885b0582d1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150825"
---
# <a name="em_getpunctuation-message"></a><span data-ttu-id="d5ea8-104">\_Mensaje GETPUNCTUATION em</span><span class="sxs-lookup"><span data-stu-id="d5ea8-104">EM\_GETPUNCTUATION message</span></span>

<span data-ttu-id="d5ea8-105">Obtiene los caracteres de puntuación actuales para el control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d5ea8-105">Gets the current punctuation characters for the rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="d5ea8-106">Este mensaje solo se admite en las versiones en idioma asiático de Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="d5ea8-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="d5ea8-107">No se admite en las versiones posteriores de Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d5ea8-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="d5ea8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5ea8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5ea8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5ea8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5ea8-110">El tipo de puntuación puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d5ea8-110">The punctuation type can be one of the following values.</span></span>



| <span data-ttu-id="d5ea8-111">Value</span><span class="sxs-lookup"><span data-stu-id="d5ea8-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="d5ea8-112">Significado</span><span class="sxs-lookup"><span data-stu-id="d5ea8-112">Meaning</span></span>                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <span data-ttu-id="d5ea8-113"><dt>**EQUIPOS \_ líderes**</dt></span><span class="sxs-lookup"><span data-stu-id="d5ea8-113"><dt>**PC\_LEADING**</dt></span></span> </dl>       | <span data-ttu-id="d5ea8-114">Caracteres de puntuación iniciales</span><span class="sxs-lookup"><span data-stu-id="d5ea8-114">Leading punctuation characters</span></span><br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <span data-ttu-id="d5ea8-115"><dt>**PC \_ después**</dt></span><span class="sxs-lookup"><span data-stu-id="d5ea8-115"><dt>**PC\_FOLLOWING**</dt></span></span> </dl> | <span data-ttu-id="d5ea8-116">Caracteres de puntuación siguientes</span><span class="sxs-lookup"><span data-stu-id="d5ea8-116">Following punctuation characters</span></span><br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <span data-ttu-id="d5ea8-117"><dt>**delimitador de PC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5ea8-117"><dt>**PC\_DELIMITER**</dt></span></span> </dl> | <span data-ttu-id="d5ea8-118">Delimitador</span><span class="sxs-lookup"><span data-stu-id="d5ea8-118">Delimiter</span></span><br/>                        |
| <span id="PC_OVERFLOW"></span><span id="pc_overflow"></span><dl> <span data-ttu-id="d5ea8-119"><dt>**desbordamiento de equipo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5ea8-119"><dt>**PC\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="d5ea8-120">No compatible</span><span class="sxs-lookup"><span data-stu-id="d5ea8-120">Not supported</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="d5ea8-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5ea8-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5ea8-122">Puntero a una estructura de [**puntuación**](/windows/desktop/api/Richedit/ns-richedit-punctuation) que recibe los caracteres de puntuación.</span><span class="sxs-lookup"><span data-stu-id="d5ea8-122">Pointer to a [**PUNCTUATION**](/windows/desktop/api/Richedit/ns-richedit-punctuation) structure that receives the punctuation characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5ea8-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5ea8-123">Return value</span></span>

<span data-ttu-id="d5ea8-124">Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="d5ea8-124">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d5ea8-125">Si se produce un error en la operación, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="d5ea8-125">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5ea8-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5ea8-126">Requirements</span></span>



| <span data-ttu-id="d5ea8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5ea8-127">Requirement</span></span> | <span data-ttu-id="d5ea8-128">Value</span><span class="sxs-lookup"><span data-stu-id="d5ea8-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5ea8-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5ea8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d5ea8-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d5ea8-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d5ea8-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5ea8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d5ea8-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5ea8-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5ea8-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5ea8-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5ea8-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5ea8-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5ea8-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5ea8-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5ea8-136">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d5ea8-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d5ea8-137">**\_SETPUNCTUATION em**</span><span class="sxs-lookup"><span data-stu-id="d5ea8-137">**EM\_SETPUNCTUATION**</span></span>](em-setpunctuation.md)
</dt> <dt>

[<span data-ttu-id="d5ea8-138">**PUNTUACIÓN**</span><span class="sxs-lookup"><span data-stu-id="d5ea8-138">**PUNCTUATION**</span></span>](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





