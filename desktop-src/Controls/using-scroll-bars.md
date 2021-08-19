---
title: Usar barras de desplazamiento
description: Esta sección contiene temas que muestran cómo crear barras de desplazamiento.
ms.assetid: 45ffb56f-f567-40d7-8172-e64e26744ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96b1341e76b80e4ba5bf45df3dcfee03db87bb82adb4ba50273edbac6db4ac8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957594"
---
# <a name="using-scroll-bars"></a>Usar barras de desplazamiento

Esta sección contiene temas que muestran cómo crear barras de desplazamiento.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cómo crear barras de desplazamiento](create-scroll-bars.md)<br/>                                                                     | Al crear una ventana superpuesta, emergente o secundaria, puede agregar barras de desplazamiento estándar mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especificando WS \_ HSCROLL, WS VSCROLL o ambos \_ estilos. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Desplazamiento de texto](scroll-text-in-scroll-bars.md)<br/>                                                                    | En esta sección se describen los cambios que puede realizar en el procedimiento de ventana principal de una aplicación para permitir que un usuario desplácese por el texto. En el ejemplo de esta sección se crea y se muestra una matriz de cadenas de texto, y se procesa wm [**\_ HSCROLL**](wm-hscroll.md) y mensajes de barra de desplazamiento [**\_ VSCROLL de WM**](wm-vscroll.md) para que el usuario pueda desplazar el texto tanto vertical como horizontalmente. <br/>                                                                                                                                                                                                                                                                 |
| [Desplazamiento de un mapa de bits](scroll-a-bitmap-in-scroll-bars.md)<br/>                                                            | En esta sección se describen los cambios que puede realizar en el procedimiento de ventana principal de una aplicación para permitir al usuario desplazarse por un mapa de bits. <br/> El ejemplo incluye un elemento de menú que copia el contenido de la pantalla en un mapa de bits y muestra el mapa de bits en el área de cliente. El ejemplo también procesa los mensajes [**\_ WM HSCROLL**](wm-hscroll.md) y [**WM \_ VSCROLL**](wm-vscroll.md) generados por las barras de desplazamiento para que el usuario pueda desplazar el mapa de bits horizontal y verticalmente. A diferencia del ejemplo de texto de desplazamiento, el ejemplo de mapa de bits emplea la [**función BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) para dibujar la parte no válida del área de cliente. <br/> |
| [Cómo crear una interfaz de teclado para barras de desplazamiento estándar](create-a-keyboard-interface-for-standard-scroll-bars.md)<br/> | Aunque un control de barra de desplazamiento proporciona una interfaz de teclado integrada, una barra de desplazamiento estándar no lo hace. Para implementar una interfaz de teclado para una barra de desplazamiento estándar, un procedimiento de ventana debe procesar el mensaje [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) y examinar el código de clave virtual especificado por el *parámetro wParam.* Si el código de clave virtual corresponde a una tecla de flecha, el procedimiento de ventana se envía a sí mismo un mensaje [**\_ WM HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con la palabra de orden bajo del parámetro *wParam* establecida en el código de solicitud de barra de desplazamiento adecuado. <br/>                                              |



 

 

