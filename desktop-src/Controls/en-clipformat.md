---
title: Código de notificación de EN_CLIPFORMAT (RichEdit. h)
description: Notifica a la ventana primaria de un control Rich Edit que se ha realizado una copia con un formato de Portapapeles determinado. Un control Rich Edit sin ventanas envía esta notificación mediante el método ITextHost TxNotify.
ms.assetid: 79FE1350-4D45-447B-B705-63E966AC7F0E
keywords:
- EN_CLIPFORMAT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_CLIPFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0430e8a4dba0b1a18f81f4e28ec67f2c93551cd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996218"
---
# <a name="en_clipformat-notification-code"></a><span data-ttu-id="e61f8-105">\_Código de notificación en CLIPFORMAT</span><span class="sxs-lookup"><span data-stu-id="e61f8-105">EN\_CLIPFORMAT notification code</span></span>

<span data-ttu-id="e61f8-106">Notifica a la ventana primaria de un control Rich Edit que se ha realizado una copia con un formato de Portapapeles determinado.</span><span class="sxs-lookup"><span data-stu-id="e61f8-106">Notifies a rich edit control's parent window that a paste occurred with a particular clipboard format.</span></span> <span data-ttu-id="e61f8-107">Un control Rich Edit sin ventanas envía esta notificación mediante el método [**ITextHost:: TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) .</span><span class="sxs-lookup"><span data-stu-id="e61f8-107">A windowless rich edit control sends this notification by using the [**ITextHost::TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method.</span></span>


```C++
EN_CLIPFORMAT

      pClipboardFmt = (CLIPBOARDFORMAT *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e61f8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e61f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e61f8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e61f8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e61f8-110">IDENTIFICADOR de ventana que se ha recuperado mediante una llamada a la función [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) con el valor de identificador de GWL \_ .</span><span class="sxs-lookup"><span data-stu-id="e61f8-110">The window ID retrieved by calling the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_ID value.</span></span>

</dd> <dt>

<span data-ttu-id="e61f8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e61f8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e61f8-112">Puntero a una estructura [**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) que contiene información sobre el formato del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="e61f8-112">A pointer to a [**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) structure that contains information about the clipboard format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e61f8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e61f8-113">Return value</span></span>

<span data-ttu-id="e61f8-114">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="e61f8-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="e61f8-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e61f8-115">Remarks</span></span>

<span data-ttu-id="e61f8-116">Para recibir los \_ códigos de notificación en CLIPFORMAT, especifique [**ENM \_ CLIPFORMAT**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="e61f8-116">To receive EN\_CLIPFORMAT notification codes, specify [**ENM\_CLIPFORMAT**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e61f8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e61f8-117">Requirements</span></span>



| <span data-ttu-id="e61f8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e61f8-118">Requirement</span></span> | <span data-ttu-id="e61f8-119">Value</span><span class="sxs-lookup"><span data-stu-id="e61f8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e61f8-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e61f8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e61f8-121">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e61f8-121">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e61f8-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e61f8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e61f8-123">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e61f8-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e61f8-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e61f8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e61f8-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e61f8-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e61f8-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e61f8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e61f8-127">**CLIPBOARDFORMAT**</span><span class="sxs-lookup"><span data-stu-id="e61f8-127">**CLIPBOARDFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 

