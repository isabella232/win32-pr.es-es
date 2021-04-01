---
title: Mensaje de WM_CLIPBOARDUPDATE (Winuser. h)
description: Se envía cuando cambia el contenido del portapapeles.
ms.assetid: 1508aa22-9cf0-40a2-8cb0-ce7c8671df2c
keywords:
- Intercambio de datos de mensajes de WM_CLIPBOARDUPDATE
topic_type:
- apiref
api_name:
- WM_CLIPBOARDUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303110f0d094cfed336a9f92006b3720a0ccc83b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150421"
---
# <a name="wm_clipboardupdate-message"></a><span data-ttu-id="bc393-104">Mensaje de CLIPBOARDUPDATE de WM \_</span><span class="sxs-lookup"><span data-stu-id="bc393-104">WM\_CLIPBOARDUPDATE message</span></span>

<span data-ttu-id="bc393-105">Se envía cuando cambia el contenido del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="bc393-105">Sent when the contents of the clipboard have changed.</span></span>


```C++
#define WM_CLIPBOARDUPDATE              0x031D
```



## <a name="parameters"></a><span data-ttu-id="bc393-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc393-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc393-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bc393-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc393-108">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bc393-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bc393-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc393-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc393-110">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bc393-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc393-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc393-111">Return value</span></span>

<span data-ttu-id="bc393-112">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="bc393-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc393-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc393-113">Remarks</span></span>

<span data-ttu-id="bc393-114">Para registrar una ventana para recibir este mensaje, utilice la función [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) .</span><span class="sxs-lookup"><span data-stu-id="bc393-114">To register a window to receive this message, use the [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc393-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc393-115">Requirements</span></span>



| <span data-ttu-id="bc393-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc393-116">Requirement</span></span> | <span data-ttu-id="bc393-117">Value</span><span class="sxs-lookup"><span data-stu-id="bc393-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc393-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc393-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bc393-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bc393-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bc393-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc393-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bc393-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bc393-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bc393-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc393-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc393-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc393-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc393-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc393-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc393-125">**AddClipboardFormatListener**</span><span class="sxs-lookup"><span data-stu-id="bc393-125">**AddClipboardFormatListener**</span></span>](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener)
</dt> <dt>

[<span data-ttu-id="bc393-126">**RemoveClipboardFormatListener**</span><span class="sxs-lookup"><span data-stu-id="bc393-126">**RemoveClipboardFormatListener**</span></span>](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener)
</dt> <dt>

[<span data-ttu-id="bc393-127">**GetClipboardSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="bc393-127">**GetClipboardSequenceNumber**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber)
</dt> </dl>

 

 





