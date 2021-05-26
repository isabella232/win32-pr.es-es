---
title: Barras de desplazamiento plano
description: Microsoft Internet Explorer 4.0 introdujo una nueva tecnología visual denominada barras de desplazamiento plano.
ms.assetid: f7e00e71-bf12-4db9-bb84-6d413b967049
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e56db4ee987a6d8cdc7b185f5db0f8d89540453
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423895"
---
# <a name="flat-scroll-bars"></a><span data-ttu-id="c443c-103">Barras de desplazamiento plano</span><span class="sxs-lookup"><span data-stu-id="c443c-103">Flat Scroll Bars</span></span>

<span data-ttu-id="c443c-104">Microsoft Internet Explorer 4.0 introdujo una nueva tecnología visual denominada barras de desplazamiento plano.</span><span class="sxs-lookup"><span data-stu-id="c443c-104">Microsoft Internet Explorer 4.0 introduced a new visual technology called flat scroll bars.</span></span> <span data-ttu-id="c443c-105">Funcionalmente, las barras de desplazamiento planos se comportan igual que las barras de desplazamiento estándar.</span><span class="sxs-lookup"><span data-stu-id="c443c-105">Functionally, flat scroll bars behave just like standard scroll bars.</span></span> <span data-ttu-id="c443c-106">La diferencia es que puede personalizar su apariencia en mayor medida que las barras de desplazamiento estándar.</span><span class="sxs-lookup"><span data-stu-id="c443c-106">The difference is that you can customize their appearance to a greater extent than standard scroll bars.</span></span>

<span data-ttu-id="c443c-107">En la ilustración siguiente se muestra una ventana que contiene una barra de desplazamiento plana.</span><span class="sxs-lookup"><span data-stu-id="c443c-107">The following illustration shows a window that contains a flat scroll bar.</span></span>

![captura de pantalla de una ventana que contiene una barra de desplazamiento plana](images/flatsb.jpg)

> [!Note]  
> <span data-ttu-id="c443c-109">Las barras de desplazamiento planos son compatibles Comctl32.dll versiones 4.71 a 5.82.</span><span class="sxs-lookup"><span data-stu-id="c443c-109">Flat scroll bars are supported by Comctl32.dll versions 4.71 through 5.82.</span></span> <span data-ttu-id="c443c-110">Comctl32.dll versiones 6.00 y posteriores no admiten barras de desplazamiento planas.</span><span class="sxs-lookup"><span data-stu-id="c443c-110">Comctl32.dll versions 6.00 and later do not support flat scroll bars.</span></span>

 

## <a name="using-flat-scroll-bars"></a><span data-ttu-id="c443c-111">Uso de barras de desplazamiento planos</span><span class="sxs-lookup"><span data-stu-id="c443c-111">Using Flat Scroll Bars</span></span>

<span data-ttu-id="c443c-112">En esta sección se describe cómo implementar barras de desplazamiento planos en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c443c-112">This section describes how to implement flat scroll bars in your application.</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="c443c-113">Antes de empezar</span><span class="sxs-lookup"><span data-stu-id="c443c-113">Before You Begin</span></span>

<span data-ttu-id="c443c-114">Para usar las funciones de barra de desplazamiento plano, debe incluir Commctrl.h en los archivos de código fuente y vincular con Comctl32.lib.</span><span class="sxs-lookup"><span data-stu-id="c443c-114">To use the flat scroll bar functions, you must include Commctrl.h in your source files and link with Comctl32.lib.</span></span>

### <a name="adding-flat-scroll-bars-to-a-window"></a><span data-ttu-id="c443c-115">Agregar barras de desplazamiento plano a una ventana</span><span class="sxs-lookup"><span data-stu-id="c443c-115">Adding Flat Scroll Bars to a Window</span></span>

<span data-ttu-id="c443c-116">Para agregar barras de desplazamiento planas a una ventana, llame a [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb)y pase el identificador a la ventana.</span><span class="sxs-lookup"><span data-stu-id="c443c-116">To add flat scroll bars to a window, call [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), passing the handle to the window.</span></span> <span data-ttu-id="c443c-117">En lugar de usar las funciones de barra de desplazamiento estándar para manipular las barras de desplazamiento, debe usar la función \_ FlatSB XXX equivalente.</span><span class="sxs-lookup"><span data-stu-id="c443c-117">Instead of using the standard scroll bar functions to manipulate your scroll bars, you must use the equivalent FlatSB\_XXX function.</span></span> <span data-ttu-id="c443c-118">Hay funciones de barra de desplazamiento planas para establecer y recuperar la información de desplazamiento, el intervalo y la posición.</span><span class="sxs-lookup"><span data-stu-id="c443c-118">There are flat scroll bar functions for setting and retrieving the scroll information, range, and position.</span></span> <span data-ttu-id="c443c-119">Si las barras de desplazamiento plano no se han inicializado para la ventana, la API de barra de desplazamiento plano se aplazará a las funciones estándar correspondientes, si se usa alguna.</span><span class="sxs-lookup"><span data-stu-id="c443c-119">If flat scroll bars haven't been initialized for your window, the flat scroll bar API will defer to the corresponding standard functions, if any are used.</span></span> <span data-ttu-id="c443c-120">Esto le permite activar y desactivar las barras de desplazamiento planas sin tener que escribir código condicional.</span><span class="sxs-lookup"><span data-stu-id="c443c-120">This allows you to turn flat scroll bars on and off without having to write conditional code.</span></span>

<span data-ttu-id="c443c-121">Dado que una aplicación puede haber establecido métricas personalizadas para sus barras de desplazamiento planas, no se actualizan automáticamente cuando cambian las métricas del sistema.</span><span class="sxs-lookup"><span data-stu-id="c443c-121">Because an application may have set custom metrics for its flat scroll bars, they are not automatically updated when system metrics change.</span></span> <span data-ttu-id="c443c-122">Cuando cambian las métricas de la barra de desplazamiento del sistema, se difunde un mensaje [**\_ WM SETTINGCHANGE,**](/windows/desktop/winmsg/wm-settingchange) con *su wParam* establecido en [**SPI \_ SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span><span class="sxs-lookup"><span data-stu-id="c443c-122">When the system scroll bar metrics change, a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message is broadcast, with its *wParam* set to [**SPI\_SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span></span> <span data-ttu-id="c443c-123">Para actualizar las barras de desplazamiento planos a las nuevas métricas del sistema, las aplicaciones deben controlar este mensaje y cambiar explícitamente las propiedades dependientes de la métrica de la barra de desplazamiento plano.</span><span class="sxs-lookup"><span data-stu-id="c443c-123">To update flat scroll bars to the new system metrics, applications must handle this message and change the flat scroll bar's metric-dependent properties explicitly.</span></span>

<span data-ttu-id="c443c-124">Para actualizar las propiedades de la barra de desplazamiento, use [**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop).</span><span class="sxs-lookup"><span data-stu-id="c443c-124">To update your scroll bar properties, use [**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop).</span></span> <span data-ttu-id="c443c-125">El fragmento de código siguiente cambia las propiedades dependientes de métricas de una barra de desplazamiento plano a los valores actuales del sistema.</span><span class="sxs-lookup"><span data-stu-id="c443c-125">The following code fragment changes a flat scroll bar's metric dependent properties to the current system values.</span></span>


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



### <a name="enhancing-flat-scroll-bars"></a><span data-ttu-id="c443c-126">Mejorar las barras de desplazamiento planos</span><span class="sxs-lookup"><span data-stu-id="c443c-126">Enhancing Flat Scroll Bars</span></span>

<span data-ttu-id="c443c-127">[**FlatSB \_ SetScrollProp permite**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) modificar las barras de desplazamiento plano para personalizar la apariencia de la ventana.</span><span class="sxs-lookup"><span data-stu-id="c443c-127">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) allows you to modify the flat scroll bars to customize the look of your window.</span></span> <span data-ttu-id="c443c-128">Para las barras de desplazamiento verticales, puede cambiar el ancho de la barra y el alto de las flechas de dirección.</span><span class="sxs-lookup"><span data-stu-id="c443c-128">For vertical scroll bars, you can change the width of the bar and the height of the direction arrows.</span></span> <span data-ttu-id="c443c-129">Para las barras de desplazamiento horizontal, puede cambiar el alto de la barra y el ancho de las flechas de dirección.</span><span class="sxs-lookup"><span data-stu-id="c443c-129">For horizontal scroll bars, you can change the height of the bar and the width of the direction arrows.</span></span> <span data-ttu-id="c443c-130">También puede cambiar el color de fondo de las barras de desplazamiento horizontal y vertical.</span><span class="sxs-lookup"><span data-stu-id="c443c-130">You can also change the background color of both the horizontal and vertical scroll bars.</span></span>

<span data-ttu-id="c443c-131">[**FlatSB \_ SetScrollProp también**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) permite personalizar cómo se muestran las barras de desplazamiento planos.</span><span class="sxs-lookup"><span data-stu-id="c443c-131">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) also allows you to customize how the flat scroll bars are displayed.</span></span> <span data-ttu-id="c443c-132">Al cambiar las propiedades PROP VSTYLE de WSB y PROP HSTYLE de \_ WSB, puede establecer el tipo de barra de desplazamiento \_ \_ que desea \_ usar.</span><span class="sxs-lookup"><span data-stu-id="c443c-132">By changing the WSB\_PROP\_VSTYLE and WSB\_PROP\_HSTYLE properties, you can set the type of scroll bar that you want to use.</span></span> <span data-ttu-id="c443c-133">Hay tres estilos disponibles.</span><span class="sxs-lookup"><span data-stu-id="c443c-133">Three styles are available.</span></span>



|   <span data-ttu-id="c443c-134">Estilo</span><span class="sxs-lookup"><span data-stu-id="c443c-134">Style</span></span>                 |   <span data-ttu-id="c443c-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="c443c-135">Description</span></span>                                                                                                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c443c-136">MODO \_ FSB \_ ENCARTA</span><span class="sxs-lookup"><span data-stu-id="c443c-136">FSB\_ENCARTA\_MODE</span></span> | <span data-ttu-id="c443c-137">Se muestra una barra de desplazamiento plana estándar.</span><span class="sxs-lookup"><span data-stu-id="c443c-137">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="c443c-138">Cuando el mouse se mueve sobre un botón de dirección o el control de posición, esa parte de la barra de desplazamiento se mostrará en 3D.</span><span class="sxs-lookup"><span data-stu-id="c443c-138">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in 3-D.</span></span>             |
| <span data-ttu-id="c443c-139">MODO PLANO DE \_ \_ FSB</span><span class="sxs-lookup"><span data-stu-id="c443c-139">FSB\_FLAT\_MODE</span></span>    | <span data-ttu-id="c443c-140">Se muestra una barra de desplazamiento plana estándar.</span><span class="sxs-lookup"><span data-stu-id="c443c-140">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="c443c-141">Cuando el mouse se mueve sobre un botón de dirección o el control de posición, esa parte de la barra de desplazamiento se mostrará en colores invertidos.</span><span class="sxs-lookup"><span data-stu-id="c443c-141">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in inverted colors.</span></span> |
| <span data-ttu-id="c443c-142">MODO REGULAR DE \_ \_ FSB</span><span class="sxs-lookup"><span data-stu-id="c443c-142">FSB\_REGULAR\_MODE</span></span> | <span data-ttu-id="c443c-143">Se muestra una barra de desplazamiento normal y no inflada.</span><span class="sxs-lookup"><span data-stu-id="c443c-143">A normal, nonflat scroll bar is displayed.</span></span> <span data-ttu-id="c443c-144">No se aplicará ningún efecto visual especial.</span><span class="sxs-lookup"><span data-stu-id="c443c-144">No special visual effects will be applied.</span></span>                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a><span data-ttu-id="c443c-145">Quitar barras de desplazamiento planos</span><span class="sxs-lookup"><span data-stu-id="c443c-145">Removing Flat Scroll Bars</span></span>

<span data-ttu-id="c443c-146">Si desea quitar las barras de desplazamiento planos de la ventana, llame a la función [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) y pase el identificador a la ventana.</span><span class="sxs-lookup"><span data-stu-id="c443c-146">If you want to remove flat scroll bars from your window, call the [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) function, passing the handle to the window.</span></span> <span data-ttu-id="c443c-147">Esta función solo quita las barras de desplazamiento planas de la ventana en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="c443c-147">This function only removes flat scroll bars from your window at run time.</span></span> <span data-ttu-id="c443c-148">No es necesario llamar a esta función cuando se destruye la ventana.</span><span class="sxs-lookup"><span data-stu-id="c443c-148">You do not need to call this function when your window is destroyed.</span></span>

 

 