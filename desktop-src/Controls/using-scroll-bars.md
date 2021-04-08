---
title: Usar barras de desplazamiento
description: Esta sección contiene temas que muestran cómo crear barras de desplazamiento.
ms.assetid: 45ffb56f-f567-40d7-8172-e64e26744ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d602426bd5f716a380d43104046f330d3240d516
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078462"
---
# <a name="using-scroll-bars"></a>Usar barras de desplazamiento

Esta sección contiene temas que muestran cómo crear barras de desplazamiento.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cómo crear barras de desplazamiento](create-scroll-bars.md)<br/>                                                                     | Al crear una ventana superpuesta, emergente o secundaria, puede Agregar barras de desplazamiento estándar mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especificando WS \_ HSCROLL, WS \_ VSCROLL o ambos estilos. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Cómo desplazarse por el texto](scroll-text-in-scroll-bars.md)<br/>                                                                    | En esta sección se describen los cambios que puede realizar en el procedimiento de ventana principal de una aplicación para permitir a los usuarios desplazarse por el texto. En el ejemplo de esta sección se crea y se muestra una matriz de cadenas de texto y se procesan los mensajes de la barra de desplazamiento [**\_ HSCROLL**](wm-hscroll.md) y [**WM \_ VSCROLL**](wm-vscroll.md) para que el usuario pueda desplazarse por el texto vertical y horizontalmente. <br/>                                                                                                                                                                                                                                                                 |
| [Cómo desplazarse por un mapa de bits](scroll-a-bitmap-in-scroll-bars.md)<br/>                                                            | En esta sección se describen los cambios que puede realizar en el procedimiento de ventana principal de una aplicación para permitir al usuario desplazarse por un mapa de bits. <br/> En el ejemplo se incluye un elemento de menú que copia el contenido de la pantalla en un mapa de bits y muestra el mapa de bits en el área cliente. En el ejemplo también se procesan los mensajes de [**WM \_ HSCROLL**](wm-hscroll.md) y [**WM \_ VSCROLL**](wm-vscroll.md) generados por las barras de desplazamiento para que el usuario pueda desplazarse por el mapa de bits horizontal y verticalmente. A diferencia del ejemplo de texto desplazado, el ejemplo de mapa de bits emplea la función [**bitblt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) para dibujar la parte no válida del área cliente. <br/> |
| [Cómo crear una interfaz de teclado para las barras de desplazamiento estándar](create-a-keyboard-interface-for-standard-scroll-bars.md)<br/> | Aunque un control de barra de desplazamiento proporciona una interfaz de teclado integrada, no existe una barra de desplazamiento estándar. Para implementar una interfaz de teclado para una barra de desplazamiento estándar, un procedimiento de ventana debe procesar el mensaje de [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) y examinar el código de la clave virtual especificado por el parámetro *wParam* . Si el código de la clave virtual corresponde a una tecla de dirección, el procedimiento de ventana se envía a sí mismo un mensaje de [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con la palabra de orden inferior del parámetro *wParam* establecida en el código de solicitud de la barra de desplazamiento correspondiente. <br/>                                              |



 

 

