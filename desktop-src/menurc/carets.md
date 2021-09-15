---
title: Carets
description: En esta sección se de abordan los caretas que parpadean en líneas, bloques o mapas de bits en el área cliente de una ventana.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\carets.htm
keywords:
- resources,carets
- carets,about
- líneas parpadeando
- bloques de parpadeo
- mapas de bits parpadeantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cb99dfc324aa039924fa26683ab0a7674706ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359726"
---
# <a name="carets"></a>Carets

Un *elemento de referencia* es una línea, un bloque o un mapa de bits parpadeante en el área cliente de una ventana. Normalmente, el símbolo de inserción indica el lugar en el que se insertará texto o gráficos.

En la ilustración siguiente se muestran algunas variaciones comunes en la apariencia del careta.

![Muestra cinco formas diferentes en las que puede aparecer un caret.](images/cscrt-01.png)

Las aplicaciones pueden crear un caret, cambiar su hora de parpadeo y mostrar, ocultar o reubicar el caret.

### <a name="in-this-section"></a>En esta sección



| Nombre                                   | Descripción                                                               |
|----------------------------------------|---------------------------------------------------------------------------|
| [Acerca de los carets](about-carets.md)       | Describe los carets.<br/>                                              |
| [Uso de los carets](using-carets.md)       | Ejemplos de código que muestran cómo realizar tareas relacionadas con los caret.<br/> |
| [Referencia de caret](caret-reference.md) | Contiene la referencia de API.<br/>                                    |



 

### <a name="caret-functions"></a>Funciones de caret



| Nombre                                           | Descripción                                                                                                                                                                                                                                                   |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret)             | Crea una nueva forma para el caret del sistema y asigna la propiedad del caret a la ventana especificada. La forma del centro de referencia puede ser una línea, un bloque o un mapa de bits. <br/>                                                                                         |
| [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret)           | Destruye la forma actual del caret, libera el caret de la ventana y quita el caret de la pantalla. <br/>                                                                                                                                       |
| [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) | Recupera el tiempo necesario para invertir los píxeles del caret. El usuario puede establecer este valor. <br/>                                                                                                                                                            |
| [**GetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos)             | Copia la posición del cursor de inserción en la estructura [**POINT**](/previous-versions//dd162805(v=vs.85)) especificada. <br/>                                                                                                                                                                    |
| [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret)                 | Quita el caret de la pantalla. Ocultar un objeto de inserción no destruye su forma actual ni invalida el punto de inserción. <br/>                                                                                                                           |
| [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) | Establece el tiempo de parpadeo del cursor de cursor en el número especificado de milisegundos. El tiempo de parpadeo es el tiempo transcurrido, en milisegundos, necesario para invertir los píxeles del cursor de subrayado. <br/>                                                                                    |
| [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos)             | Mueve el elemento de subrayado a las coordenadas especificadas. Si la ventana propietaria del caret se creó con el estilo de clase **\_ OWNDC de CS,** las coordenadas especificadas están sujetas al modo de asignación del contexto de dispositivo asociado a esa ventana. <br/> |
| [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret)                 | Hace que el caret sea visible en la pantalla en la posición actual del cursor de la pantalla. Cuando el signo de asignación se vuelve visible, comienza a parpadear automáticamente. <br/>                                                                                                          |



 

 

