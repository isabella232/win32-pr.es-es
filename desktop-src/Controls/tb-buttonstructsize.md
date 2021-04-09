---
title: Mensaje de TB_BUTTONSTRUCTSIZE (commctrl. h)
description: Especifica el tamaño de la estructura TBBUTTON.
ms.assetid: 4e63a075-4191-44c1-8df6-38fce51d4be5
keywords:
- TB_BUTTONSTRUCTSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_BUTTONSTRUCTSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7187c1f4cb45306fd293c7eb74ef8807f395ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079779"
---
# <a name="tb_buttonstructsize-message"></a><span data-ttu-id="b166c-104">\_Mensaje BUTTONSTRUCTSIZE TB</span><span class="sxs-lookup"><span data-stu-id="b166c-104">TB\_BUTTONSTRUCTSIZE message</span></span>

<span data-ttu-id="b166c-105">Especifica el tamaño de la estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) .</span><span class="sxs-lookup"><span data-stu-id="b166c-105">Specifies the size of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure.</span></span>

## <a name="parameters"></a><span data-ttu-id="b166c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b166c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b166c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b166c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b166c-108">Tamaño, en bytes, de la estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) .</span><span class="sxs-lookup"><span data-stu-id="b166c-108">Size, in bytes, of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b166c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b166c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b166c-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b166c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b166c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b166c-111">Return value</span></span>

<span data-ttu-id="b166c-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b166c-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b166c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b166c-113">Remarks</span></span>

<span data-ttu-id="b166c-114">El sistema utiliza el tamaño para determinar qué versión de la biblioteca de vínculos dinámicos (DLL) de controles comunes se está usando.</span><span class="sxs-lookup"><span data-stu-id="b166c-114">The system uses the size to determine which version of the common control dynamic-link library (DLL) is being used.</span></span>

<span data-ttu-id="b166c-115">Si una aplicación usa la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear la barra de herramientas, la aplicación debe enviar este mensaje a la barra de herramientas antes de enviar el mensaje [**TB \_ ADDBITMAP**](tb-addbitmap.md) o [**TB \_ ADDBUTTONS**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="b166c-115">If an application uses the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create the toolbar, the application must send this message to the toolbar before sending the [**TB\_ADDBITMAP**](tb-addbitmap.md) or [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span> <span data-ttu-id="b166c-116">La función [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) envía automáticamente **TB \_ BUTTONSTRUCTSIZE** y el tamaño de la estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) es un parámetro de la función.</span><span class="sxs-lookup"><span data-stu-id="b166c-116">The [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) function automatically sends **TB\_BUTTONSTRUCTSIZE**, and the size of the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure is a parameter of the function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b166c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b166c-117">Requirements</span></span>



| <span data-ttu-id="b166c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b166c-118">Requirement</span></span> | <span data-ttu-id="b166c-119">Value</span><span class="sxs-lookup"><span data-stu-id="b166c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b166c-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b166c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b166c-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b166c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b166c-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b166c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b166c-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b166c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b166c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b166c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b166c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b166c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

