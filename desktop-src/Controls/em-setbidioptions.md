---
title: Mensaje EM_SETBIDIOPTIONS (RichEdit. h)
description: El \_ mensaje SETBIDIOPTIONS em establece el estado actual de las opciones bidireccionales en el control Rich Edit.
ms.assetid: b518e423-317a-4654-9d9f-c501028e2a0a
keywords:
- EM_SETBIDIOPTIONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84dc4b92f7a989ab5ef283b36708094a143475de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150923"
---
# <a name="em_setbidioptions-message"></a><span data-ttu-id="3e021-104">\_Mensaje SETBIDIOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="3e021-104">EM\_SETBIDIOPTIONS message</span></span>

<span data-ttu-id="3e021-105">El **mensaje \_ SETBIDIOPTIONS em** establece el estado actual de las opciones bidireccionales en el control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="3e021-105">The **EM\_SETBIDIOPTIONS** message sets the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3e021-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e021-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e021-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3e021-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e021-108">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3e021-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3e021-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e021-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e021-110">Puntero a una estructura [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) que indica cómo establecer el estado de las opciones bidireccionales en el control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="3e021-110">Pointer to a [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) structure that indicates how to set the state of the bidirectional options in the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e021-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e021-111">Return value</span></span>

<span data-ttu-id="3e021-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3e021-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e021-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e021-113">Remarks</span></span>

<span data-ttu-id="3e021-114">El control Rich Edit debe estar en modo de texto sin formato o **em \_ SETBIDIOPTIONS** no hará nada.</span><span class="sxs-lookup"><span data-stu-id="3e021-114">The rich edit control must be in plain text mode or **EM\_SETBIDIOPTIONS** will not do anything.</span></span>

<span data-ttu-id="3e021-115">En los controles de texto sin formato, **em \_ SETBIDIOPTIONS** determina automáticamente la dirección del párrafo y/o la alineación en función de las reglas de contexto.</span><span class="sxs-lookup"><span data-stu-id="3e021-115">In plain text controls, **EM\_SETBIDIOPTIONS** automatically determines the paragraph direction and/or alignment based on the context rules.</span></span> <span data-ttu-id="3e021-116">Estas reglas determinan que la dirección y/o la alineación se derivan del primer carácter fuerte del control.</span><span class="sxs-lookup"><span data-stu-id="3e021-116">These rules state that the direction and/or alignment is derived from the first strong character in the control.</span></span> <span data-ttu-id="3e021-117">Un carácter seguro es aquél del que se puede determinar la dirección del texto (vea la versión 2,0 del estándar Unicode).</span><span class="sxs-lookup"><span data-stu-id="3e021-117">A strong character is one from which text direction can be determined (see Unicode Standard version 2.0).</span></span> <span data-ttu-id="3e021-118">La dirección del párrafo y/o la alineación se aplican al formato predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3e021-118">The paragraph direction and/or alignment is applied to the default format.</span></span>

<span data-ttu-id="3e021-119">**Em \_ SETBIDIOPTIONS** solo cambia el formato de párrafo predeterminado a RTL (de derecha a izquierda) si encuentra un carácter RTL,</span><span class="sxs-lookup"><span data-stu-id="3e021-119">**EM\_SETBIDIOPTIONS** only switches the default paragraph format to RTL (right to left) if it finds an RTL character,</span></span>

## <a name="requirements"></a><span data-ttu-id="3e021-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e021-120">Requirements</span></span>



| <span data-ttu-id="3e021-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e021-121">Requirement</span></span> | <span data-ttu-id="3e021-122">Value</span><span class="sxs-lookup"><span data-stu-id="3e021-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e021-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e021-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3e021-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3e021-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3e021-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e021-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3e021-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e021-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3e021-127">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="3e021-127">Redistributable</span></span><br/>          | <span data-ttu-id="3e021-128">Edición enriquecida 3,0</span><span class="sxs-lookup"><span data-stu-id="3e021-128">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="3e021-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e021-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e021-130"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e021-130"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e021-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e021-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="3e021-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="3e021-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3e021-133">**BIDIOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="3e021-133">**BIDIOPTIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[<span data-ttu-id="3e021-134">**\_GETBIDIOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="3e021-134">**EM\_GETBIDIOPTIONS**</span></span>](em-getbidioptions.md)
</dt> </dl>

 

 





