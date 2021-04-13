---
title: Mensaje de WM_ENTERIDLE (Winuser. h)
description: Se envía a la ventana propietaria de un cuadro de diálogo o un menú modal que está entrando en un estado de inactividad. Un cuadro de diálogo o un menú modal entra en un estado de inactividad cuando no hay mensajes en espera en su cola después de haber procesado uno o más mensajes anteriores.
ms.assetid: 11b1f942-185f-4de4-90a2-e2934bb1394f
keywords:
- WM_ENTERIDLE cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_ENTERIDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f99b3150a0dbc1a81b78498c8e295fbf2397c22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422502"
---
# <a name="wm_enteridle-message"></a><span data-ttu-id="3b3db-105">Mensaje de ENTERIDLE de WM \_</span><span class="sxs-lookup"><span data-stu-id="3b3db-105">WM\_ENTERIDLE message</span></span>

<span data-ttu-id="3b3db-106">Se envía a la ventana propietaria de un cuadro de diálogo o un menú modal que está entrando en un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="3b3db-106">Sent to the owner window of a modal dialog box or menu that is entering an idle state.</span></span> <span data-ttu-id="3b3db-107">Un cuadro de diálogo o un menú modal entra en un estado de inactividad cuando no hay mensajes en espera en su cola después de haber procesado uno o más mensajes anteriores.</span><span class="sxs-lookup"><span data-stu-id="3b3db-107">A modal dialog box or menu enters an idle state when no messages are waiting in its queue after it has processed one or more previous messages.</span></span>


```C++
#define WM_ENTERIDLE                    0x0121
```



## <a name="parameters"></a><span data-ttu-id="3b3db-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b3db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b3db-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3b3db-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b3db-110">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3b3db-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="3b3db-111">Valor</span><span class="sxs-lookup"><span data-stu-id="3b3db-111">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="3b3db-112">Significado</span><span class="sxs-lookup"><span data-stu-id="3b3db-112">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="MSGF_DIALOGBOX"></span><span id="msgf_dialogbox"></span><dl> <span data-ttu-id="3b3db-113"><dt>**MSGF \_ DIALOGBOX**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3b3db-113"><dt>**MSGF\_DIALOGBOX**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="3b3db-114">El sistema está inactivo porque se muestra un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3b3db-114">The system is idle because a dialog box is displayed.</span></span><br/> |
| <span id="MSGF_MENU"></span><span id="msgf_menu"></span><dl> <span data-ttu-id="3b3db-115"><dt>**MSGF \_ MENÚ**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3b3db-115"><dt>**MSGF\_MENU**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="3b3db-116">El sistema está inactivo porque se muestra un menú.</span><span class="sxs-lookup"><span data-stu-id="3b3db-116">The system is idle because a menu is displayed.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="3b3db-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b3db-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b3db-118">Un identificador para el cuadro de diálogo (si *wParam* es **MSGF \_ DIALOGBOX**) o una ventana que contiene el menú mostrado (si *wParam* es el **\_ menú de MSGF**).</span><span class="sxs-lookup"><span data-stu-id="3b3db-118">A handle to the dialog box (if *wParam* is **MSGF\_DIALOGBOX**) or window containing the displayed menu (if *wParam* is **MSGF\_MENU**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b3db-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b3db-119">Return value</span></span>

<span data-ttu-id="3b3db-120">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="3b3db-120">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b3db-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b3db-121">Remarks</span></span>

<span data-ttu-id="3b3db-122">Puede suprimir el mensaje de **\_ ENTERIDLE de WM** para un cuadro de diálogo creando el cuadro de diálogo con el estilo **DS \_ NOIDLEMSG** .</span><span class="sxs-lookup"><span data-stu-id="3b3db-122">You can suppress the **WM\_ENTERIDLE** message for a dialog box by creating the dialog box with the **DS\_NOIDLEMSG** style.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b3db-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b3db-123">Requirements</span></span>



| <span data-ttu-id="3b3db-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b3db-124">Requirement</span></span> | <span data-ttu-id="3b3db-125">Value</span><span class="sxs-lookup"><span data-stu-id="3b3db-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b3db-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b3db-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3b3db-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3b3db-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3b3db-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b3db-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3b3db-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3b3db-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3b3db-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b3db-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b3db-131"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b3db-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b3db-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b3db-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="3b3db-133">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="3b3db-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3b3db-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="3b3db-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="3b3db-135">**Vista**</span><span class="sxs-lookup"><span data-stu-id="3b3db-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3b3db-136">Cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="3b3db-136">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

