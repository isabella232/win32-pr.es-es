---
title: Mensaje de PSM_GETCURRENTPAGEHWND (Prsht. h)
description: Recupera un identificador de la ventana de la página actual de una hoja de propiedades. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ GetCurrentPageHwnd.
ms.assetid: 1f2d0af9-5853-48e7-b827-483be032b6ca
keywords:
- PSM_GETCURRENTPAGEHWND controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_GETCURRENTPAGEHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae9ac89e6bc60317f2caf31ea92754d10983e11a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658317"
---
# <a name="psm_getcurrentpagehwnd-message"></a><span data-ttu-id="6ec47-105">Mensaje de PSM \_ GETCURRENTPAGEHWND</span><span class="sxs-lookup"><span data-stu-id="6ec47-105">PSM\_GETCURRENTPAGEHWND message</span></span>

<span data-ttu-id="6ec47-106">Recupera un identificador de la ventana de la página actual de una hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="6ec47-106">Retrieves a handle to the window of the current page of a property sheet.</span></span> <span data-ttu-id="6ec47-107">Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) .</span><span class="sxs-lookup"><span data-stu-id="6ec47-107">You can send this message explicitly or by using the [**PropSheet\_GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ec47-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ec47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ec47-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ec47-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ec47-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6ec47-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6ec47-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ec47-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ec47-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6ec47-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ec47-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ec47-113">Return value</span></span>

<span data-ttu-id="6ec47-114">Devuelve un identificador a la ventana de la página de la hoja de propiedades actual.</span><span class="sxs-lookup"><span data-stu-id="6ec47-114">Returns a handle to the window of the current property sheet page.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ec47-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ec47-115">Remarks</span></span>

<span data-ttu-id="6ec47-116">Use el mensaje **PSM \_ GETCURRENTPAGEHWND** con hojas de propiedades no modales para determinar cuándo se debe destruir el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6ec47-116">Use the **PSM\_GETCURRENTPAGEHWND** message with modeless property sheets to determine when to destroy the dialog box.</span></span> <span data-ttu-id="6ec47-117">Cuando el usuario hace clic en el botón **Aceptar** o **Cancelar** , **PSM \_ GETCURRENTPAGEHWND** devuelve **null** y, a continuación, puede usar la función [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para destruir el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6ec47-117">When the user clicks the **OK** or **Cancel** button, **PSM\_GETCURRENTPAGEHWND** returns **NULL**, and you can then use the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function to destroy the dialog box.</span></span>

> [!Note]  
> <span data-ttu-id="6ec47-118">Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="6ec47-118">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6ec47-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ec47-119">Requirements</span></span>



| <span data-ttu-id="6ec47-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ec47-120">Requirement</span></span> | <span data-ttu-id="6ec47-121">Value</span><span class="sxs-lookup"><span data-stu-id="6ec47-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec47-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ec47-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6ec47-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6ec47-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6ec47-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ec47-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6ec47-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ec47-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6ec47-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ec47-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ec47-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ec47-127"><dt>Prsht.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ec47-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ec47-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ec47-129">**Hoja**</span><span class="sxs-lookup"><span data-stu-id="6ec47-129">**PropertySheet**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

