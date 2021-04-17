---
description: El mensaje de CTLCOLOR de WM \_ se usa en las versiones de 16 bits de Windows para cambiar la combinación de colores de los cuadros de lista, los cuadros de lista de los cuadros combinados, los cuadros de mensaje, los controles de botón, los controles de edición, los controles estáticos y los cuadros de diálogo. Nota para obtener información relacionada con este mensaje y con las versiones de 32 bits de Windows, consulte la sección Comentarios.
ms.assetid: e654cf48-550f-4210-9952-20470b9a397a
title: Mensaje de WM_CTLCOLOR (WindowsX. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8166979c17b7d2eef50af062e5df13712e9d32ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660717"
---
# <a name="wm_ctlcolor-message"></a><span data-ttu-id="d4f96-103">Mensaje de CTLCOLOR de WM \_</span><span class="sxs-lookup"><span data-stu-id="d4f96-103">WM\_CTLCOLOR message</span></span>

<span data-ttu-id="d4f96-104">El mensaje de **\_ CTLCOLOR de WM** se usa en las versiones de 16 bits de Windows para cambiar la combinación de colores de los cuadros de lista, los cuadros de lista de los cuadros combinados, los cuadros de mensaje, los controles de botón, los controles de edición, los controles estáticos y los cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d4f96-104">The **WM\_CTLCOLOR** message is used in 16-bit versions of Windows to change the color scheme of list boxes, the list boxes of combo boxes, message boxes, button controls, edit controls, static controls, and dialog boxes.</span></span>

> [!Note]  
> <span data-ttu-id="d4f96-105">Para obtener información relacionada con este mensaje y versiones de 32 bits de Windows, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="d4f96-105">For information related to this message and 32-bit versions of Windows, see Remarks.</span></span>

 


```C++
  WM_CTLCOLOR

  WPARAM wParam;
  LPARAM lParam;
    
```



## <a name="parameters"></a><span data-ttu-id="d4f96-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4f96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4f96-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="d4f96-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d4f96-108">Identificador de la ventana de destino.</span><span class="sxs-lookup"><span data-stu-id="d4f96-108">A handle to destination window.</span></span>

</dd> <dt>

<span data-ttu-id="d4f96-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d4f96-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4f96-110">Identificador de un contexto de presentación (DC).</span><span class="sxs-lookup"><span data-stu-id="d4f96-110">A handle to a display context (DC).</span></span>

</dd> <dt>

<span data-ttu-id="d4f96-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d4f96-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4f96-112">Identificador de una ventana secundaria (control).</span><span class="sxs-lookup"><span data-stu-id="d4f96-112">A handle to a child window (control).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4f96-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4f96-113">Return value</span></span>

<span data-ttu-id="d4f96-114">Si una aplicación procesa este mensaje, devuelve un identificador a un pincel.</span><span class="sxs-lookup"><span data-stu-id="d4f96-114">If an application processes this message, it returns a handle to a brush.</span></span> <span data-ttu-id="d4f96-115">El sistema utiliza el pincel para pintar el fondo del control.</span><span class="sxs-lookup"><span data-stu-id="d4f96-115">The system uses the brush to paint the background of the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4f96-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4f96-116">Remarks</span></span>

<span data-ttu-id="d4f96-117">El mensaje de **\_ CTLCOLOR de WM** de Windows de 16 bits se ha sustituido por notificaciones más específicas.</span><span class="sxs-lookup"><span data-stu-id="d4f96-117">The **WM\_CTLCOLOR** message from 16-bit Windows has been replaced by more specific notifications.</span></span> <span data-ttu-id="d4f96-118">Entre estos reemplazos se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d4f96-118">These replacements include the following:</span></span>

-   [<span data-ttu-id="d4f96-119">**CTLCOLORBTN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d4f96-119">**WM\_CTLCOLORBTN**</span></span>](../controls/wm-ctlcolorbtn.md)
-   [<span data-ttu-id="d4f96-120">**CTLCOLOREDIT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d4f96-120">**WM\_CTLCOLOREDIT**</span></span>](../controls/wm-ctlcoloredit.md)
-   [<span data-ttu-id="d4f96-121">**CTLCOLORDLG de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d4f96-121">**WM\_CTLCOLORDLG**</span></span>](../dlgbox/wm-ctlcolordlg.md)
-   [<span data-ttu-id="d4f96-122">**CTLCOLORLISTBOX de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d4f96-122">**WM\_CTLCOLORLISTBOX**</span></span>](../controls/wm-ctlcolorlistbox.md)
-   [<span data-ttu-id="d4f96-123">**CTLCOLORSCROLLBAR de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d4f96-123">**WM\_CTLCOLORSCROLLBAR**</span></span>](../controls/wm-ctlcolorscrollbar.md)
-   [<span data-ttu-id="d4f96-124">**CTLCOLORSTATIC de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d4f96-124">**WM\_CTLCOLORSTATIC**</span></span>](../controls/wm-ctlcolorstatic.md)

## <a name="requirements"></a><span data-ttu-id="d4f96-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4f96-125">Requirements</span></span>



| <span data-ttu-id="d4f96-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4f96-126">Requirement</span></span> | <span data-ttu-id="d4f96-127">Value</span><span class="sxs-lookup"><span data-stu-id="d4f96-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f96-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4f96-128">Header</span></span><br/> | <dl> <span data-ttu-id="d4f96-129"><dt>WindowsX. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4f96-129"><dt>WindowsX.h</dt></span></span> </dl> |



 

 
