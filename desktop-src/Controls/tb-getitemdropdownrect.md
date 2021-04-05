---
title: Mensaje de TB_GETITEMDROPDOWNRECT (commctrl. h)
description: Obtiene el rectángulo delimitador de la ventana desplegable para un elemento de barra de herramientas con la \_ lista desplegable de estilo BTNS.
ms.assetid: 4b59c96b-8d75-44c1-b771-c1d62502a2c2
keywords:
- TB_GETITEMDROPDOWNRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcbcef725b0ade0bfc776200fa5b191618d2ccb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078995"
---
# <a name="tb_getitemdropdownrect-message"></a><span data-ttu-id="fd363-104">\_Mensaje GETITEMDROPDOWNRECT TB</span><span class="sxs-lookup"><span data-stu-id="fd363-104">TB\_GETITEMDROPDOWNRECT message</span></span>

<span data-ttu-id="fd363-105">Obtiene el rectángulo delimitador de la ventana desplegable para un elemento de barra de herramientas con la [**\_ lista desplegable**](toolbar-control-and-button-styles.md)de estilo BTNS.</span><span class="sxs-lookup"><span data-stu-id="fd363-105">Gets the bounding rectangle of the dropdown window for a toolbar item with style [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="fd363-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd363-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd363-107">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fd363-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd363-108">Índice de base cero del elemento de control de la barra de herramientas para el que se va a recuperar el rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="fd363-108">The zero-based index of the toolbar control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="fd363-109">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fd363-109">*lParam* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="fd363-110">Puntero a una estructura <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> para recibir la información del rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="fd363-110">A pointer to a <a href="/previous-versions//dd162897(v=vs.85)">**RECT**</a> structure to receive the bounding rectangle information.</span></span> <span data-ttu-id="fd363-111">El remitente del mensaje es responsable de la asignación de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="fd363-111">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="fd363-112">Las coordenadas devueltas en la estructura **Rect** se expresan como coordenadas de cliente.</span><span class="sxs-lookup"><span data-stu-id="fd363-112">The coordinates returned in the **RECT** structure are expressed as client coordinates.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd363-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd363-113">Return value</span></span>

<span data-ttu-id="fd363-114">Siempre devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="fd363-114">Always returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd363-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd363-115">Remarks</span></span>

<span data-ttu-id="fd363-116">El elemento debe tener el estilo de [**\_ lista desplegable BTNS**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fd363-116">The item must have the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd363-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd363-117">Requirements</span></span>



| <span data-ttu-id="fd363-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd363-118">Requirement</span></span> | <span data-ttu-id="fd363-119">Value</span><span class="sxs-lookup"><span data-stu-id="fd363-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd363-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd363-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fd363-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fd363-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd363-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd363-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fd363-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fd363-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fd363-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd363-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd363-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd363-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

