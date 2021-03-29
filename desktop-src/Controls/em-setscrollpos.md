---
title: Mensaje EM_SETSCROLLPOS (RichEdit. h)
description: Desplaza el contenido de un control Rich Edit al punto especificado.
ms.assetid: 9ec514a4-97b1-44ab-b2ca-973b1f6fc404
keywords:
- EM_SETSCROLLPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41ac5255059b8d40f3a4c2e9b666815b9094fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492449"
---
# <a name="em_setscrollpos-message"></a><span data-ttu-id="2069b-104">\_Mensaje SETSCROLLPOS em</span><span class="sxs-lookup"><span data-stu-id="2069b-104">EM\_SETSCROLLPOS message</span></span>

<span data-ttu-id="2069b-105">Desplaza el contenido de un control Rich Edit al punto especificado.</span><span class="sxs-lookup"><span data-stu-id="2069b-105">Scrolls the contents of a rich edit control to the specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="2069b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2069b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2069b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2069b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2069b-108">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2069b-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2069b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2069b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2069b-110">Puntero a una estructura de [**punto**](/previous-versions//dd162805(v=vs.85)) que especifica un punto en el espacio de texto virtual del documento, expresado en píxeles.</span><span class="sxs-lookup"><span data-stu-id="2069b-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure which specifies a point in the virtual text space of the document, expressed in pixels.</span></span> <span data-ttu-id="2069b-111">El documento se desplazará hasta que este punto se encuentre en la esquina superior izquierda de la ventana Editar control.</span><span class="sxs-lookup"><span data-stu-id="2069b-111">The document will be scrolled until this point is located in the upper-left corner of the edit control window.</span></span> <span data-ttu-id="2069b-112">Si desea cambiar la vista de forma que la esquina superior izquierda de la vista tenga dos líneas hacia abajo y un carácter en el borde izquierdo.</span><span class="sxs-lookup"><span data-stu-id="2069b-112">If you want to change the view such that the upper left corner of the view is two lines down and one character in from the left edge.</span></span> <span data-ttu-id="2069b-113">Pasaría un punto de (7, 22).</span><span class="sxs-lookup"><span data-stu-id="2069b-113">You would pass a point of (7, 22).</span></span>

<span data-ttu-id="2069b-114">El control Rich Edit comprueba las coordenadas x e y, y las ajusta si es necesario, para que se muestre una línea completa en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="2069b-114">The rich edit control checks the x and y coordinates and adjusts them if necessary, so that a complete line is displayed at the top.</span></span> <span data-ttu-id="2069b-115">También garantiza que el texto nunca se desplaza completamente fuera del rectángulo de la vista.</span><span class="sxs-lookup"><span data-stu-id="2069b-115">It also ensures that the text is never completely scrolled off the view rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2069b-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2069b-116">Return value</span></span>

<span data-ttu-id="2069b-117">Este mensaje siempre devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="2069b-117">This message always returns 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="2069b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2069b-118">Requirements</span></span>



| <span data-ttu-id="2069b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2069b-119">Requirement</span></span> | <span data-ttu-id="2069b-120">Value</span><span class="sxs-lookup"><span data-stu-id="2069b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2069b-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2069b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2069b-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2069b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2069b-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2069b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2069b-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2069b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2069b-125">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="2069b-125">Redistributable</span></span><br/>          | <span data-ttu-id="2069b-126">Edición enriquecida 3,0</span><span class="sxs-lookup"><span data-stu-id="2069b-126">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="2069b-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2069b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2069b-128"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2069b-128"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2069b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="2069b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2069b-130">**\_GETSCROLLPOS em**</span><span class="sxs-lookup"><span data-stu-id="2069b-130">**EM\_GETSCROLLPOS**</span></span>](em-getscrollpos.md)
</dt> </dl>

 

