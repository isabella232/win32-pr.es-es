---
title: Carets
description: En esta sección se de abordan los mapas de bits, bloques o líneas parpadeantes en el área cliente de una ventana.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\carets.htm
keywords:
- resources,carets
- carets,about
- líneas parpadeando
- bloques parpadeando
- mapas de bits parpadeantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed77a9d7fe315f5cef1be501c6392cce5fcfc3e79c5994f197a9fe6e254d8f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734865"
---
# <a name="carets"></a>Carets

Un *elemento de referencia* es una línea, un bloque o un mapa de bits parpadeante en el área cliente de una ventana. El símbolo de inserción suele indicar el lugar en el que se insertará texto o gráficos.

En la ilustración siguiente se muestran algunas variaciones comunes en la apariencia del centro de atención.

![Muestra cinco formas diferentes en las que puede aparecer un centro de diálogo.](images/cscrt-01.png)

Las aplicaciones pueden crear un centro de atención, cambiar su hora de parpadeo y mostrar, ocultar o reubicar el cursor de cursor.

### <a name="in-this-section"></a>En esta sección



| Nombre                                   | Descripción                                                               |
|----------------------------------------|---------------------------------------------------------------------------|
| [Acerca de los carets](about-carets.md)       | Describe los sesos.<br/>                                              |
| [Uso de carets](using-carets.md)       | Ejemplos de código que muestran cómo realizar tareas relacionadas con los elementos de búsqueda.<br/> |
| [Referencia de caret](caret-reference.md) | Contiene la referencia de API.<br/>                                    |



 

### <a name="caret-functions"></a>Funciones de caret



| Nombre                                           | Descripción                                                                                                                                                                                                                                                   |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret)             | Crea una nueva forma para el elemento de asignación del sistema y asigna la propiedad del elemento de asignación a la ventana especificada. La forma del centro de referencia puede ser una línea, un bloque o un mapa de bits. <br/>                                                                                         |
| [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret)           | Destruye la forma actual del centro de diálogo, libera el centro de diálogo de la ventana y lo quita de la pantalla. <br/>                                                                                                                                       |
| [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) | Recupera el tiempo necesario para invertir los píxeles del centro de atención. El usuario puede establecer este valor. <br/>                                                                                                                                                            |
| [**GetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos)             | Copia la posición del elemento de inserción en la estructura [**POINT**](/previous-versions//dd162805(v=vs.85)) especificada. <br/>                                                                                                                                                                    |
| [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret)                 | Quita el centro de atención de la pantalla. Ocultar un objeto de inserción no destruye su forma actual ni invalida el punto de inserción. <br/>                                                                                                                           |
| [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) | Establece el tiempo de parpadeo del cursor de referencia en el número especificado de milisegundos. El tiempo de parpadeo es el tiempo transcurrido, en milisegundos, necesario para invertir los píxeles del cursor de subrayado. <br/>                                                                                    |
| [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos)             | Mueve el elemento de subrayado a las coordenadas especificadas. Si la ventana propietaria del elemento de asignación se creó con el estilo de clase **\_ OWNDC de CS,** las coordenadas especificadas están sujetas al modo de asignación del contexto de dispositivo asociado a esa ventana. <br/> |
| [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret)                 | Hace que el signo de cursor sea visible en la pantalla en la posición actual del centro de atención. Cuando el signo de asignación se vuelve visible, comienza a parpadear automáticamente. <br/>                                                                                                          |



 

 

