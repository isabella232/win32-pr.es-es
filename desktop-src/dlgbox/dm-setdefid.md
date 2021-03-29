---
title: Mensaje de DM_SETDEFID (Winuser. h)
description: Cambia el identificador del botón de opción predeterminado para un cuadro de diálogo.
ms.assetid: 30720fa1-48cb-42d4-8370-87bdbaa34600
keywords:
- DM_SETDEFID cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- DM_SETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ceda9ac9e8fd399604e9c55431b8fcd74646f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535265"
---
# <a name="dm_setdefid-message"></a><span data-ttu-id="08ded-104">\_Mensaje SETDEFID de DM</span><span class="sxs-lookup"><span data-stu-id="08ded-104">DM\_SETDEFID message</span></span>

<span data-ttu-id="08ded-105">Cambia el identificador del botón de opción predeterminado para un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="08ded-105">Changes the identifier of the default push button for a dialog box.</span></span>


```C++
#define WM_USER              0x0400
#define DM_SETDEFID         (WM_USER+1)
```



## <a name="parameters"></a><span data-ttu-id="08ded-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08ded-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08ded-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08ded-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08ded-108">Identificador de un control de botón de control que se convertirá en el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="08ded-108">The identifier of a push button control that will become the default.</span></span>

</dd> <dt>

<span data-ttu-id="08ded-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08ded-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08ded-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="08ded-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08ded-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08ded-111">Return value</span></span>

<span data-ttu-id="08ded-112">El valor devuelto siempre es **true**.</span><span class="sxs-lookup"><span data-stu-id="08ded-112">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="08ded-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08ded-113">Remarks</span></span>

<span data-ttu-id="08ded-114">Este mensaje lo procesa la función [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) .</span><span class="sxs-lookup"><span data-stu-id="08ded-114">This message is processed by the [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) function.</span></span> <span data-ttu-id="08ded-115">Para establecer el botón de opción predeterminado, la función puede enviar mensajes [**WM \_ GETDLGCODE**](wm-getdlgcode.md) y [**BM \_ SETSTYLE**](../controls/bm-setstyle.md) al control especificado y al botón de opción predeterminado actual.</span><span class="sxs-lookup"><span data-stu-id="08ded-115">To set the default push button, the function can send [**WM\_GETDLGCODE**](wm-getdlgcode.md) and [**BM\_SETSTYLE**](../controls/bm-setstyle.md) messages to the specified control and the current default push button.</span></span>

<span data-ttu-id="08ded-116">El uso del mensaje **DM \_ SETDEFID** puede dar lugar a que aparezca más de un botón para que tenga el estado del botón de envío predeterminado.</span><span class="sxs-lookup"><span data-stu-id="08ded-116">Using the **DM\_SETDEFID** message can result in more than one button appearing to have the default push button state.</span></span> <span data-ttu-id="08ded-117">Cuando el sistema abre un cuadro de diálogo, dibuja el primer botón de opción de la plantilla de cuadro de diálogo con el borde de estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="08ded-117">When the system brings up a dialog, it draws the first push button in the dialog template with the default state border.</span></span> <span data-ttu-id="08ded-118">El envío de un mensaje **DM \_ SETDEFID** para cambiar el botón predeterminado no quitará siempre el borde de estado predeterminado del primer botón de la tecla de opción.</span><span class="sxs-lookup"><span data-stu-id="08ded-118">Sending a **DM\_SETDEFID** message to change the default button will not always remove the default state border from the first push button.</span></span> <span data-ttu-id="08ded-119">En estos casos, la aplicación debe enviar un mensaje de [**BM \_ SETSTYLE**](../controls/bm-setstyle.md) para cambiar el primer estilo de borde del botón de la tecla.</span><span class="sxs-lookup"><span data-stu-id="08ded-119">In these cases, the application should send a [**BM\_SETSTYLE**](../controls/bm-setstyle.md) message to change the first push button border style.</span></span>

## <a name="requirements"></a><span data-ttu-id="08ded-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08ded-120">Requirements</span></span>



| <span data-ttu-id="08ded-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="08ded-121">Requirement</span></span> | <span data-ttu-id="08ded-122">Value</span><span class="sxs-lookup"><span data-stu-id="08ded-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08ded-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08ded-123">Minimum supported client</span></span><br/> | <span data-ttu-id="08ded-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="08ded-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="08ded-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08ded-125">Minimum supported server</span></span><br/> | <span data-ttu-id="08ded-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="08ded-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="08ded-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08ded-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="08ded-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08ded-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08ded-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="08ded-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="08ded-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="08ded-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="08ded-131">**DefDlgProc**</span><span class="sxs-lookup"><span data-stu-id="08ded-131">**DefDlgProc**</span></span>](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="08ded-132">**DM \_ GETDEFID**</span><span class="sxs-lookup"><span data-stu-id="08ded-132">**DM\_GETDEFID**</span></span>](dm-getdefid.md)
</dt> <dt>

[<span data-ttu-id="08ded-133">**GETDLGCODE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="08ded-133">**WM\_GETDLGCODE**</span></span>](wm-getdlgcode.md)
</dt> <dt>

<span data-ttu-id="08ded-134">**Vista**</span><span class="sxs-lookup"><span data-stu-id="08ded-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="08ded-135">Cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="08ded-135">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="08ded-136">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="08ded-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="08ded-137">**BM \_ SETSTYLE**</span><span class="sxs-lookup"><span data-stu-id="08ded-137">**BM\_SETSTYLE**</span></span>](../controls/bm-setstyle.md)
</dt> <dt>

[<span data-ttu-id="08ded-138">**\_SETLIMITTEXT em**</span><span class="sxs-lookup"><span data-stu-id="08ded-138">**EM\_SETLIMITTEXT**</span></span>](../controls/em-setlimittext.md)
</dt> </dl>

 

