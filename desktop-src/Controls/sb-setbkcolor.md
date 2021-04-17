---
title: Mensaje de SB_SETBKCOLOR (commctrl. h)
description: Establece el color de fondo de una barra de estado.
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- SB_SETBKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc08687c6d228074bc3e4dd7c8442a1c1e35a835
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422516"
---
# <a name="sb_setbkcolor-message"></a><span data-ttu-id="3e6c7-104">\_Mensaje SETBKCOLOR de SB</span><span class="sxs-lookup"><span data-stu-id="3e6c7-104">SB\_SETBKCOLOR message</span></span>

<span data-ttu-id="3e6c7-105">Establece el color de fondo de una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="3e6c7-105">Sets the background color in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="3e6c7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e6c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e6c7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3e6c7-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3e6c7-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3e6c7-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3e6c7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e6c7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e6c7-110">Valor [**COLORREF**](/windows/desktop/gdi/colorref) que especifica el nuevo color de fondo.</span><span class="sxs-lookup"><span data-stu-id="3e6c7-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that specifies the new background color.</span></span> <span data-ttu-id="3e6c7-111">Especifique el \_ valor predeterminado de CLR para que la barra de estado use su color de fondo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3e6c7-111">Specify the CLR\_DEFAULT value to cause the status bar to use its default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e6c7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e6c7-112">Return value</span></span>

<span data-ttu-id="3e6c7-113">Devuelve el color de fondo anterior, o el \_ valor predeterminado de CLR si el color de fondo es el color predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3e6c7-113">Returns the previous background color, or CLR\_DEFAULT if the background color is the default color.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e6c7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e6c7-114">Requirements</span></span>



| <span data-ttu-id="3e6c7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e6c7-115">Requirement</span></span> | <span data-ttu-id="3e6c7-116">Value</span><span class="sxs-lookup"><span data-stu-id="3e6c7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e6c7-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e6c7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3e6c7-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3e6c7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3e6c7-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e6c7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3e6c7-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e6c7-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3e6c7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e6c7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e6c7-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e6c7-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

