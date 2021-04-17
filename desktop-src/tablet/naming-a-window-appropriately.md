---
description: Información general sobre cómo asignar un nombre a una ventana de forma adecuada y establecer el título de la ventana para Tablet PC.
ms.assetid: 9d064188-53a1-4cb5-b516-99610d7b8134
title: Asignar un nombre adecuado a una ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaee320f621acf834d7c0ec5978a9e42f0811e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659931"
---
# <a name="naming-a-window-appropriately"></a>Asignar un nombre adecuado a una ventana

Asigne a cada ventana un título descriptivo, incluso si la ventana o su título es invisible. Esto permite que la funcionalidad de voz identifique la ventana y la jerarquía de ventanas. Esta recomendación se aplica a todas las ventanas: ventanas de nivel superior con fotogramas visibles; ventanas secundarias, como las paletas flotantes; controles personalizados; barras los paneles y dentro de una ventana, cuando se implementan como ventanas secundarias.

Hay tres maneras de establecer el título de la ventana:

-   Establezca la cadena en el script de recursos cuando llame a [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o a funciones relacionadas.
-   Llame a la función [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) .
-   Defina el nombre de los controles en los cuadros de diálogo mediante las técnicas descritas en [nombrar controles en los cuadros de diálogo](naming-controls-in-dialog-boxes.md). Este es el único método para etiquetar un control de edición, ya que el establecimiento de la etiqueta intrínseca Controls cambia el contenido de los controles.

Puede consultar el título mediante Microsoft Active Accessibility o el mensaje de GETTEXT de WM \_ .

Para obtener más información sobre cómo consultar el título mediante Active Accessibility, vea la sección [accesibilidad](/windows/desktop/accessibility) .

 

 
