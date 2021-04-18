---
title: Consideraciones de rendimiento y prácticas recomendadas
description: En este tema se presenta un conjunto de prácticas recomendadas para usar las API de Administrador de ventanas de escritorio (DWM).
ms.assetid: 5b1f6ff8-1d3f-4a70-8efd-90f8802e8532
keywords:
- Administrador de ventanas de escritorio (DWM), procedimientos recomendados
- DWM (Administrador de ventanas de escritorio), procedimientos recomendados
- Administrador de ventanas de escritorio (DWM), prácticas de aplicación
- DWM (Administrador de ventanas de escritorio), prácticas de aplicación
- Administrador de ventanas de escritorio (DWM), prácticas de dibujo
- DWM (Administrador de ventanas de escritorio), prácticas de dibujo
- Administrador de ventanas de escritorio (DWM), efecto Desenfoque detrás
- DWM (Administrador de ventanas de escritorio), efecto Desenfoque detrás
- prácticas de aplicación
- prácticas de dibujo
- Desenfoque detrás del efecto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec76a4920a91f9502940e866d58641a2550d9354
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105705011"
---
# <a name="performance-considerations-and-best-practices"></a>Consideraciones de rendimiento y prácticas recomendadas

En este tema se presenta un conjunto de prácticas recomendadas para usar las API de Administrador de ventanas de escritorio (DWM).

Este tema contiene las siguientes secciones:

-   [Prácticas de aplicación para DWM](#application-practices-for-dwm)
-   [Prácticas de dibujo para DWM](#drawing-practices-for-dwm)
-   [Región de cliente de Blur-Behind DWM](#dwm-blur-behind-client-region)

## <a name="application-practices-for-dwm"></a>Prácticas de aplicación para DWM

Si la aplicación controla el escalado de puntos por pulgada (PPP), puede declarar una aplicación como compatible con PPP y evitar el escalado automático estableciendo la marca de reconocimiento de PPP en el manifiesto del programa o llamando a la función [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) durante la inicialización del programa.

Con la composición DWM activada, las aplicaciones ocultas ya no reciben mensajes de [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) y no se les pide que se vuelvan a representar. El contenido de cada ventana ya está disponible para crear la imagen de la pantalla.

Las ventanas de nivel superior [**WS \_ ex \_ transparentes**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) deben combinarse con un estilo con **\_ \_ capas de WS ex** para la prueba de posicionamiento. **WS \_ Como es \_ transparente** en el sentido clásico, sin redireccionamiento, resulta útil para las ventanas secundarias de una jerarquía de ventanas que pertenecen al mismo subproceso, pero no está pensada para las ventanas de nivel superior.

Utilice regiones o capas para crear ventanas con forma o mezcla. Tenga en cuenta que en Windows Vista y versiones posteriores de Windows, el dibujo personalizado solo parte de una ventana de nivel superior no proporcionará el contenido obsoleto deseado en regiones desdibujadas.

Las API como [**GetDCOrgEx**](/windows/desktop/api/wingdi/nf-wingdi-getdcorgex) se pueden usar para determinar ciertos valores reales. Si tiene un contexto de dispositivo (DC) para una ventana redirigida, el origen devuelto por **GetDCOrgEx** no coincidirá con el origen de la ventana en la pantalla. En su lugar, el origen será el origen de la superficie del búfer de reserva de la ventana: (0,0).

Si se produce un error en todo lo demás, deshabilite la representación de la ventana mediante una llamada a la función [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) .

## <a name="drawing-practices-for-dwm"></a>Prácticas de dibujo para DWM

Evite dibujar directamente en la superficie de visualización principal. Al hacerlo, se forzará al DWM a deshabilitar la composición hasta que la aplicación libere la superficie del dispositivo principal.

Evalúe si la aplicación debe proporcionar su propio almacenamiento en búfer doble. De forma eficaz, el DWM almacena en búfer el contenido y presenta la ventana en un solo fotograma.

Evite leer o escribir en un controlador de dominio de pantalla. Aunque es compatible con DWM, no se recomienda porque disminuye el rendimiento.

Evite dibujar en el área no cliente. Aunque la aplicación puede obtener acceso a esta área y el dibujo de la API de Microsoft Win32 lo admite, esto puede hacer que la ventana pierda cualquier borde Glass que tenga.

Evite mezclar Windows Interfaz de dispositivo gráfico (GDI) y Microsoft DirectX a menos que no se superpongan. Si es necesario mezclar, dibuje el contenido de GDI en una superficie de software de DirectX y combínelo antes de componerlo en la pantalla, o bien dibuje en ventanas independientes.

Use la función [**bitblt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) o [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) en lugar de Windows GDI+ para presentar el dibujo para su representación. GDI+ representa una línea de recorrido a la vez con la representación de software. Esto puede provocar parpadeos en las aplicaciones.

## <a name="dwm-blur-behind-client-region"></a>Región de cliente de Blur-Behind DWM

La representación del efecto de desenfoque es una operación que consume muchos recursos tanto para la CPU como para la unidad de procesamiento de gráficos (GPU). Se recomienda a los desarrolladores de aplicaciones que tengan en cuenta las implicaciones de usar el desenfoque del área de cliente para que no consuma demasiados recursos. Debe tener especial cuidado en los casos siguientes:

-   Cuando se espera que el tamaño del desenfoque del área cliente sea significativo, incluso si no se producirán actualizaciones en el área desenfocada. Se debe representar el desenfoque en caso de que se produzcan actualizaciones en el área desenfocada de la ventana, lo que incurre en costos de CPU y GPU. Además, las operaciones de ventana en la ventana (movimiento/cambio de tamaño/transiciones) incurrirán en costos.
-   Cuando se esperan actualizaciones significativas en el área de cliente desenfocada. Esto requerirá que se vuelva a dibujar el desenfoque en cada actualización y consuma demasiados recursos.
-   Si se espera que el desenfoque cubra un área significativa y también se esperan actualizaciones en esa área, se recomienda encarecidamente no desenfocar el área cliente.

 

 