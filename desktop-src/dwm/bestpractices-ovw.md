---
title: Consideraciones de rendimiento y procedimientos recomendados
description: En este tema se presenta un conjunto de procedimientos recomendados para usar las API Administrador de ventanas de escritorio (DWM).
ms.assetid: 5b1f6ff8-1d3f-4a70-8efd-90f8802e8532
keywords:
- Administrador de ventanas de escritorio (DWM),procedimientos recomendados
- DWM (Administrador de ventanas de escritorio),procedimientos recomendados
- Administrador de ventanas de escritorio (DWM),prácticas de aplicación
- DWM (Administrador de ventanas de escritorio),prácticas de aplicación
- Administrador de ventanas de escritorio (DWM),prácticas de dibujo
- DWM (Administrador de ventanas de escritorio),prácticas de dibujo
- Administrador de ventanas de escritorio (DWM), efecto de desenfoque subyacente
- DWM (Administrador de ventanas de escritorio), efecto de desenfoque subyacente
- prácticas de aplicación
- prácticas de dibujo
- efecto de desenfoque subyacente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7affbbf5ebca91a4e5172e75f88da4b9fe8e33f6e1e3de1e7a735add816a313f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280278"
---
# <a name="performance-considerations-and-best-practices"></a>Consideraciones de rendimiento y procedimientos recomendados

En este tema se presenta un conjunto de procedimientos recomendados para usar las API Administrador de ventanas de escritorio (DWM).

Este tema contiene las siguientes secciones:

-   [Prácticas de aplicación para DWM](#application-practices-for-dwm)
-   [Prácticas de dibujo para DWM](#drawing-practices-for-dwm)
-   [Región de cliente Blur-Behind DWM](#dwm-blur-behind-client-region)

## <a name="application-practices-for-dwm"></a>Prácticas de aplicación para DWM

Si la aplicación controla el escalado de puntos por pulgada (ppp), puede declarar una aplicación como compatible con ppp y evitar el escalado automático estableciendo la marca compatible con ppp en el manifiesto del programa o llamando a la función [**SetProcessDPIAware durante**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) la inicialización del programa.

Con la composición de DWM activada, las aplicaciones ocultas ya no reciben mensajes [**\_ WM PAINT**](/windows/desktop/gdi/wm-paint) y no se les pide que vuelvan a representarse. El contenido de cada ventana ya está disponible para crear la imagen de pantalla.

Las ventanas [**transparentes de WS \_ EX \_ de**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) nivel superior deben combinarse con un estilo **WS EX \_ \_ LAYERED** con el fin de realizar pruebas de acceso. **WS \_ EX \_ TRANSPARENT** en el sentido clásico, sin redireccionamiento, es útil para las ventanas secundarias de una jerarquía de ventanas que pertenecen al mismo subproceso, pero no está pensada para ventanas de nivel superior.

Use regiones o capas para crear ventanas en forma o mezcla. Tenga en cuenta que Windows Vista y versiones posteriores de Windows, el dibujo personalizado solo parte de una ventana de nivel superior no proporcionará el contenido obsoleto deseado en regiones sin dibujar.

Las API como [**GetDCOrgEx**](/windows/desktop/api/wingdi/nf-wingdi-getdcorgex) se pueden usar para determinar determinados valores reales. Si tiene un contexto de dispositivo (DC) para una ventana redirigida, el origen devuelto por **GetDCOrgEx** no coincidirá con el origen de la ventana en la pantalla. En su lugar, el origen será el origen de la superficie del búfer de reserva de la ventana: (0, 0).

Cuando se produce un error en todo lo demás, deshabilite la representación de la ventana mediante una llamada [**a la función DwmSetWindowAttribute.**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute)

## <a name="drawing-practices-for-dwm"></a>Prácticas de dibujo para DWM

Evite dibujar directamente en la superficie de presentación principal. Si lo hace, el DWM deshabilitará la composición hasta que la aplicación libere la superficie del dispositivo principal.

Evalúe si la aplicación debe proporcionar su propio almacenamiento en búfer doble. DwM almacena en búfer de forma eficaz el contenido y presenta la ventana en un solo fotograma.

Evite leer o escribir en un controlador de dominio de pantalla. Aunque es compatible con DWM, no se recomienda debido a una reducción del rendimiento.

Evite dibujar en el área que no es de cliente. Aunque la aplicación puede acceder a esta área y la API de Microsoft Win32 admite el dibujo, esto puede hacer que la ventana pierda cualquier borde de cristal que tenga.

Evite mezclar Windows Interfaz de dispositivo gráfico (GDI) y Microsoft DirectX a menos que no se superpongan. Si es necesaria la combinación, dibuje el contenido GDI en una superficie de software de DirectX y conéctelo antes de componer en la pantalla, o bien dibuje el contenido en ventanas independientes.

Use [**la función BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) [**o StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) en lugar Windows GDI+ para presentar el dibujo para su representación. GDI+ representa una línea de examen a la vez con representación de software. Esto puede provocar parpadeo en las aplicaciones.

## <a name="dwm-blur-behind-client-region"></a>Región de cliente Blur-Behind DWM

La representación del efecto de desenfoque subyacente es una operación que consume muchos recursos tanto para la CPU como para la unidad de procesamiento gráfico (GPU). Los desarrolladores de aplicaciones se animan a tener en cuenta las implicaciones de usar el desenfoque del área de cliente para que no consuma recursos excesivos. Debe tener especial precaución en los casos siguientes:

-   Cuando se espera que el tamaño del desenfoque del área de cliente sea significativo, incluso si no se producirá ninguna actualización en el área desenfoque propiamente dicha. El desenfoque debe representarse en caso de que se produzcan actualizaciones en el área desenfoque de la ventana, lo que conlleva costos de CPU y GPU. Además, las operaciones de ventana en la ventana (movimiento, cambio de tamaño o transiciones) incurrirán en más costos.
-   Cuando se esperan actualizaciones significativas en el área de cliente desenfoque. Esto requerirá volver a dibujar el desenfoque en cada actualización y consumir recursos excesivos.
-   Si se espera que el desenfoque cubra un área significativa y también se esperan actualizaciones en esa área, se recomienda encarecidamente no desenfocar el área de cliente.

 

 