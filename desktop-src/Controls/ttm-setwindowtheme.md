---
title: Mensaje de TTM_SETWINDOWTHEME (commctrl. h)
description: Establece el estilo visual de un control ToolTip.
ms.assetid: eeddb91e-8eb8-4480-9ab2-5efa9e3ef48a
keywords:
- TTM_SETWINDOWTHEME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9c3f25b62bf0fe38a679234183cd5046f60784f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535248"
---
# <a name="ttm_setwindowtheme-message"></a><span data-ttu-id="97091-104">TTM \_ SETWINDOWTHEME</span><span class="sxs-lookup"><span data-stu-id="97091-104">TTM\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="97091-105">Establece el estilo visual de un control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="97091-105">Sets the visual style of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="97091-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97091-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97091-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97091-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="97091-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="97091-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="97091-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97091-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97091-110">Puntero a una cadena Unicode que contiene el estilo visual de información sobre herramientas que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="97091-110">Pointer to a Unicode string that contains the tooltip visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97091-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97091-111">Return value</span></span>

<span data-ttu-id="97091-112">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="97091-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="97091-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97091-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="97091-114">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="97091-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="97091-115">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="97091-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="97091-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97091-116">Requirements</span></span>



| <span data-ttu-id="97091-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="97091-117">Requirement</span></span> | <span data-ttu-id="97091-118">Value</span><span class="sxs-lookup"><span data-stu-id="97091-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97091-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97091-119">Minimum supported client</span></span><br/> | <span data-ttu-id="97091-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="97091-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="97091-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97091-121">Minimum supported server</span></span><br/> | <span data-ttu-id="97091-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="97091-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97091-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97091-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="97091-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="97091-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





