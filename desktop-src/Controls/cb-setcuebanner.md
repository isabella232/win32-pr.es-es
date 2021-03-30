---
title: Mensaje de CB_SETCUEBANNER (Winuser. h)
description: Establece el texto del titular de indicación que se muestra para el control de edición de un cuadro combinado.
ms.assetid: 4b2b5042-ba64-4e3f-adeb-9aea66773b0e
keywords:
- CB_SETCUEBANNER controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5799b1b1be5e938ce1e234948a1f7d878122f30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079358"
---
# <a name="cb_setcuebanner-message"></a><span data-ttu-id="6ec1a-104">\_Mensaje SETCUEBANNER CB</span><span class="sxs-lookup"><span data-stu-id="6ec1a-104">CB\_SETCUEBANNER message</span></span>

<span data-ttu-id="6ec1a-105">Establece el texto del titular de indicación que se muestra para el control de edición de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="6ec1a-105">Sets the cue banner text that is displayed for the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ec1a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ec1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ec1a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ec1a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ec1a-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6ec1a-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6ec1a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ec1a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ec1a-110">Un puntero a un búfer de cadena Unicode terminada en null que contiene el texto.</span><span class="sxs-lookup"><span data-stu-id="6ec1a-110">A pointer to a null-terminated Unicode string buffer that contains the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ec1a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ec1a-111">Return value</span></span>

<span data-ttu-id="6ec1a-112">Devuelve 1 si se realiza correctamente, o un valor de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6ec1a-112">Returns 1 if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ec1a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ec1a-113">Remarks</span></span>

<span data-ttu-id="6ec1a-114">El banner de indicación es el texto que se muestra en el control de edición de un cuadro combinado cuando no hay ninguna selección.</span><span class="sxs-lookup"><span data-stu-id="6ec1a-114">The cue banner is text that is displayed in the edit control of a combo box when there is no selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ec1a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ec1a-115">Requirements</span></span>



| <span data-ttu-id="6ec1a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ec1a-116">Requirement</span></span> | <span data-ttu-id="6ec1a-117">Value</span><span class="sxs-lookup"><span data-stu-id="6ec1a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec1a-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ec1a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6ec1a-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6ec1a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6ec1a-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ec1a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6ec1a-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ec1a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6ec1a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ec1a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ec1a-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ec1a-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ec1a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ec1a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ec1a-125">Características del cuadro combinado</span><span class="sxs-lookup"><span data-stu-id="6ec1a-125">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





