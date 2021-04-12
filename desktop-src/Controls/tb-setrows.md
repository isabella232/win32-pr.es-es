---
title: Mensaje de TB_SETROWS (commctrl. h)
description: Establece el número de filas de los botones de una barra de herramientas.
ms.assetid: d8ea7b80-d23e-4593-8eb1-d23808173fc9
keywords:
- TB_SETROWS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d0065a3f5f6a277713e368177886ebd064ea132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079776"
---
# <a name="tb_setrows-message"></a><span data-ttu-id="40a20-104">\_Mensaje SETROWS TB</span><span class="sxs-lookup"><span data-stu-id="40a20-104">TB\_SETROWS message</span></span>

<span data-ttu-id="40a20-105">Establece el número de filas de los botones de una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="40a20-105">Sets the number of rows of buttons in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="40a20-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40a20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40a20-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="40a20-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40a20-108">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el número de filas solicitadas.</span><span class="sxs-lookup"><span data-stu-id="40a20-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the number of rows requested.</span></span> <span data-ttu-id="40a20-109">El número mínimo de filas es uno y el número máximo de filas es igual al número de botones de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="40a20-109">The minimum number of rows is one, and the maximum number of rows is equal to the number of buttons in the toolbar.</span></span>

<span data-ttu-id="40a20-110">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) es un valor **booleano** que indica si se van a crear más filas de las que se solicitan cuando el sistema no puede crear el número de filas especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="40a20-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **BOOL** that indicates whether to create more rows than requested when the system cannot create the number of rows specified by *wParam*.</span></span> <span data-ttu-id="40a20-111">Si **es true**, el sistema crea más filas.</span><span class="sxs-lookup"><span data-stu-id="40a20-111">If **TRUE**, the system creates more rows.</span></span> <span data-ttu-id="40a20-112">Si **es false**, el sistema crea menos filas.</span><span class="sxs-lookup"><span data-stu-id="40a20-112">If **FALSE**, the system creates fewer rows.</span></span>

</dd> <dt>

<span data-ttu-id="40a20-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="40a20-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40a20-114">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibe el rectángulo delimitador de la barra de herramientas una vez establecidas las filas.</span><span class="sxs-lookup"><span data-stu-id="40a20-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle of the toolbar after the rows are set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40a20-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40a20-115">Return value</span></span>

<span data-ttu-id="40a20-116">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="40a20-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="40a20-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40a20-117">Remarks</span></span>

<span data-ttu-id="40a20-118">Dado que el sistema no divide los grupos de botones al establecer el número de filas, el número resultante de filas podría diferir del número solicitado.</span><span class="sxs-lookup"><span data-stu-id="40a20-118">Because the system does not break up button groups when setting the number of rows, the resulting number of rows might differ from the number requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="40a20-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40a20-119">Requirements</span></span>



| <span data-ttu-id="40a20-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="40a20-120">Requirement</span></span> | <span data-ttu-id="40a20-121">Value</span><span class="sxs-lookup"><span data-stu-id="40a20-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40a20-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40a20-122">Minimum supported client</span></span><br/> | <span data-ttu-id="40a20-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="40a20-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="40a20-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40a20-124">Minimum supported server</span></span><br/> | <span data-ttu-id="40a20-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="40a20-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="40a20-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40a20-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="40a20-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="40a20-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

