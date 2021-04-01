---
title: Mensaje de TB_SETINSERTMARKCOLOR (commctrl. h)
description: Establece el color utilizado para dibujar la marca de inserción de la barra de herramientas.
ms.assetid: 09a04449-9a1f-4f9a-b09f-9f22f930d735
keywords:
- TB_SETINSERTMARKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 954654d71a3e3b7bba9af287d3e92fb2362e8711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149886"
---
# <a name="tb_setinsertmarkcolor-message"></a><span data-ttu-id="46d19-104">\_Mensaje SETINSERTMARKCOLOR TB</span><span class="sxs-lookup"><span data-stu-id="46d19-104">TB\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="46d19-105">Establece el color utilizado para dibujar la marca de inserción de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="46d19-105">Sets the color used to draw the insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="46d19-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46d19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46d19-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="46d19-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="46d19-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="46d19-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="46d19-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="46d19-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46d19-110">Valor de **COLORREF** que contiene el nuevo color de la marca de inserción.</span><span class="sxs-lookup"><span data-stu-id="46d19-110">**COLORREF** value that contains the new insertion mark color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46d19-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46d19-111">Return value</span></span>

<span data-ttu-id="46d19-112">Devuelve un valor de **COLORREF** que contiene el color anterior de la marca de inserción.</span><span class="sxs-lookup"><span data-stu-id="46d19-112">Returns a **COLORREF** value that contains the previous insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="46d19-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46d19-113">Requirements</span></span>



| <span data-ttu-id="46d19-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="46d19-114">Requirement</span></span> | <span data-ttu-id="46d19-115">Value</span><span class="sxs-lookup"><span data-stu-id="46d19-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46d19-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46d19-116">Minimum supported client</span></span><br/> | <span data-ttu-id="46d19-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="46d19-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="46d19-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46d19-118">Minimum supported server</span></span><br/> | <span data-ttu-id="46d19-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="46d19-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46d19-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46d19-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="46d19-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="46d19-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46d19-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="46d19-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46d19-123">**TB \_ GETINSERTMARKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="46d19-123">**TB\_GETINSERTMARKCOLOR**</span></span>](tb-getinsertmarkcolor.md)
</dt> </dl>

 

 





