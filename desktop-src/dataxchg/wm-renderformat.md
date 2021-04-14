---
title: Mensaje de WM_RENDERFORMAT (Winuser. h)
description: Se envía al propietario del portapapeles si ha retrasado la representación de un formato específico del portapapeles y si una aplicación ha solicitado datos en ese formato.
ms.assetid: 81638109-4c5e-4b4c-b2db-4208b6ee83cc
keywords:
- Intercambio de datos de mensajes de WM_RENDERFORMAT
topic_type:
- apiref
api_name:
- WM_RENDERFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9d0e8539dc666c7a791a24c9ba7ac772c3c2c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359740"
---
# <a name="wm_renderformat-message"></a><span data-ttu-id="a9bcb-104">Mensaje de RENDERFORMAT de WM \_</span><span class="sxs-lookup"><span data-stu-id="a9bcb-104">WM\_RENDERFORMAT message</span></span>

<span data-ttu-id="a9bcb-105">Se envía al propietario del portapapeles si ha retrasado la representación de un formato específico del portapapeles y si una aplicación ha solicitado datos en ese formato.</span><span class="sxs-lookup"><span data-stu-id="a9bcb-105">Sent to the clipboard owner if it has delayed rendering a specific clipboard format and if an application has requested data in that format.</span></span> <span data-ttu-id="a9bcb-106">El propietario del portapapeles debe representar los datos en el formato especificado y colocarlos en el portapapeles mediante una llamada a la función [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) .</span><span class="sxs-lookup"><span data-stu-id="a9bcb-106">The clipboard owner must render data in the specified format and place it on the clipboard by calling the [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) function.</span></span>


```C++
#define WM_RENDERFORMAT                 0x0305
```



## <a name="parameters"></a><span data-ttu-id="a9bcb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a9bcb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9bcb-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9bcb-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9bcb-109">[Formato del portapapeles](standard-clipboard-formats.md) que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="a9bcb-109">The [clipboard format](standard-clipboard-formats.md) to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="a9bcb-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9bcb-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9bcb-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a9bcb-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9bcb-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9bcb-112">Return value</span></span>

<span data-ttu-id="a9bcb-113">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="a9bcb-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9bcb-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9bcb-114">Remarks</span></span>

<span data-ttu-id="a9bcb-115">Cuando se responde a un mensaje de **\_ RENDERFORMAT de WM** , el propietario del portapapeles no debe abrir el portapapeles antes de llamar a [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span><span class="sxs-lookup"><span data-stu-id="a9bcb-115">When responding to a **WM\_RENDERFORMAT** message, the clipboard owner must not open the clipboard before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span></span> <span data-ttu-id="a9bcb-116">No es necesario abrir el portapapeles antes de colocar los datos en respuesta a **WM \_ RENDERFORMAT** y se producirá un error al intentar abrir el portapapeles, ya que la aplicación que solicitó el formato para representarlo tiene abierto el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="a9bcb-116">Opening the clipboard is not necessary before placing data in response to **WM\_RENDERFORMAT**, and any attempt to open the clipboard will fail because the clipboard is currently being held open by the application that requested the format to be rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9bcb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9bcb-117">Requirements</span></span>



| <span data-ttu-id="a9bcb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9bcb-118">Requirement</span></span> | <span data-ttu-id="a9bcb-119">Value</span><span class="sxs-lookup"><span data-stu-id="a9bcb-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9bcb-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9bcb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a9bcb-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a9bcb-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a9bcb-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9bcb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a9bcb-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a9bcb-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a9bcb-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9bcb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9bcb-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9bcb-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9bcb-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9bcb-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="a9bcb-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="a9bcb-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a9bcb-128">**SetClipboardData**</span><span class="sxs-lookup"><span data-stu-id="a9bcb-128">**SetClipboardData**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[<span data-ttu-id="a9bcb-129">**RENDERALLFORMATS de WM \_**</span><span class="sxs-lookup"><span data-stu-id="a9bcb-129">**WM\_RENDERALLFORMATS**</span></span>](wm-renderallformats.md)
</dt> <dt>

<span data-ttu-id="a9bcb-130">**Vista**</span><span class="sxs-lookup"><span data-stu-id="a9bcb-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a9bcb-131">Portapapeles</span><span class="sxs-lookup"><span data-stu-id="a9bcb-131">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

 





