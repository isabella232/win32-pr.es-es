---
description: El mensaje de PALETTEISCHANGING de WM \_ informa a las aplicaciones de que una aplicación va a obtener su paleta lógica.
ms.assetid: 64ec1042-0ab5-496f-9a88-2f293b412704
title: Mensaje de WM_PALETTEISCHANGING (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2127dc9c682bba1fc4cea4e10b2b96ecc92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815526"
---
# <a name="wm_paletteischanging-message"></a><span data-ttu-id="ed13a-103">Mensaje de PALETTEISCHANGING de WM \_</span><span class="sxs-lookup"><span data-stu-id="ed13a-103">WM\_PALETTEISCHANGING message</span></span>

<span data-ttu-id="ed13a-104">El mensaje de **\_ PALETTEISCHANGING de WM** informa a las aplicaciones de que una aplicación va a obtener su paleta lógica.</span><span class="sxs-lookup"><span data-stu-id="ed13a-104">The **WM\_PALETTEISCHANGING** message informs applications that an application is going to realize its logical palette.</span></span>

<span data-ttu-id="ed13a-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ed13a-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="ed13a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed13a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed13a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed13a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed13a-108">Identificador de la ventana que va a obtener su paleta lógica.</span><span class="sxs-lookup"><span data-stu-id="ed13a-108">A handle to the window that is going to realize its logical palette.</span></span>

</dd> <dt>

<span data-ttu-id="ed13a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed13a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed13a-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ed13a-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed13a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed13a-111">Return value</span></span>

<span data-ttu-id="ed13a-112">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="ed13a-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed13a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed13a-113">Remarks</span></span>

<span data-ttu-id="ed13a-114">La aplicación que cambia su paleta no espera la confirmación de este mensaje antes de cambiar la paleta y enviar el mensaje de [**\_ PALETTECHANGED de WM**](wm-palettechanged.md) .</span><span class="sxs-lookup"><span data-stu-id="ed13a-114">The application changing its palette does not wait for acknowledgment of this message before changing the palette and sending the [**WM\_PALETTECHANGED**](wm-palettechanged.md) message.</span></span> <span data-ttu-id="ed13a-115">Como resultado, es posible que la paleta ya haya cambiado en el momento en que una aplicación recibe este mensaje.</span><span class="sxs-lookup"><span data-stu-id="ed13a-115">As a result, the palette may already be changed by the time an application receives this message.</span></span>

<span data-ttu-id="ed13a-116">Si la aplicación pasa por alto o no puede procesar este mensaje y una segunda aplicación detecta su paleta mientras que la primera usa índices de paleta, existe la posibilidad de que el usuario vea colores inesperados durante las operaciones de dibujo posteriores.</span><span class="sxs-lookup"><span data-stu-id="ed13a-116">If the application either ignores or fails to process this message and a second application realizes its palette while the first is using palette indexes, there is a strong possibility that the user will see unexpected colors during subsequent drawing operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed13a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed13a-117">Requirements</span></span>



| <span data-ttu-id="ed13a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed13a-118">Requirement</span></span> | <span data-ttu-id="ed13a-119">Value</span><span class="sxs-lookup"><span data-stu-id="ed13a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed13a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed13a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ed13a-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ed13a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ed13a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed13a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ed13a-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ed13a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ed13a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed13a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed13a-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed13a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed13a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed13a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed13a-127">Información general sobre colores</span><span class="sxs-lookup"><span data-stu-id="ed13a-127">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="ed13a-128">Mensajes de color</span><span class="sxs-lookup"><span data-stu-id="ed13a-128">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="ed13a-129">**PALETTECHANGED de WM \_**</span><span class="sxs-lookup"><span data-stu-id="ed13a-129">**WM\_PALETTECHANGED**</span></span>](wm-palettechanged.md)
</dt> <dt>

[<span data-ttu-id="ed13a-130">**QUERYNEWPALETTE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="ed13a-130">**WM\_QUERYNEWPALETTE**</span></span>](wm-querynewpalette.md)
</dt> </dl>

 

 
