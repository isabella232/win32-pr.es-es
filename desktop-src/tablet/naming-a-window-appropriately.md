---
description: Información general sobre cómo asignar un nombre adecuado a una ventana y establecer el título de la ventana para tablet PC.
ms.assetid: 9d064188-53a1-4cb5-b516-99610d7b8134
title: Asignar un nombre adecuado a una ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f2109568306e8817c518eecd8761ab00a2b1ecb8c54d4388b78e3eb456278d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883405"
---
# <a name="naming-a-window-appropriately"></a>Asignar un nombre adecuado a una ventana

Asigne a cada ventana un título descriptivo, incluso si la ventana o su título son invisibles. Esto permite que la funcionalidad de voz identifique la ventana y la jerarquía de ventanas. Esta recomendación se aplica a todas las ventanas: ventanas de nivel superior con marcos visibles; ventanas secundarias, como paletas flotantes; controles personalizados; barras de herramientas; y paneles dentro de una ventana, cuando se implementan como ventanas secundarias.

Hay tres maneras de establecer el título de la ventana:

-   Establezca la cadena en el script de recursos al llamar [**a CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o a funciones relacionadas.
-   Llame a [**la función SetWindowText.**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta)
-   Defina el nombre de los controles en los cuadros de diálogo mediante las técnicas descritas en [Controles de nomenclatura en cuadros de diálogo](naming-controls-in-dialog-boxes.md). Este es el único método para etiquetar un control de edición, ya que al establecer la etiqueta intrínseca de los controles se cambia el contenido de los controles.

Puede consultar el título mediante Microsoft Active Accessibility o el mensaje \_ GETTEXT de WM.

Para obtener más información sobre cómo consultar el título mediante Active Accessibility, vea la [sección Accesibilidad.](/windows/desktop/accessibility)

 

 
