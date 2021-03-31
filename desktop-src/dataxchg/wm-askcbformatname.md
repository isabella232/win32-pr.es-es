---
title: Mensaje de WM_ASKCBFORMATNAME (Winuser. h)
description: Se envía al propietario del portapapeles mediante una ventana del visor del portapapeles para solicitar el nombre de un \_ formato de Portapapeles de OWNERDISPLAY de CF.
ms.assetid: eee026ec-58db-41b3-9705-30a17eebbd70
keywords:
- Intercambio de datos de mensajes de WM_ASKCBFORMATNAME
topic_type:
- apiref
api_name:
- WM_ASKCBFORMATNAME
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b14a7f2fc2ff57076d6b694061466fd60e09dce0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150079"
---
# <a name="wm_askcbformatname-message"></a><span data-ttu-id="96ed7-104">Mensaje de ASKCBFORMATNAME de WM \_</span><span class="sxs-lookup"><span data-stu-id="96ed7-104">WM\_ASKCBFORMATNAME message</span></span>

<span data-ttu-id="96ed7-105">Se envía al propietario del portapapeles mediante una ventana del visor del portapapeles para solicitar el nombre de un formato de Portapapeles de [**\_ OWNERDISPLAY de CF**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="96ed7-105">Sent to the clipboard owner by a clipboard viewer window to request the name of a [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) clipboard format.</span></span>

<span data-ttu-id="96ed7-106">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="96ed7-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ASKCBFORMATNAME              0x030C
```



## <a name="parameters"></a><span data-ttu-id="96ed7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96ed7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96ed7-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96ed7-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96ed7-109">Tamaño, en caracteres, del búfer al que apunta el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="96ed7-109">The size, in characters, of the buffer pointed to by the *lParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="96ed7-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96ed7-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96ed7-111">Puntero al búfer que va a recibir el nombre de formato del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="96ed7-111">A pointer to the buffer that is to receive the clipboard format name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96ed7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96ed7-112">Return value</span></span>

<span data-ttu-id="96ed7-113">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="96ed7-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="96ed7-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96ed7-114">Remarks</span></span>

<span data-ttu-id="96ed7-115">En respuesta a este mensaje, el propietario del portapapeles debe copiar el nombre del formato de presentación del propietario en el búfer especificado, sin superar el tamaño de búfer especificado por el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="96ed7-115">In response to this message, the clipboard owner should copy the name of the owner-display format to the specified buffer, not exceeding the buffer size specified by the *wParam* parameter.</span></span>

<span data-ttu-id="96ed7-116">Una ventana del visor del portapapeles envía este mensaje al propietario del portapapeles para determinar el nombre del formato [**\_ OWNERDISPLAY de CF**](standard-clipboard-formats.md) , por ejemplo, para inicializar un menú que muestre los formatos disponibles.</span><span class="sxs-lookup"><span data-stu-id="96ed7-116">A clipboard viewer window sends this message to the clipboard owner to determine the name of the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format   for example, to initialize a menu listing available formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="96ed7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96ed7-117">Requirements</span></span>



| <span data-ttu-id="96ed7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="96ed7-118">Requirement</span></span> | <span data-ttu-id="96ed7-119">Value</span><span class="sxs-lookup"><span data-stu-id="96ed7-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96ed7-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96ed7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="96ed7-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="96ed7-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="96ed7-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96ed7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="96ed7-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="96ed7-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="96ed7-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96ed7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="96ed7-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96ed7-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96ed7-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="96ed7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96ed7-127">Información general del portapapeles</span><span class="sxs-lookup"><span data-stu-id="96ed7-127">Clipboard Overview</span></span>](clipboard.md)
</dt> </dl>

 

