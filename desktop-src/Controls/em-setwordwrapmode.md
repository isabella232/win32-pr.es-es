---
title: Mensaje EM_SETWORDWRAPMODE (RichEdit. h)
description: Establece las opciones de ajuste de palabras y de separación de palabras para un control Rich Edit.
ms.assetid: 43703ac8-6ae5-470b-9156-e60330ef97c4
keywords:
- EM_SETWORDWRAPMODE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1dc6f064f52bf2a5f58c71db099f38b9350e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079485"
---
# <a name="em_setwordwrapmode-message"></a><span data-ttu-id="02bc8-104">\_Mensaje SETWORDWRAPMODE em</span><span class="sxs-lookup"><span data-stu-id="02bc8-104">EM\_SETWORDWRAPMODE message</span></span>

<span data-ttu-id="02bc8-105">Establece las opciones de ajuste de palabras y de separación de palabras para un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="02bc8-105">Sets the word-wrapping and word-breaking options for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="02bc8-106">Este mensaje solo se admite en las versiones en idioma asiático de Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="02bc8-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="02bc8-107">No se admite en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="02bc8-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="02bc8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02bc8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02bc8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="02bc8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02bc8-110">Especifica uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="02bc8-110">Specifies one or more of the following values.</span></span>



| <span data-ttu-id="02bc8-111">Value</span><span class="sxs-lookup"><span data-stu-id="02bc8-111">Value</span></span>                                                                                                                                                         | <span data-ttu-id="02bc8-112">Significado</span><span class="sxs-lookup"><span data-stu-id="02bc8-112">Meaning</span></span>                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="WBF_WORDWRAP"></span><span id="wbf_wordwrap"></span><dl> <span data-ttu-id="02bc8-113"><dt>**WBF \_ WORDWRAP**</dt></span><span class="sxs-lookup"><span data-stu-id="02bc8-113"><dt>**WBF\_WORDWRAP**</dt></span></span> </dl>    | <span data-ttu-id="02bc8-114">Habilita operaciones de ajuste de palabras específicas de Asia, como Kinsoku en japonés.</span><span class="sxs-lookup"><span data-stu-id="02bc8-114">Enables Asian-specific word wrap operations, such as kinsoku in Japanese.</span></span> <br/>                                 |
| <span id="WBF_WORDBREAK"></span><span id="wbf_wordbreak"></span><dl> <span data-ttu-id="02bc8-115"><dt>**WBF \_ WORDBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="02bc8-115"><dt>**WBF\_WORDBREAK**</dt></span></span> </dl> | <span data-ttu-id="02bc8-116">Habilita las operaciones de división de palabras en inglés en japonés y chino.</span><span class="sxs-lookup"><span data-stu-id="02bc8-116">Enables English word-breaking operations in Japanese and Chinese.</span></span> <span data-ttu-id="02bc8-117">Habilita la operación de separación de palabras de Hangeul.</span><span class="sxs-lookup"><span data-stu-id="02bc8-117">Enables Hangeul word-breaking operation.</span></span><br/> |
| <span id="WBF_OVERFLOW"></span><span id="wbf_overflow"></span><dl> <span data-ttu-id="02bc8-118"><dt>**desbordamiento de WBF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="02bc8-118"><dt>**WBF\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="02bc8-119">Reconoce la puntuación de desbordamiento.</span><span class="sxs-lookup"><span data-stu-id="02bc8-119">Recognizes overflow punctuation.</span></span> <span data-ttu-id="02bc8-120">(Actualmente no se admite).</span><span class="sxs-lookup"><span data-stu-id="02bc8-120">(Not currently supported.)</span></span><br/>                                                |
| <span id="WBF_LEVEL1"></span><span id="wbf_level1"></span><dl> <span data-ttu-id="02bc8-121"><dt>**WBF \_ Level1**</dt></span><span class="sxs-lookup"><span data-stu-id="02bc8-121"><dt>**WBF\_LEVEL1**</dt></span></span> </dl>          | <span data-ttu-id="02bc8-122">Establece la tabla de puntuación de nivel 1 como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="02bc8-122">Sets the Level 1 punctuation table as the default.</span></span><br/>                                                         |
| <span id="WBF_LEVEL2"></span><span id="wbf_level2"></span><dl> <span data-ttu-id="02bc8-123"><dt>**WBF \_ LEVEL2**</dt></span><span class="sxs-lookup"><span data-stu-id="02bc8-123"><dt>**WBF\_LEVEL2**</dt></span></span> </dl>          | <span data-ttu-id="02bc8-124">Establece la tabla de puntuación de nivel 2 como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="02bc8-124">Sets the Level 2 punctuation table as the default.</span></span><br/>                                                         |
| <span id="WBF_CUSTOM"></span><span id="wbf_custom"></span><dl> <span data-ttu-id="02bc8-125"><dt>**WBF \_ personalizado**</dt></span><span class="sxs-lookup"><span data-stu-id="02bc8-125"><dt>**WBF\_CUSTOM**</dt></span></span> </dl>          | <span data-ttu-id="02bc8-126">Establece la tabla de puntuación definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="02bc8-126">Sets the application-defined punctuation table.</span></span><br/>                                                            |



 

</dd> <dt>

<span data-ttu-id="02bc8-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="02bc8-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02bc8-128">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="02bc8-128">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02bc8-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02bc8-129">Return value</span></span>

<span data-ttu-id="02bc8-130">Este mensaje devuelve las opciones actuales de ajuste de palabras y de separación de palabras.</span><span class="sxs-lookup"><span data-stu-id="02bc8-130">This message returns the current word-wrapping and word-breaking options.</span></span>

## <a name="remarks"></a><span data-ttu-id="02bc8-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02bc8-131">Remarks</span></span>

<span data-ttu-id="02bc8-132">Este mensaje no se debe enviar mediante el procedimiento de separación de palabras definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="02bc8-132">This message must not be sent by the application defined word breaking procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="02bc8-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02bc8-133">Requirements</span></span>



| <span data-ttu-id="02bc8-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="02bc8-134">Requirement</span></span> | <span data-ttu-id="02bc8-135">Value</span><span class="sxs-lookup"><span data-stu-id="02bc8-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02bc8-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02bc8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="02bc8-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="02bc8-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="02bc8-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02bc8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="02bc8-139">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="02bc8-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="02bc8-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02bc8-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="02bc8-141"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="02bc8-141"><dt>Richedit.h</dt></span></span> </dl> |



 

 





