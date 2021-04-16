---
description: Al usar cuadros de diálogo de Microsoft Windows, debe etiquetar todos los controles para facilitar la funcionalidad de voz. El siguiente cuadro de diálogo de ejecución muestra una etiqueta de control de texto estático para un cuadro de lista desplegable. El texto estático termina con un signo de dos puntos.
ms.assetid: 3b01a4d2-9deb-413f-bab8-566df86b6af9
title: Asignar nombres a controles en cuadros de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0f74ecb3737b422450388ee87ab4177e899aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104570697"
---
# <a name="naming-controls-in-dialog-boxes"></a>Asignar nombres a controles en cuadros de diálogo

Al usar cuadros de diálogo de Microsoft Windows, debe etiquetar todos los controles para facilitar la funcionalidad de voz. El siguiente cuadro de diálogo de **ejecución** muestra una etiqueta de control de texto estático para un cuadro de lista desplegable. El texto estático termina con un signo de dos puntos.

![captura de pantalla que muestra el cuadro de diálogo Ejecutar](images/fb0bd076-e9f9-4260-a54a-9d7db93157da.jpg)

Existen dos tipos de controles:

-   Controles que tienen sus títulos como propiedad de ese control, como botones de comando y casillas. Las ayudas de accesibilidad no tienen ningún problema al identificar estos controles, siempre que el título esté definido correctamente.
-   Los controles que no tienen sus propios títulos, como controles de edición, cuadros de lista y vistas de lista, deben etiquetarse mediante controles de texto estático independientes. Para obtener más información sobre los controles que no tienen sus propios títulos, vea [controles sin propiedades de título](controls-without-caption-properties.md).

Se pueden usar varias técnicas para solucionar situaciones en las que los controles no tienen sus propios títulos, pero solo se aplican a las ventanas que se muestran en el administrador de cuadros de diálogo estándar (SDM). Todas las demás ventanas deben exponer los nombres y la relación entre los controles que admiten explícitamente Microsoft Active Accessibility. Para obtener más información acerca de Active Accessibility, vea la sección de [accesibilidad](/windows/desktop/accessibility) de MSDN Library.

 

 
