---
title: Barras de desplazamiento plana
description: Microsoft Internet Explorer 4,0 presentó una nueva tecnología visual denominada barras de desplazamiento plana.
ms.assetid: f7e00e71-bf12-4db9-bb84-6d413b967049
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fbbdb64aa9815cb56f5dc3bf55ffb17390db38
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793995"
---
# <a name="flat-scroll-bars"></a><span data-ttu-id="a5582-103">Barras de desplazamiento plana</span><span class="sxs-lookup"><span data-stu-id="a5582-103">Flat Scroll Bars</span></span>

<span data-ttu-id="a5582-104">Microsoft Internet Explorer 4,0 presentó una nueva tecnología visual denominada barras de desplazamiento plana.</span><span class="sxs-lookup"><span data-stu-id="a5582-104">Microsoft Internet Explorer 4.0 introduced a new visual technology called flat scroll bars.</span></span> <span data-ttu-id="a5582-105">Funcionalmente, las barras de desplazamiento sin formato se comportan igual que las barras de desplazamiento estándar.</span><span class="sxs-lookup"><span data-stu-id="a5582-105">Functionally, flat scroll bars behave just like standard scroll bars.</span></span> <span data-ttu-id="a5582-106">La diferencia es que puede personalizar su apariencia en una extensión mayor que las barras de desplazamiento estándar.</span><span class="sxs-lookup"><span data-stu-id="a5582-106">The difference is that you can customize their appearance to a greater extent than standard scroll bars.</span></span>

<span data-ttu-id="a5582-107">En la ilustración siguiente se muestra una ventana que contiene una barra de desplazamiento plana.</span><span class="sxs-lookup"><span data-stu-id="a5582-107">The following illustration shows a window that contains a flat scroll bar.</span></span>

![captura de pantalla de una ventana que contiene una barra de desplazamiento plana](images/flatsb.jpg)

> [!Note]  
> <span data-ttu-id="a5582-109">Las barras de desplazamiento plana son compatibles con las versiones de Comctl32.dll 4,71 a 5,82.</span><span class="sxs-lookup"><span data-stu-id="a5582-109">Flat scroll bars are supported by Comctl32.dll versions 4.71 through 5.82.</span></span> <span data-ttu-id="a5582-110">Comctl32.dll versiones 6,00 y posteriores no admiten barras de desplazamiento sin formato.</span><span class="sxs-lookup"><span data-stu-id="a5582-110">Comctl32.dll versions 6.00 and later do not support flat scroll bars.</span></span>

 

## <a name="using-flat-scroll-bars"></a><span data-ttu-id="a5582-111">Usar barras de desplazamiento plana</span><span class="sxs-lookup"><span data-stu-id="a5582-111">Using Flat Scroll Bars</span></span>

<span data-ttu-id="a5582-112">En esta sección se describe cómo implementar barras de desplazamiento sin formato en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a5582-112">This section describes how to implement flat scroll bars in your application.</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="a5582-113">Antes de empezar</span><span class="sxs-lookup"><span data-stu-id="a5582-113">Before You Begin</span></span>

<span data-ttu-id="a5582-114">Para usar las funciones de barra de desplazamiento plana, debe incluir commctrl. h en los archivos de código fuente y vincular con COMCTL32. lib.</span><span class="sxs-lookup"><span data-stu-id="a5582-114">To use the flat scroll bar functions, you must include Commctrl.h in your source files and link with Comctl32.lib.</span></span>

### <a name="adding-flat-scroll-bars-to-a-window"></a><span data-ttu-id="a5582-115">Agregar barras de desplazamiento sin formato a una ventana</span><span class="sxs-lookup"><span data-stu-id="a5582-115">Adding Flat Scroll Bars to a Window</span></span>

<span data-ttu-id="a5582-116">Para agregar barras de desplazamiento plana a una ventana, llame a [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), pasando el identificador a la ventana.</span><span class="sxs-lookup"><span data-stu-id="a5582-116">To add flat scroll bars to a window, call [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), passing the handle to the window.</span></span> <span data-ttu-id="a5582-117">En lugar de usar las funciones de barra de desplazamiento estándar para manipular las barras de desplazamiento, debe usar la función equivalente FlatSB \_ xxx.</span><span class="sxs-lookup"><span data-stu-id="a5582-117">Instead of using the standard scroll bar functions to manipulate your scroll bars, you must use the equivalent FlatSB\_XXX function.</span></span> <span data-ttu-id="a5582-118">Hay funciones de barra de desplazamiento plana para establecer y recuperar la información de desplazamiento, el intervalo y la posición.</span><span class="sxs-lookup"><span data-stu-id="a5582-118">There are flat scroll bar functions for setting and retrieving the scroll information, range, and position.</span></span> <span data-ttu-id="a5582-119">Si las barras de desplazamiento sin formato no se han inicializado para la ventana, la API de la barra de desplazamiento plana diferirá a las funciones estándar correspondientes, en caso de que se use alguna.</span><span class="sxs-lookup"><span data-stu-id="a5582-119">If flat scroll bars haven't been initialized for your window, the flat scroll bar API will defer to the corresponding standard functions, if any are used.</span></span> <span data-ttu-id="a5582-120">Esto le permite activar y desactivar las barras de desplazamiento sin necesidad de escribir código condicional.</span><span class="sxs-lookup"><span data-stu-id="a5582-120">This allows you to turn flat scroll bars on and off without having to write conditional code.</span></span>

<span data-ttu-id="a5582-121">Dado que una aplicación puede haber establecido métricas personalizadas para sus barras de desplazamiento sin formato, no se actualizan automáticamente cuando se modifican las métricas del sistema.</span><span class="sxs-lookup"><span data-stu-id="a5582-121">Because an application may have set custom metrics for its flat scroll bars, they are not automatically updated when system metrics change.</span></span> <span data-ttu-id="a5582-122">Cuando cambian las métricas de la barra de desplazamiento del sistema, se emite un mensaje de [**\_ SETTINGCHANGE de WM**](/windows/desktop/winmsg/wm-settingchange) , con el valor de *wParam* establecido en [**SPI \_ SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span><span class="sxs-lookup"><span data-stu-id="a5582-122">When the system scroll bar metrics change, a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message is broadcast, with its *wParam* set to [**SPI\_SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span></span> <span data-ttu-id="a5582-123">Para actualizar las barras de desplazamiento plana a las nuevas métricas del sistema, las aplicaciones deben controlar este mensaje y cambiar explícitamente las propiedades dependientes de las métricas de la barra de desplazamiento plana.</span><span class="sxs-lookup"><span data-stu-id="a5582-123">To update flat scroll bars to the new system metrics, applications must handle this message and change the flat scroll bar's metric-dependent properties explicitly.</span></span>

<span data-ttu-id="a5582-124">Para actualizar las propiedades de la barra de desplazamiento, utilice [**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop).</span><span class="sxs-lookup"><span data-stu-id="a5582-124">To update your scroll bar properties, use [**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop).</span></span> <span data-ttu-id="a5582-125">El siguiente fragmento de código cambia las propiedades dependientes de las métricas de una barra de desplazamiento sin formato a los valores actuales del sistema.</span><span class="sxs-lookup"><span data-stu-id="a5582-125">The following code fragment changes a flat scroll bar's metric dependent properties to the current system values.</span></span>


```
void FlatSB_UpdateMetrics(HWND hWnd)
{
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXVSCROLL, GetSystemMetrics(SM_CXVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHSCROLL, GetSystemMetrics(SM_CXHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVSCROLL, GetSystemMetrics(SM_CYVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYHSCROLL, GetSystemMetrics(SM_CYHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHTHUMB, GetSystemMetrics(SM_CXHTHUMB), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVTHUMB, GetSystemMetrics(SM_CYVTHUMB), TRUE);
}
```



### <a name="enhancing-flat-scroll-bars"></a><span data-ttu-id="a5582-126">Mejorar las barras de desplazamiento plana</span><span class="sxs-lookup"><span data-stu-id="a5582-126">Enhancing Flat Scroll Bars</span></span>

<span data-ttu-id="a5582-127">[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) le permite modificar las barras de desplazamiento plana para personalizar la apariencia de la ventana.</span><span class="sxs-lookup"><span data-stu-id="a5582-127">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) allows you to modify the flat scroll bars to customize the look of your window.</span></span> <span data-ttu-id="a5582-128">En el caso de las barras de desplazamiento verticales, puede cambiar el ancho de la barra y el alto de las flechas de dirección.</span><span class="sxs-lookup"><span data-stu-id="a5582-128">For vertical scroll bars, you can change the width of the bar and the height of the direction arrows.</span></span> <span data-ttu-id="a5582-129">En el caso de las barras de desplazamiento horizontal, puede cambiar el alto de la barra y el ancho de las flechas de dirección.</span><span class="sxs-lookup"><span data-stu-id="a5582-129">For horizontal scroll bars, you can change the height of the bar and the width of the direction arrows.</span></span> <span data-ttu-id="a5582-130">También puede cambiar el color de fondo de las barras de desplazamiento horizontal y vertical.</span><span class="sxs-lookup"><span data-stu-id="a5582-130">You can also change the background color of both the horizontal and vertical scroll bars.</span></span>

<span data-ttu-id="a5582-131">[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) también le permite personalizar cómo se muestran las barras de desplazamiento sin formato.</span><span class="sxs-lookup"><span data-stu-id="a5582-131">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) also allows you to customize how the flat scroll bars are displayed.</span></span> <span data-ttu-id="a5582-132">Mediante el cambio de las propiedades de la \_ \_ propiedad VSTYLE y la \_ propiedad HSTYLE de la propiedad WSB \_ , puede establecer el tipo de barra de desplazamiento que desea utilizar.</span><span class="sxs-lookup"><span data-stu-id="a5582-132">By changing the WSB\_PROP\_VSTYLE and WSB\_PROP\_HSTYLE properties, you can set the type of scroll bar that you want to use.</span></span> <span data-ttu-id="a5582-133">Hay tres estilos disponibles.</span><span class="sxs-lookup"><span data-stu-id="a5582-133">Three styles are available.</span></span>



|                    |                                                                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5582-134">\_modo Encarta de FSB \_</span><span class="sxs-lookup"><span data-stu-id="a5582-134">FSB\_ENCARTA\_MODE</span></span> | <span data-ttu-id="a5582-135">Se muestra una barra de desplazamiento estándar.</span><span class="sxs-lookup"><span data-stu-id="a5582-135">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="a5582-136">Cuando el mouse se mueve sobre un botón de dirección o el control de posición, esa parte de la barra de desplazamiento se mostrará en 3D.</span><span class="sxs-lookup"><span data-stu-id="a5582-136">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in 3-D.</span></span>             |
| <span data-ttu-id="a5582-137">\_modo plano de FSB \_</span><span class="sxs-lookup"><span data-stu-id="a5582-137">FSB\_FLAT\_MODE</span></span>    | <span data-ttu-id="a5582-138">Se muestra una barra de desplazamiento estándar.</span><span class="sxs-lookup"><span data-stu-id="a5582-138">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="a5582-139">Cuando el mouse se mueve sobre un botón de dirección o el control de posición, esa parte de la barra de desplazamiento se mostrará en los colores invertidos.</span><span class="sxs-lookup"><span data-stu-id="a5582-139">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in inverted colors.</span></span> |
| <span data-ttu-id="a5582-140">\_modo normal de FSB \_</span><span class="sxs-lookup"><span data-stu-id="a5582-140">FSB\_REGULAR\_MODE</span></span> | <span data-ttu-id="a5582-141">Se muestra una barra de desplazamiento normal y no plana.</span><span class="sxs-lookup"><span data-stu-id="a5582-141">A normal, nonflat scroll bar is displayed.</span></span> <span data-ttu-id="a5582-142">No se aplicarán efectos visuales especiales.</span><span class="sxs-lookup"><span data-stu-id="a5582-142">No special visual effects will be applied.</span></span>                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a><span data-ttu-id="a5582-143">Quitar barras de desplazamiento plana</span><span class="sxs-lookup"><span data-stu-id="a5582-143">Removing Flat Scroll Bars</span></span>

<span data-ttu-id="a5582-144">Si desea quitar las barras de desplazamiento plana de la ventana, llame a la función [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) , pasando el identificador a la ventana.</span><span class="sxs-lookup"><span data-stu-id="a5582-144">If you want to remove flat scroll bars from your window, call the [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) function, passing the handle to the window.</span></span> <span data-ttu-id="a5582-145">Esta función solo quita las barras de desplazamiento sin formato de la ventana en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="a5582-145">This function only removes flat scroll bars from your window at run time.</span></span> <span data-ttu-id="a5582-146">No es necesario llamar a esta función cuando se destruye la ventana.</span><span class="sxs-lookup"><span data-stu-id="a5582-146">You do not need to call this function when your window is destroyed.</span></span>

 

 