---
title: Mensaje EM_SHOWSCROLLBAR (RichEdit. h)
description: Muestra u oculta una de las barras de desplazamiento en la ventana host de un control Rich Edit.
ms.assetid: 0a6ec010-4870-4faf-9dc2-1da961dc8194
keywords:
- EM_SHOWSCROLLBAR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SHOWSCROLLBAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb569b194be3d744db67f98b71a595ba18a2d3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996289"
---
# <a name="em_showscrollbar-message"></a><span data-ttu-id="bfe41-104">\_Mensaje SHOWSCROLLBAR em</span><span class="sxs-lookup"><span data-stu-id="bfe41-104">EM\_SHOWSCROLLBAR message</span></span>

<span data-ttu-id="bfe41-105">Muestra u oculta una de las barras de desplazamiento en la ventana host de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="bfe41-105">Shows or hides one of the scroll bars in the host window of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bfe41-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfe41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfe41-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bfe41-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfe41-108">Identifica la barra de desplazamiento que se va a mostrar: horizontal o vertical.</span><span class="sxs-lookup"><span data-stu-id="bfe41-108">Identifies which scroll bar to display: horizontal or vertical.</span></span> <span data-ttu-id="bfe41-109">Este parámetro debe ser **SB \_ Vert** o **SB \_ horizontal**.</span><span class="sxs-lookup"><span data-stu-id="bfe41-109">This parameter must be **SB\_VERT** or **SB\_HORZ**.</span></span>

</dd> <dt>

<span data-ttu-id="bfe41-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bfe41-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfe41-111">Especifica si se muestra o se oculta la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="bfe41-111">Specifies whether to show the scroll bar or hide it.</span></span> <span data-ttu-id="bfe41-112">Especifique **true** para mostrar la barra de desplazamiento y **false** para ocultarla.</span><span class="sxs-lookup"><span data-stu-id="bfe41-112">Specify **TRUE** to show the scroll bar and **FALSE** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfe41-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfe41-113">Return value</span></span>

<span data-ttu-id="bfe41-114">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="bfe41-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfe41-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfe41-115">Remarks</span></span>

<span data-ttu-id="bfe41-116">Este método solo es válido cuando el control está activo en contexto.</span><span class="sxs-lookup"><span data-stu-id="bfe41-116">This method is only valid when the control is in-place active.</span></span> <span data-ttu-id="bfe41-117">Puede producirse un error en las llamadas realizadas mientras el control está inactivo.</span><span class="sxs-lookup"><span data-stu-id="bfe41-117">Calls made while the control is inactive may fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfe41-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfe41-118">Requirements</span></span>



| <span data-ttu-id="bfe41-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfe41-119">Requirement</span></span> | <span data-ttu-id="bfe41-120">Value</span><span class="sxs-lookup"><span data-stu-id="bfe41-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bfe41-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfe41-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bfe41-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bfe41-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bfe41-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfe41-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bfe41-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bfe41-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bfe41-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfe41-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfe41-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfe41-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfe41-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfe41-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="bfe41-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="bfe41-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bfe41-129">**\_GETSCROLLPOS em**</span><span class="sxs-lookup"><span data-stu-id="bfe41-129">**EM\_GETSCROLLPOS**</span></span>](em-getscrollpos.md)
</dt> <dt>

[<span data-ttu-id="bfe41-130">**\_SETSCROLLPOS em**</span><span class="sxs-lookup"><span data-stu-id="bfe41-130">**EM\_SETSCROLLPOS**</span></span>](em-setscrollpos.md)
</dt> </dl>

 

 





