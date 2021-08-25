---
title: Barras de desplazamiento plano
description: Microsoft Internet Explorer 4.0 introdujo una nueva tecnología visual denominada barras de desplazamiento plano.
ms.assetid: f7e00e71-bf12-4db9-bb84-6d413b967049
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24a89479ffc5bae08ed08f5c3f0ca2ec9498ac781438708154ca503a2427ffc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799655"
---
# <a name="flat-scroll-bars"></a>Barras de desplazamiento plano

Microsoft Internet Explorer 4.0 introdujo una nueva tecnología visual denominada barras de desplazamiento plano. Funcionalmente, las barras de desplazamiento planos se comportan como las barras de desplazamiento estándar. La diferencia es que puede personalizar su apariencia en mayor medida que las barras de desplazamiento estándar.

En la ilustración siguiente se muestra una ventana que contiene una barra de desplazamiento plano.

![captura de pantalla de una ventana que contiene una barra de desplazamiento plano](images/flatsb.jpg)

> [!Note]  
> Las barras de desplazamiento plano son compatibles Comctl32.dll versiones 4.71 a 5.82. Comctl32.dll versiones 6.00 y posteriores no admiten barras de desplazamiento planas.

 

## <a name="using-flat-scroll-bars"></a>Uso de barras de desplazamiento planos

En esta sección se describe cómo implementar barras de desplazamiento plano en la aplicación.

### <a name="before-you-begin"></a>Antes de empezar

Para usar las funciones de barra de desplazamiento plano, debe incluir Commctrl.h en los archivos de código fuente y vincular con Comctl32.lib.

### <a name="adding-flat-scroll-bars-to-a-window"></a>Agregar barras de desplazamiento plano a una ventana

Para agregar barras de desplazamiento planas a una ventana, llame a [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb)y pase el identificador a la ventana. En lugar de usar las funciones de barra de desplazamiento estándar para manipular las barras de desplazamiento, debe usar la función XXX de FlatSB \_ equivalente. Hay funciones de barra de desplazamiento plano para establecer y recuperar la información de desplazamiento, el intervalo y la posición. Si no se han inicializado barras de desplazamiento planos para la ventana, la API de barra de desplazamiento plano se aplazará a las funciones estándar correspondientes, si se usa alguna. Esto le permite activar y desactivar las barras de desplazamiento sin tener que escribir código condicional.

Dado que una aplicación puede haber establecido métricas personalizadas para sus barras de desplazamiento plano, no se actualizan automáticamente cuando cambian las métricas del sistema. Cuando cambian las métricas de la barra de desplazamiento del sistema, se difunde un mensaje [**\_ WM SETTINGCHANGE,**](/windows/desktop/winmsg/wm-settingchange) con *su wParam* establecido en [**SPI \_ SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). Para actualizar las barras de desplazamiento planos a las nuevas métricas del sistema, las aplicaciones deben controlar este mensaje y cambiar explícitamente las propiedades dependientes de la métrica de la barra de desplazamiento plano.

Para actualizar las propiedades de la barra de desplazamiento, use [**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop). El fragmento de código siguiente cambia las propiedades dependientes de métricas de una barra de desplazamiento plano a los valores actuales del sistema.


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



### <a name="enhancing-flat-scroll-bars"></a>Mejorar las barras de desplazamiento planos

[**FlatSB \_ SetScrollProp permite**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) modificar las barras de desplazamiento plano para personalizar la apariencia de la ventana. Para las barras de desplazamiento verticales, puede cambiar el ancho de la barra y el alto de las flechas de dirección. Para las barras de desplazamiento horizontal, puede cambiar el alto de la barra y el ancho de las flechas de dirección. También puede cambiar el color de fondo de las barras de desplazamiento horizontal y vertical.

[**FlatSB \_ SetScrollProp también**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) permite personalizar cómo se muestran las barras de desplazamiento planos. Al cambiar las propiedades PROP VSTYLE de WSB y \_ \_ PROP HSTYLE de WSB, puede establecer el tipo de barra de desplazamiento \_ que desea \_ usar. Hay tres estilos disponibles.



|   Estilo                 |   Descripción                                                                                                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODO \_ FSB \_ ENCARTA | Se muestra una barra de desplazamiento plana estándar. Cuando el mouse se mueve sobre un botón de dirección o el control de posición, esa parte de la barra de desplazamiento se mostrará en 3D.             |
| MODO PLANO DE \_ \_ FSB    | Se muestra una barra de desplazamiento plana estándar. Cuando el mouse se mueve sobre un botón de dirección o el control de posición, esa parte de la barra de desplazamiento se mostrará en colores invertidos. |
| MODO REGULAR DE \_ \_ FSB | Se muestra una barra de desplazamiento normal y no inflada. No se aplicará ningún efecto visual especial.                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a>Quitar barras de desplazamiento planos

Si desea quitar las barras de desplazamiento planos de la ventana, llame a la función [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) y pase el identificador a la ventana. Esta función solo quita las barras de desplazamiento planos de la ventana en tiempo de ejecución. No es necesario llamar a esta función cuando se destruye la ventana.

 

 