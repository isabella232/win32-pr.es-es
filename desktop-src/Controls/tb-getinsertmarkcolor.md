---
title: Mensaje de TB_GETINSERTMARKCOLOR (commctrl. h)
description: Recupera el color usado para dibujar la marca de inserción de la barra de herramientas.
ms.assetid: 52915dc6-a45c-4f3b-aa9b-99a23d423e59
keywords:
- TB_GETINSERTMARKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 104ceebd5f3989ed870cf70ccad819300d85c05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905262"
---
# <a name="tb_getinsertmarkcolor-message"></a><span data-ttu-id="bdb77-104">\_Mensaje GETINSERTMARKCOLOR TB</span><span class="sxs-lookup"><span data-stu-id="bdb77-104">TB\_GETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="bdb77-105">Recupera el color usado para dibujar la marca de inserción de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="bdb77-105">Retrieves the color used to draw the insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="bdb77-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bdb77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdb77-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bdb77-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bdb77-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bdb77-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bdb77-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdb77-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bdb77-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bdb77-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdb77-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bdb77-111">Return value</span></span>

<span data-ttu-id="bdb77-112">Devuelve un valor de [**COLORREF**](/windows/desktop/gdi/colorref) que contiene el color de la marca de inserción actual.</span><span class="sxs-lookup"><span data-stu-id="bdb77-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that contains the current insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdb77-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdb77-113">Requirements</span></span>



| <span data-ttu-id="bdb77-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdb77-114">Requirement</span></span> | <span data-ttu-id="bdb77-115">Value</span><span class="sxs-lookup"><span data-stu-id="bdb77-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdb77-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bdb77-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bdb77-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bdb77-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bdb77-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bdb77-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bdb77-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bdb77-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bdb77-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bdb77-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdb77-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdb77-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdb77-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="bdb77-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdb77-123">**TB \_ SETINSERTMARKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="bdb77-123">**TB\_SETINSERTMARKCOLOR**</span></span>](tb-setinsertmarkcolor.md)
</dt> </dl>

 

