---
title: Barras de estado (controles de Windows)
description: Una barra de estado es una ventana horizontal situada en la parte inferior de una ventana primaria en la que una aplicación puede mostrar diversos tipos de información de estado.
ms.assetid: vs|controls|~\controls\status\status.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2d1130b25cf0dc6373021e063210b765aa34a5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105656451"
---
# <a name="status-bars-windows-controls"></a>Barras de estado (controles de Windows)

Una *barra de estado* es una ventana horizontal situada en la parte inferior de una ventana primaria en la que una aplicación puede mostrar diversos tipos de información de estado. La barra de estado se puede dividir en partes para mostrar más de un tipo de información. En la captura de pantalla siguiente se muestra la barra de estado de la aplicación Paint de Microsoft Windows. En este caso, la barra de estado contiene el texto "para obtener ayuda, haga clic en temas de ayuda en el menú Ayuda". La barra de estado es el área de la parte inferior de la ventana que contiene el texto de ayuda y la información de coordenadas.

![captura de pantalla de la aplicación Paint, con una barra de estado que contiene sugerencias sobre la ayuda en línea](images/sb-paint.png)

Esta sección incluye los temas siguientes.

-   [Tipos y estilos](#types-and-styles)
-   [Tamaño y alto](#size-and-height)
-   [Barras de estado de varias partes](#multiple-part-status-bars)
-   [Operaciones de texto de la barra de estado](#status-bar-text-operations)
-   [Barras de estado dibujadas por el propietario](#owner-drawn-status-bars)
-   [Barras de estado de modo simple](#simple-mode-status-bars)
-   [Procesamiento de mensajes de la barra de estado predeterminada](#default-status-bar-message-processing)

## <a name="types-and-styles"></a>Tipos y estilos

La posición predeterminada de una barra de estado está a lo largo de la parte inferior de la ventana primaria, pero puede especificar el estilo de [**CCS \_ superior**](common-control-styles.md) para que aparezca en la parte superior del área de cliente de la ventana primaria.

Puede especificar el estilo [**de \_ SIZEGRIP de SBARS**](status-bar-styles.md) para incluir un control de tamaño en el extremo derecho de la barra de estado.

> [!Note]  
> No se recomienda combinar los estilos [**CCS \_ Top**](common-control-styles.md) y [**SBARS \_ SIZEGRIP**](status-bar-styles.md) porque el control de tamaño resultante no es funcional.

 

## <a name="size-and-height"></a>Tamaño y alto

El procedimiento de ventana de la barra de Estado establece automáticamente el tamaño inicial y la posición de la ventana, omitiendo los valores especificados en la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . El ancho es el mismo que el del área de cliente de la ventana primaria. El alto se basa en las métricas de la fuente seleccionada actualmente en el contexto de dispositivo de la barra de estado y en el ancho de los bordes de la ventana.

El procedimiento de ventana ajusta automáticamente el tamaño de la barra de estado cada vez que recibe un mensaje de [**\_ tamaño de WM**](/windows/desktop/winmsg/wm-size) . Normalmente, cuando cambia el tamaño de la ventana primaria, el elemento primario envía un mensaje de **\_ tamaño de WM** a la barra de estado.

Una aplicación puede establecer el alto mínimo del área de dibujo de una barra de estado mediante el envío de la ventana de un mensaje [**\_ SETMINHEIGHT de SB**](sb-setminheight.md) , especificando el alto mínimo, en píxeles. El área de dibujo no incluye los bordes de la ventana. Un alto mínimo es útil para dibujar en una barra de estado dibujada por el propietario. Para obtener más información, vea [barras de estado dibujadas por el propietario](#owner-drawn-status-bars) más adelante en este capítulo.

Para recuperar el ancho de los bordes de una barra de estado, envíe la ventana a un mensaje [**\_ GETBORDERS de SB**](sb-getborders.md) . El mensaje incluye la dirección de una matriz de tres elementos que recibe los anchos.

## <a name="multiple-part-status-bars"></a>Multiple-Part barras de estado

Una barra de estado puede tener muchas partes diferentes, cada una de las cuales muestra una línea de texto diferente. Divida una barra de estado en partes mediante el envío de la ventana de un mensaje [**\_ SETPARTS de SB**](sb-setparts.md) , especificando el número de elementos que se van a crear y la dirección de una matriz de enteros. La matriz contiene un elemento para cada elemento y cada elemento especifica la coordenada del cliente del borde derecho de una parte.

Una barra de estado puede tener un máximo de 256 partes, aunque las aplicaciones suelen usar muchos menos. Para recuperar un recuento de los elementos de una barra de estado, así como la coordenada del borde derecho de cada parte, envíe la ventana a un mensaje [**\_ GETPARTS de SB**](sb-getparts.md) .

## <a name="status-bar-text-operations"></a>Operaciones de texto de la barra de estado

El texto de cualquier parte de una barra de estado se establece mediante el envío del mensaje [**\_ SETTEXT de SB**](sb-settext.md) , que especifica el índice de base cero de un elemento, una dirección de la cadena que se va a dibujar en la parte y la técnica para dibujar la cadena. La técnica de dibujo determina si el texto tiene un borde y, si es así, el estilo del borde. También determina si la ventana primaria es responsable de dibujar el texto. Para obtener más información, vea la sección [barras de estado dibujadas](#owner-drawn-status-bars) por el propietario más adelante.

De forma predeterminada, el texto se alinea a la izquierda en la parte especificada de una barra de estado. Puede insertar caracteres de tabulación ( \\ t) en el texto para centrar o alinear a la derecha. El texto situado a la derecha de un carácter de tabulación se centra y el texto situado a la derecha de un segundo carácter de tabulación se alinea a la derecha.

Para recuperar texto de una barra de estado, use los mensajes [**\_ GETTEXTLENGTH**](sb-gettextlength.md) y [**\_ GETTEXT**](sb-gettext.md) de SB.

Si la aplicación usa una barra de estado que solo tiene una parte, puede usar los mensajes [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext), [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)y [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) para realizar operaciones de texto. Estos mensajes solo tratan con el elemento que tiene un índice de cero, lo que le permite tratar la barra de estado de forma similar a un control de texto estático.

Para mostrar una línea de estado sin crear una barra de estado, utilice la función [**DrawStatusText**](/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta) . La función utiliza las mismas técnicas para dibujar el estado como el procedimiento de ventana de la barra de estado, pero no establece automáticamente el tamaño y la posición de la información de estado. Al llamar a la función, debe especificar el tamaño y la posición de la información de estado, así como el contexto de dispositivo de la ventana en la que se va a dibujar.

## <a name="owner-drawn-status-bars"></a>Owner-Drawn barras de estado

Puede definir partes individuales de una barra de estado como elementos dibujados por el propietario. El uso de esta técnica le proporciona más control de lo que tendría en el aspecto de la parte de la ventana. Por ejemplo, puede mostrar un mapa de bits en lugar de texto o dibujar texto con una fuente diferente.

Para definir una parte de la ventana como dibujada por el propietario, envíe el mensaje [**\_ SETTEXT de SB**](sb-settext.md) a la barra de estado, especificando la parte y la \_ técnica de dibujo de OWNERDRAW SBT. Cuando \_ se especifica SBT OWNERDRAW, el parámetro *lParam* es un valor definido por la aplicación de 32 bits que la aplicación puede usar al dibujar el elemento. Por ejemplo, puede especificar un identificador de fuente, un identificador de mapa de bits, una dirección de una cadena, etc.

Cuando una barra de estado necesita dibujar un elemento dibujado por el propietario, envía el mensaje de la ventana de Windows de [**WM \_**](wm-drawitem.md) a la ventana primaria. El parámetro *wParam* del mensaje es el identificador de la ventana secundaria de la barra de estado y el parámetro *lParam* es la dirección de una estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) . La ventana primaria usa la información de la estructura para dibujar el elemento. En el caso de una parte dibujada por el propietario de una barra de estado, **drawitemstruct (** contiene la siguiente información.



| Miembro         | Descripción                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| **CtlType**    | Indefinido No use.                                                                                                 |
| **CtlID**      | Identificador de la ventana secundaria de la barra de estado.                                                                             |
| **ID**     | Índice de base cero del elemento que se va a dibujar.                                                                              |
| **Del itemaction** | Indefinido No use.                                                                                                 |
| **itemState**  | Indefinido No use.                                                                                                 |
| **hwndItem**   | Identificador de la barra de estado.                                                                                              |
| **Cámaras**        | Identificador del contexto de dispositivo de la barra de estado.                                                                        |
| **rcItem**     | Coordenadas de la parte de la ventana que se va a dibujar. Las coordenadas son relativas a la esquina superior izquierda de la barra de estado.   |
| **itemData**   | Valor de 32 bits definido por la aplicación especificado en el parámetro *lParam* del mensaje de [**\_ SETTEXT de SB**](sb-settext.md) . |



 

## <a name="simple-mode-status-bars"></a>Barras de estado de modo simple

Se coloca una barra de estado en "modo simple" mediante el envío de un mensaje [**\_ simple de SB**](sb-simple.md) . Una barra de estado de modo simple muestra solo una parte. Cuando se establece el texto de la ventana, se invalida la ventana, pero no se vuelve a dibujar hasta la siguiente [**\_ pintura de WM**](/windows/desktop/gdi/wm-paint). La espera del mensaje reduce el parpadeo de la pantalla al minimizar el número de veces que se vuelve a dibujar la ventana. Una barra de estado de modo simple es útil para mostrar el texto de ayuda de los elementos de menú mientras el usuario se desplaza por el menú.

La cadena que muestra una barra de estado en modo simple se mantiene de forma independiente de las cadenas que muestra mientras se encuentra en modo no simple. Esto significa que puede colocar la ventana en modo simple, establecer su texto y volver a cambiar al modo no simple sin cambiar el texto del modo no simple.

Al establecer el texto de una barra de estado de modo simple, puede especificar cualquier técnica de dibujo excepto SBT \_ OWNERDRAW. Una barra de estado de modo simple no admite el dibujo del propietario.

## <a name="default-status-bar-message-processing"></a>Procesamiento de mensajes de la barra de estado predeterminada

En esta sección se describen los mensajes administrados por el procedimiento de ventana para la clase [**STATUSCLASSNAME**](common-control-window-classes.md) predefinida.



| Message               | Procesamiento predeterminado                                                                                                                                                                                                                                                       |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **creación de WM \_**        | Inicializa la barra de estado.                                                                                                                                                                                                                                              |
| **destrucción de WM \_**       | Libera los recursos asignados para la barra de estado.                                                                                                                                                                                                                            |
| **GETFONT de WM \_**       | Devuelve el identificador de la fuente actual con la que la barra de estado dibuja su texto.                                                                                                                                                                                         |
| **GETTEXT de WM \_**       | Copia el texto de la primera parte de una barra de estado en un búfer. Devuelve un valor de 32 bits que especifica la longitud, en caracteres, del texto y la técnica que se usa para dibujar el texto.                                                                                |
| **GETTEXTLENGTH de WM \_** | Devuelve un valor de 32 bits que especifica la longitud, en caracteres, del texto en la primera parte de una barra de estado y la técnica que se usa para dibujar el texto.                                                                                                                  |
| **NCHITTEST de WM \_**     | Devuelve el valor de HTBOTTOMRIGHT si el cursor del mouse está en el control de tamaño, lo que hace que el sistema muestre el cursor de ajuste de tamaño. Si el cursor del mouse no está en el control de tamaño, la barra de estado pasa este mensaje a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . |
| **pintura de WM \_**         | Pinta la región no válida de la barra de estado. Si el parámetro *wParam* no es **null**, el control supone que el valor es HDC y pinta usando ese contexto de dispositivo.                                                                                               |
| **WM \_**       | Selecciona el identificador de fuente en el contexto de dispositivo para la barra de estado.                                                                                                                                                                                                      |
| **SETTEXT de WM \_**       | Copia el texto especificado en la primera parte de una barra de estado, usando la operación de dibujo predeterminada (especificada como cero). Devuelve **true** si es correcto, o **false** en caso contrario.                                                                                       |
| **tamaño de WM \_**          | Cambia el tamaño de la barra de estado en función del ancho actual del área de cliente de la ventana primaria y del alto de la fuente actual de la barra de estado.                                                                                                                               |



 

 

 
