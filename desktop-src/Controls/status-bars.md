---
title: Barras de estado (Windows controles)
description: Una barra de estado es una ventana horizontal en la parte inferior de una ventana primaria en la que una aplicación puede mostrar varios tipos de información de estado.
ms.assetid: vs|controls|~\controls\status\status.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2d1130b25cf0dc6373021e063210b765aa34a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167009"
---
# <a name="status-bars-windows-controls"></a>Barras de estado (Windows controles)

Una *barra de estado* es una ventana horizontal en la parte inferior de una ventana primaria en la que una aplicación puede mostrar varios tipos de información de estado. La barra de estado se puede dividir en partes para mostrar más de un tipo de información. En la siguiente captura de pantalla se muestra la barra de estado en microsoft Windows Paint aplicación. En este caso, la barra de estado contiene el texto "Para ayuda, haga clic en Temas de Ayuda en el menú Ayuda". La barra de estado es el área de la parte inferior de la ventana que contiene el texto de ayuda y la información de coordenadas.

![captura de pantalla de la aplicación de pintura, con una barra de estado que contiene sugerencias sobre la ayuda en línea](images/sb-paint.png)

Esta sección incluye los temas siguientes.

-   [Tipos y estilos](#types-and-styles)
-   [Tamaño y altura](#size-and-height)
-   [Barras de estado de varias partes](#multiple-part-status-bars)
-   [Operaciones de texto de la barra de estado](#status-bar-text-operations)
-   [Barras de estado dibujadas por el propietario](#owner-drawn-status-bars)
-   [Barras de estado de modo simple](#simple-mode-status-bars)
-   [Procesamiento de mensajes de la barra de estado predeterminada](#default-status-bar-message-processing)

## <a name="types-and-styles"></a>Tipos y estilos

La posición predeterminada de una barra de estado se encuentra en la parte inferior de la ventana primaria, pero puede especificar el estilo [**CCS \_ TOP**](common-control-styles.md) para que aparezca en la parte superior del área cliente de la ventana primaria.

Puede especificar el estilo [**SBARS \_ SIZEVOLUCIONP**](status-bar-styles.md) para incluir un control de tamaño en el extremo derecho de la barra de estado.

> [!Note]  
> No se recomienda [**combinar los estilos CCS \_ TOP**](common-control-styles.md) y [**SBARS \_ SIZEVOLUCIONP**](status-bar-styles.md) porque el control de tamaño resultante no es funcional.

 

## <a name="size-and-height"></a>Tamaño y altura

El procedimiento de ventana de la barra de estado establece automáticamente el tamaño inicial y la posición de la ventana, omitiendo los valores especificados en la [**función CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) El ancho es el mismo que el del área cliente de la ventana primaria. El alto se basa en las métricas de la fuente que está seleccionada actualmente en el contexto del dispositivo de la barra de estado y en el ancho de los bordes de la ventana.

El procedimiento de ventana ajusta automáticamente el tamaño de la barra de estado cada vez que recibe un [**mensaje \_ WM SIZE.**](/windows/desktop/winmsg/wm-size) Normalmente, cuando cambia el tamaño de la ventana primaria, el elemento primario envía un mensaje **WM \_ SIZE** a la barra de estado.

Una aplicación puede establecer el alto mínimo del área de dibujo de una barra de estado enviando a la ventana un mensaje [**SB \_ SETMINHEIGHT,**](sb-setminheight.md) especificando el alto mínimo, en píxeles. El área de dibujo no incluye los bordes de la ventana. Un alto mínimo es útil para dibujar en una barra de estado dibujada por el propietario. Para obtener más información, vea [Barras de estado dibujadas por el propietario](#owner-drawn-status-bars) más adelante en este capítulo.

Para recuperar los anchos de los bordes de una barra de estado, envíe a la ventana [**un mensaje \_ SB GETBORDERS.**](sb-getborders.md) El mensaje incluye la dirección de una matriz de tres elementos que recibe los anchos.

## <a name="multiple-part-status-bars"></a>Multiple-Part de estado

Una barra de estado puede tener muchas partes diferentes, cada una con una línea de texto diferente. Para dividir una barra de estado en partes, envíe a la ventana un mensaje [**SB \_ SETPARTS,**](sb-setparts.md) especificando el número de elementos que se crearán y la dirección de una matriz de enteros. La matriz contiene un elemento para cada parte y cada elemento especifica la coordenada de cliente del borde derecho de un elemento.

Una barra de estado puede tener un máximo de 256 partes, aunque las aplicaciones suelen usar mucho menos. Para recuperar un recuento de las partes de una barra de estado, así como la coordenada del borde derecho de cada parte, envíe a la ventana un [**mensaje \_ SB GETPARTS.**](sb-getparts.md)

## <a name="status-bar-text-operations"></a>Operaciones de texto de la barra de estado

El texto de cualquier parte de una barra de estado se establece enviando el mensaje [**\_ SB SETTEXT,**](sb-settext.md) especificando el índice de base cero de una parte, una dirección de la cadena que se va a dibujar en el elemento y la técnica para dibujar la cadena. La técnica de dibujo determina si el texto tiene un borde y, si lo hace, el estilo del borde. También determina si la ventana primaria es responsable de dibujar el texto. Para más información, consulte la sección [Barras de estado dibujadas por el](#owner-drawn-status-bars) propietario a continuación.

De forma predeterminada, el texto se alinea a la izquierda dentro de la parte especificada de una barra de estado. Puede insertar caracteres de tabulación (t) en el texto para centrarlo \\ o alinearlo a la derecha. El texto situado a la derecha de un solo carácter de tabulación se centra y el texto a la derecha de un segundo carácter de tabulación se alinea a la derecha.

Para recuperar texto de una barra de estado, use los [**mensajes \_ SB GETTEXTLENGTH**](sb-gettextlength.md) [**y SB \_ GETTEXT.**](sb-gettext.md)

Si la aplicación usa una barra de estado que solo tiene una parte, puede usar los mensajes [**WM \_ SETTEXT,**](/windows/desktop/winmsg/wm-settext) [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)y [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) para realizar operaciones de texto. Estos mensajes solo tratan con la parte que tiene un índice de cero, lo que le permite tratar la barra de estado de forma muy parecido a un control de texto estático.

Para mostrar una línea de estado sin crear una barra de estado, use la [**función DrawStatusText.**](/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta) La función usa las mismas técnicas para dibujar el estado como el procedimiento de ventana de la barra de estado, pero no establece automáticamente el tamaño y la posición de la información de estado. Al llamar a la función, debe especificar el tamaño y la posición de la información de estado, así como el contexto del dispositivo de la ventana en la que se va a dibujar.

## <a name="owner-drawn-status-bars"></a>Owner-Drawn de estado

Puede definir partes individuales de una barra de estado para que sean elementos dibujados por el propietario. El uso de esta técnica le proporciona más control del que tendría de lo contrario sobre la apariencia de la parte de la ventana. Por ejemplo, puede mostrar un mapa de bits en lugar de texto o dibujar texto con una fuente diferente.

Para definir un elemento de ventana como dibujado por el propietario, envíe el mensaje [**\_ SB SETTEXT**](sb-settext.md) a la barra de estado, especificando la parte y la técnica de dibujo SBT \_ OWNERDRAW. Cuando se especifica SBT OWNERDRAW, el parámetro lParam es un valor definido por la aplicación de 32 bits que la aplicación puede usar al \_ dibujar el elemento.  Por ejemplo, puede especificar un identificador de fuente, un identificador de mapa de bits, una dirección de una cadena, y así sucesivamente.

Cuando una barra de estado necesita dibujar una parte dibujada por el propietario, envía el [**mensaje \_ DRAWITEM de WM**](wm-drawitem.md) a la ventana primaria. El *parámetro wParam* del mensaje es el identificador de ventana secundaria de la barra de estado y el parámetro *lParam* es la dirección de una [**estructura DRAWITEMSTRUCT.**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) La ventana primaria usa la información de la estructura para dibujar el elemento. Para una parte dibujada por el propietario de una barra de estado, **DRAWITEMSTRUCT** contiene la siguiente información.



| Miembro         | Descripción                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| **CtlType**    | Sin definir; no se usan.                                                                                                 |
| **CtlID**      | Identificador de ventana secundaria de la barra de estado.                                                                             |
| **Itemid**     | Índice de base cero del elemento que se va a dibujar.                                                                              |
| **itemAction** | Sin definir; no se usan.                                                                                                 |
| **itemState**  | Sin definir; no se usan.                                                                                                 |
| **hwndItem**   | Identificador de la barra de estado.                                                                                              |
| **Hdc**        | Controlar el contexto del dispositivo de la barra de estado.                                                                        |
| **rcItem**     | Coordenadas de la parte de ventana que se va a dibujar. Las coordenadas son relativas a la esquina superior izquierda de la barra de estado.   |
| **itemData**   | Valor de 32 bits definido por la aplicación especificado en el parámetro *lParam* del [**mensaje SB \_ SETTEXT.**](sb-settext.md) |



 

## <a name="simple-mode-status-bars"></a>Barras de estado de modo simple

Para colocar una barra de estado en "modo simple", envíele un [**mensaje \_ SB SIMPLE.**](sb-simple.md) Una barra de estado de modo simple muestra solo una parte. Cuando se establece el texto de la ventana, la ventana se invalida, pero no se vuelve a dibujar hasta el [**siguiente WM \_ PAINT**](/windows/desktop/gdi/wm-paint). La espera del mensaje reduce el parpadeo de la pantalla al minimizar el número de veces que se vuelve a dibujar la ventana. Una barra de estado de modo simple es útil para mostrar texto de Ayuda para los elementos de menú mientras el usuario se desplaza por el menú.

La cadena que muestra una barra de estado mientras está en modo simple se mantiene por separado de las cadenas que muestra mientras está en modo no sencillo. Esto significa que puede poner la ventana en modo simple, establecer su texto y volver al modo no sencillo sin cambiar el texto del modo no sencillo.

Al establecer el texto de una barra de estado de modo simple, puede especificar cualquier técnica de dibujo excepto SBT \_ OWNERDRAW. Una barra de estado de modo simple no admite el dibujo de propietario.

## <a name="default-status-bar-message-processing"></a>Procesamiento de mensajes de la barra de estado predeterminada

En esta sección se describen los mensajes que controla el procedimiento de ventana para la clase [**STATUSCLASSNAME**](common-control-window-classes.md) predefinida.



| Message               | Procesamiento predeterminado                                                                                                                                                                                                                                                       |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WM \_ CREATE**        | Inicializa la barra de estado.                                                                                                                                                                                                                                              |
| **WM \_ DESTROY**       | Libera los recursos asignados para la barra de estado.                                                                                                                                                                                                                            |
| **WM \_ GETFONT**       | Devuelve el identificador a la fuente actual con la que la barra de estado dibuja su texto.                                                                                                                                                                                         |
| **WM \_ GETTEXT**       | Copia el texto de la primera parte de una barra de estado en un búfer. Devuelve un valor de 32 bits que especifica la longitud, en caracteres, del texto y la técnica utilizada para dibujar el texto.                                                                                |
| **WM \_ GETTEXTLENGTH** | Devuelve un valor de 32 bits que especifica la longitud, en caracteres, del texto de la primera parte de una barra de estado y la técnica utilizada para dibujar el texto.                                                                                                                  |
| **WM \_ NCHITTEST**     | Devuelve el valor HTBOTTOMRIGHT si el cursor del mouse está en el control de tamaño, lo que hace que el sistema muestre el cursor de tamaño. Si el cursor del mouse no está en el control de tamaño, la barra de estado pasa este mensaje a la [**función DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) |
| **WM \_ PAINT**         | Pinta la región no válida de la barra de estado. Si el *parámetro wParam* no es **NULL,** el control asume que el valor es un HDC y pinta con ese contexto de dispositivo.                                                                                               |
| **WM \_ SETFONT**       | Selecciona el identificador de fuente en el contexto del dispositivo para la barra de estado.                                                                                                                                                                                                      |
| **WM \_ SETTEXT**       | Copia el texto especificado en la primera parte de una barra de estado mediante la operación de dibujo predeterminada (especificada como cero). Devuelve **TRUE si se** realiza correctamente o **FALSE** en caso contrario.                                                                                       |
| **TAMAÑO \_ WM**          | Cambia el tamaño de la barra de estado según el ancho actual del área de cliente de la ventana primaria y el alto de la fuente actual de la barra de estado.                                                                                                                               |



 

 

 
