---
title: Mensaje EM_EXLIMITTEXT (RichEdit. h)
description: Establece un límite superior para la cantidad de texto que el usuario puede escribir o pegar en un control Rich Edit.
ms.assetid: 66fcdbb9-99ac-4122-b89c-be4aef80fbae
keywords:
- EM_EXLIMITTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_EXLIMITTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c4ebb554e3aa3139a66ca63970356e1261a23f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491489"
---
# <a name="em_exlimittext-message"></a><span data-ttu-id="1ec17-104">\_Mensaje EXLIMITTEXT em</span><span class="sxs-lookup"><span data-stu-id="1ec17-104">EM\_EXLIMITTEXT message</span></span>

<span data-ttu-id="1ec17-105">Establece un límite superior para la cantidad de texto que el usuario puede escribir o pegar en un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="1ec17-105">Sets an upper limit to the amount of text the user can type or paste into a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ec17-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ec17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec17-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ec17-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec17-108">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1ec17-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1ec17-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ec17-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec17-110">Especifica la cantidad máxima de texto que se puede escribir.</span><span class="sxs-lookup"><span data-stu-id="1ec17-110">Specifies the maximum amount of text that can be entered.</span></span> <span data-ttu-id="1ec17-111">Si este parámetro es cero, se usa el valor máximo predeterminado, que es de 64 KB.</span><span class="sxs-lookup"><span data-stu-id="1ec17-111">If this parameter is zero, the default maximum is used, which is 64K characters.</span></span> <span data-ttu-id="1ec17-112">Un objeto COM cuenta como un solo carácter.</span><span class="sxs-lookup"><span data-stu-id="1ec17-112">A COM object counts as a single character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec17-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ec17-113">Return value</span></span>

<span data-ttu-id="1ec17-114">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1ec17-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ec17-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ec17-115">Remarks</span></span>

<span data-ttu-id="1ec17-116">El límite de texto establecido por el mensaje **em \_ EXLIMITTEXT** no limita la cantidad de texto que se puede transmitir en un control Rich Edit mediante el [**mensaje \_ secuencia em**](em-streamin.md) con *lParam* establecido en texto SF \_ .</span><span class="sxs-lookup"><span data-stu-id="1ec17-116">The text limit set by the **EM\_EXLIMITTEXT** message does not limit the amount of text that you can stream into a rich edit control using the [**EM\_STREAMIN**](em-streamin.md) message with *lParam* set to SF\_TEXT.</span></span> <span data-ttu-id="1ec17-117">Sin embargo, limita la cantidad de texto que se puede transmitir en un control Rich Edit mediante el mensaje **\_ secuencia em** con *lParam* establecido en el \_ formato RTF SF.</span><span class="sxs-lookup"><span data-stu-id="1ec17-117">However, it does limit the amount of text that you can stream into a rich edit control using the **EM\_STREAMIN** message with *lParam* set to SF\_RTF.</span></span>

<span data-ttu-id="1ec17-118">Antes de que se llame a **em \_ EXLIMITTEXT** , el límite predeterminado para la cantidad de texto que un usuario puede escribir es de 32.767 caracteres.</span><span class="sxs-lookup"><span data-stu-id="1ec17-118">Before **EM\_EXLIMITTEXT** is called, the default limit to the amount of text a user can enter is 32,767 characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ec17-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ec17-119">Requirements</span></span>



| <span data-ttu-id="1ec17-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ec17-120">Requirement</span></span> | <span data-ttu-id="1ec17-121">Value</span><span class="sxs-lookup"><span data-stu-id="1ec17-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec17-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ec17-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1ec17-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1ec17-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ec17-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ec17-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1ec17-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ec17-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ec17-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ec17-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ec17-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ec17-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ec17-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ec17-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec17-129">**\_secuencia em**</span><span class="sxs-lookup"><span data-stu-id="1ec17-129">**EM\_STREAMIN**</span></span>](em-streamin.md)
</dt> </dl>

 

 





