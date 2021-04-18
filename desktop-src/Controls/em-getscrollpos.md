---
title: Mensaje EM_GETSCROLLPOS (RichEdit. h)
description: Obtiene la posición de desplazamiento actual del control de edición.
ms.assetid: 26e122da-f1b4-4694-978c-ff678dad5d9f
keywords:
- EM_GETSCROLLPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70458abca94e483f8e202f13ecaed3df04a68366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490378"
---
# <a name="em_getscrollpos-message"></a><span data-ttu-id="9b3d5-104">\_Mensaje GETSCROLLPOS em</span><span class="sxs-lookup"><span data-stu-id="9b3d5-104">EM\_GETSCROLLPOS message</span></span>

<span data-ttu-id="9b3d5-105">Obtiene la posición de desplazamiento actual del control de edición.</span><span class="sxs-lookup"><span data-stu-id="9b3d5-105">Obtains the current scroll position of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b3d5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b3d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b3d5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b3d5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b3d5-108">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9b3d5-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9b3d5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b3d5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b3d5-110">Puntero a una estructura de [**punto**](/previous-versions//dd162805(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9b3d5-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <span data-ttu-id="9b3d5-111">Después de llamar a **em \_ GETSCROLLPOS**, este parámetro contiene un punto en el espacio de texto virtual del documento, expresado en píxeles.</span><span class="sxs-lookup"><span data-stu-id="9b3d5-111">After calling **EM\_GETSCROLLPOS**, this parameters contains a point in the virtual text space of the document, expressed in pixels.</span></span> <span data-ttu-id="9b3d5-112">Este punto será el punto que se encuentra actualmente en la esquina superior izquierda de la ventana Editar control.</span><span class="sxs-lookup"><span data-stu-id="9b3d5-112">This point will be the point that is currently located in the upper-left corner of the edit control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b3d5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b3d5-113">Return value</span></span>

<span data-ttu-id="9b3d5-114">Este mensaje siempre devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="9b3d5-114">This message always returns 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b3d5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b3d5-115">Remarks</span></span>

<span data-ttu-id="9b3d5-116">Los valores devueltos en la estructura [**Point**](/previous-versions//dd162805(v=vs.85)) son valores de 16 bits (incluso en los campos anchos de 32 bits).</span><span class="sxs-lookup"><span data-stu-id="9b3d5-116">The values returned in the [**POINT**](/previous-versions//dd162805(v=vs.85)) structure are 16-bit values (even in the 32-bit wide fields).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b3d5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b3d5-117">Requirements</span></span>



| <span data-ttu-id="9b3d5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b3d5-118">Requirement</span></span> | <span data-ttu-id="9b3d5-119">Value</span><span class="sxs-lookup"><span data-stu-id="9b3d5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b3d5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b3d5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9b3d5-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9b3d5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9b3d5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b3d5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9b3d5-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b3d5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9b3d5-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="9b3d5-124">Redistributable</span></span><br/>          | <span data-ttu-id="9b3d5-125">Edición enriquecida 3,0</span><span class="sxs-lookup"><span data-stu-id="9b3d5-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="9b3d5-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b3d5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b3d5-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b3d5-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b3d5-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b3d5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b3d5-129">**\_SETSCROLLPOS em**</span><span class="sxs-lookup"><span data-stu-id="9b3d5-129">**EM\_SETSCROLLPOS**</span></span>](em-setscrollpos.md)
</dt> </dl>

 

