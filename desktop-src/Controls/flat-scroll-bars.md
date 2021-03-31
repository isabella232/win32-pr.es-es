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
# <a name="flat-scroll-bars"></a>Barras de desplazamiento plana

Microsoft Internet Explorer 4,0 presentó una nueva tecnología visual denominada barras de desplazamiento plana. Funcionalmente, las barras de desplazamiento sin formato se comportan igual que las barras de desplazamiento estándar. La diferencia es que puede personalizar su apariencia en una extensión mayor que las barras de desplazamiento estándar.

En la ilustración siguiente se muestra una ventana que contiene una barra de desplazamiento plana.

![captura de pantalla de una ventana que contiene una barra de desplazamiento plana](images/flatsb.jpg)

> [!Note]  
> Las barras de desplazamiento plana son compatibles con las versiones de Comctl32.dll 4,71 a 5,82. Comctl32.dll versiones 6,00 y posteriores no admiten barras de desplazamiento sin formato.

 

## <a name="using-flat-scroll-bars"></a>Usar barras de desplazamiento plana

En esta sección se describe cómo implementar barras de desplazamiento sin formato en la aplicación.

### <a name="before-you-begin"></a>Antes de empezar

Para usar las funciones de barra de desplazamiento plana, debe incluir commctrl. h en los archivos de código fuente y vincular con COMCTL32. lib.

### <a name="adding-flat-scroll-bars-to-a-window"></a>Agregar barras de desplazamiento sin formato a una ventana

Para agregar barras de desplazamiento plana a una ventana, llame a [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), pasando el identificador a la ventana. En lugar de usar las funciones de barra de desplazamiento estándar para manipular las barras de desplazamiento, debe usar la función equivalente FlatSB \_ xxx. Hay funciones de barra de desplazamiento plana para establecer y recuperar la información de desplazamiento, el intervalo y la posición. Si las barras de desplazamiento sin formato no se han inicializado para la ventana, la API de la barra de desplazamiento plana diferirá a las funciones estándar correspondientes, en caso de que se use alguna. Esto le permite activar y desactivar las barras de desplazamiento sin necesidad de escribir código condicional.

Dado que una aplicación puede haber establecido métricas personalizadas para sus barras de desplazamiento sin formato, no se actualizan automáticamente cuando se modifican las métricas del sistema. Cuando cambian las métricas de la barra de desplazamiento del sistema, se emite un mensaje de [**\_ SETTINGCHANGE de WM**](/windows/desktop/winmsg/wm-settingchange) , con el valor de *wParam* establecido en [**SPI \_ SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). Para actualizar las barras de desplazamiento plana a las nuevas métricas del sistema, las aplicaciones deben controlar este mensaje y cambiar explícitamente las propiedades dependientes de las métricas de la barra de desplazamiento plana.

Para actualizar las propiedades de la barra de desplazamiento, utilice [**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop). El siguiente fragmento de código cambia las propiedades dependientes de las métricas de una barra de desplazamiento sin formato a los valores actuales del sistema.


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



### <a name="enhancing-flat-scroll-bars"></a>Mejorar las barras de desplazamiento plana

[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) le permite modificar las barras de desplazamiento plana para personalizar la apariencia de la ventana. En el caso de las barras de desplazamiento verticales, puede cambiar el ancho de la barra y el alto de las flechas de dirección. En el caso de las barras de desplazamiento horizontal, puede cambiar el alto de la barra y el ancho de las flechas de dirección. También puede cambiar el color de fondo de las barras de desplazamiento horizontal y vertical.

[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) también le permite personalizar cómo se muestran las barras de desplazamiento sin formato. Mediante el cambio de las propiedades de la \_ \_ propiedad VSTYLE y la \_ propiedad HSTYLE de la propiedad WSB \_ , puede establecer el tipo de barra de desplazamiento que desea utilizar. Hay tres estilos disponibles.



|                    |                                                                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_modo Encarta de FSB \_ | Se muestra una barra de desplazamiento estándar. Cuando el mouse se mueve sobre un botón de dirección o el control de posición, esa parte de la barra de desplazamiento se mostrará en 3D.             |
| \_modo plano de FSB \_    | Se muestra una barra de desplazamiento estándar. Cuando el mouse se mueve sobre un botón de dirección o el control de posición, esa parte de la barra de desplazamiento se mostrará en los colores invertidos. |
| \_modo normal de FSB \_ | Se muestra una barra de desplazamiento normal y no plana. No se aplicarán efectos visuales especiales.                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a>Quitar barras de desplazamiento plana

Si desea quitar las barras de desplazamiento plana de la ventana, llame a la función [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) , pasando el identificador a la ventana. Esta función solo quita las barras de desplazamiento sin formato de la ventana en tiempo de ejecución. No es necesario llamar a esta función cuando se destruye la ventana.

 

 