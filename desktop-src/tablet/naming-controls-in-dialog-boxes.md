---
description: Al usar los cuadros Windows de diálogo de Microsoft, debe etiquetar todos los controles para facilitar la funcionalidad de voz. En el siguiente cuadro de diálogo Ejecutar se muestra una etiqueta de control de texto estático para un cuadro de lista desplegable. El texto estático termina con dos puntos.
ms.assetid: 3b01a4d2-9deb-413f-bab8-566df86b6af9
title: Asignar nombres a controles en cuadros de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c33720c08a7f5454b54d7d982b14c091fe6e1df4c18a49cd649f54690f2eb11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449837"
---
# <a name="naming-controls-in-dialog-boxes"></a>Asignar nombres a controles en cuadros de diálogo

Al usar los cuadros Windows de diálogo de Microsoft, debe etiquetar todos los controles para facilitar la funcionalidad de voz. En el **siguiente cuadro de** diálogo Ejecutar se muestra una etiqueta de control de texto estático para un cuadro de lista desplegable. El texto estático termina con dos puntos.

![captura de pantalla que muestra el cuadro de diálogo ejecutar](images/fb0bd076-e9f9-4260-a54a-9d7db93157da.jpg)

Existen dos tipos de controles:

-   Controles que tienen sus títulos como una propiedad de ese control, como botones de comando y casillas. Las ayuda de accesibilidad no tienen ningún problema para identificar estos controles, siempre y cuando el título esté definido correctamente.
-   Los controles que no tienen sus propios títulos, como controles de edición, cuadros de lista y vistas de lista, deben etiquetarse mediante controles de texto estático independientes. Para obtener más información sobre los controles que no tienen sus propios títulos, vea [Controles sin propiedades de título.](controls-without-caption-properties.md)

Se pueden usar varias técnicas para superar situaciones en las que los controles no tienen sus propios títulos, pero solo son efectivos para las ventanas mostradas por el Administrador de diálogos estándar (SDM). Todas las demás ventanas deben exponer los nombres y la relación entre los controles al admitir explícitamente Microsoft Active Accessibility. Para obtener más información Active Accessibility, vea la [sección Accesibilidad](/windows/desktop/accessibility) de MSDN Library.

 

 
