---
title: Mensaje de CQPM_HELP (Cmnquery. h)
description: Se envía a la función de devolución de llamada CQPageProc de una página de extensión de formulario de consulta para permitir que la extensión de página muestre ayuda contextual para la página.
ms.assetid: 07f5bd24-bca2-4d87-8e1e-acce552a3bf2
ms.tgt_platform: multiple
keywords:
- CQPM_HELP Active Directory de mensaje
topic_type:
- apiref
api_name:
- CQPM_HELP
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7635b87a0ba489c63f87fb32742c37a9f7044860
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149986"
---
# <a name="cqpm_help-message"></a><span data-ttu-id="c4a17-104">CQPM \_ mensaje de ayuda</span><span class="sxs-lookup"><span data-stu-id="c4a17-104">CQPM\_HELP message</span></span>

<span data-ttu-id="c4a17-105">El mensaje de **\_ ayuda CQPM** se envía a la función de devolución de llamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de una página de extensión de formulario de consulta para permitir que la extensión de página muestre ayuda contextual para la página.</span><span class="sxs-lookup"><span data-stu-id="c4a17-105">The **CQPM\_HELP** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to allow the page extension to display context-sensitive help for the page.</span></span> <span data-ttu-id="c4a17-106">Si es posible, la extensión de página de consulta debe mostrar ayuda contextual en respuesta a este evento.</span><span class="sxs-lookup"><span data-stu-id="c4a17-106">If possible, the query page extension should display context-sensitive help in response to this event.</span></span>

## <a name="parameters"></a><span data-ttu-id="c4a17-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4a17-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4a17-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4a17-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4a17-109">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="c4a17-109">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4a17-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4a17-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4a17-111">Puntero a una estructura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que contiene datos adicionales sobre el elemento de menú, el control, el cuadro de diálogo o la ventana para la que se solicita ayuda contextual.</span><span class="sxs-lookup"><span data-stu-id="c4a17-111">Pointer to a [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure that contains additional data about the menu item, control, dialog box, or window for which context-sensitive help is requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4a17-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4a17-112">Return value</span></span>

<span data-ttu-id="c4a17-113">Se omite el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="c4a17-113">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4a17-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4a17-114">Requirements</span></span>



| <span data-ttu-id="c4a17-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4a17-115">Requirement</span></span> | <span data-ttu-id="c4a17-116">Value</span><span class="sxs-lookup"><span data-stu-id="c4a17-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a17-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4a17-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c4a17-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4a17-118">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="c4a17-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4a17-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c4a17-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4a17-120">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="c4a17-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4a17-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4a17-122"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4a17-122"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4a17-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4a17-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4a17-124">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="c4a17-124">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="c4a17-125">**HELPINFO**</span><span class="sxs-lookup"><span data-stu-id="c4a17-125">**HELPINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-helpinfo)
</dt> </dl>

 

