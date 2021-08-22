---
description: Una aplicación obtiene un controlador de dominio para mostrar llamando a la función BeginPaint, GetDC o GetDCEx e identificando la ventana en la que aparecerá la salida correspondiente.
ms.assetid: 8f952d68-ee52-4e63-9f09-80a14c755d31
title: Mostrar contextos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2e2bbd847d1a473ff08de7db52da7513b91377e8a891b2c6fdde04a82bf1d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761333"
---
# <a name="display-device-contexts"></a>Mostrar contextos de dispositivo

Una aplicación obtiene un controlador de dominio para mostrar llamando a la función [**BeginPaint,**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) e identificando la ventana en la que aparecerá la salida correspondiente. Normalmente, una aplicación obtiene un controlador de dominio de presentación solo cuando debe dibujar en el área cliente. Sin embargo, se puede obtener un contexto [de dispositivo de ventana](#window-device-contexts) mediante una llamada a la función [**GetWindowDC.**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) Cuando la aplicación termina de dibujarse, debe liberar el controlador de dominio mediante una llamada a [**la función EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) [**o ReleaseDC.**](/windows/desktop/api/Winuser/nf-winuser-releasedc)

Hay cinco tipos de DCs para las pantallas de vídeo:

-   Clase
-   Comunes
-   Privada
-   Periodo
-   Parent

## <a name="class-device-contexts"></a>Contextos de dispositivo de clase

*Los contextos de dispositivo de* clase se admiten estrictamente para la compatibilidad con versiones de 16 bits de Windows. Al escribir la aplicación, evite usar el contexto de dispositivo de clase; use un contexto de dispositivo privado en su lugar.

## <a name="common-device-contexts"></a>Contextos de dispositivo comunes

*Los contextos de dispositivo comunes* se muestran en los DCs mantenidos en una caché especial por el sistema. Los contextos de dispositivo comunes se usan en aplicaciones que realizan operaciones de dibujo poco frecuentes. Antes de que el sistema devuelva el controlador de dominio, inicializa el contexto de dispositivo común con objetos, atributos y modos predeterminados. Las operaciones de dibujo realizadas por la aplicación usan estos valores predeterminados a menos que se llame a una de las funciones GDI para seleccionar un nuevo objeto, cambiar los atributos de un objeto existente o seleccionar un nuevo modo.

Dado que solo existe un número limitado de contextos de dispositivo comunes, una aplicación debe liberarlos una vez que haya terminado de dibujarse. Cuando la aplicación libera un contexto de dispositivo común, se pierden los cambios en los datos predeterminados.

## <a name="private-device-contexts"></a>Contextos de dispositivo privado

*Los contextos de dispositivo privado* son centros de datos de visualización que, a diferencia de los contextos de dispositivo comunes, conservan los cambios en los datos predeterminados incluso después de que una aplicación los libera. Los contextos de dispositivo privado se usan en aplicaciones que realizan numerosas operaciones de dibujo, como aplicaciones de diseño asistido por PC (CAD), aplicaciones de publicación de escritorio, aplicaciones de dibujo y dibujo, entre otras. Los contextos de dispositivo privado no forman parte de la caché del sistema y, por tanto, no es necesario liberar después de su uso. El sistema quita automáticamente un contexto de dispositivo privado después de que se haya destruido la última ventana de esa clase.

Una aplicación crea un contexto de dispositivo privado especificando primero el estilo de clase de ventana OWNDC de CS cuando inicializa el miembro de estilo de la estructura WNDCLASS y llama a la \_ [**función RegisterClass.**](/windows/win32/api/winuser/nf-winuser-registerclassa)  [](/windows/win32/api/winuser/ns-winuser-wndclassa) (Para obtener más información sobre las clases de ventana, vea [Clases de ventana).](../winmsg/window-classes.md)

Después de crear una ventana con el estilo OWNDC de CS, una aplicación puede llamar a la función \_ [**GetDC,**](/windows/desktop/api/Winuser/nf-winuser-getdc) [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)o [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) una vez para obtener un identificador que identifique un contexto de dispositivo privado. La aplicación puede seguir usando este identificador (y el controlador de dominio asociado) hasta que elimine la ventana creada con esta clase. El sistema conserva los cambios en los objetos gráficos y sus atributos, o en los modos gráficos hasta que se elimina la ventana.

## <a name="window-device-contexts"></a>Contextos de dispositivo de ventana

Un *contexto de dispositivo de ventana* permite que una aplicación dibuje en cualquier parte de una ventana, incluido el área no cliente. Los contextos de dispositivo de ventana suelen usarse en aplicaciones que procesan los mensajes [**WM \_ NCPAINT**](wm-ncpaint.md) y [**WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) para ventanas con áreas no cliente personalizadas. No se recomienda usar un contexto de dispositivo de ventana para ningún otro propósito. Para obtener más información; vea [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc).

## <a name="parent-device-contexts"></a>Contextos de dispositivo primario

Un *contexto de dispositivo primario* permite que una aplicación minimice el tiempo necesario para configurar la región de recorte de una ventana. Normalmente, una aplicación usa contextos de dispositivo primarios para acelerar el dibujo de las ventanas de control sin necesidad de un contexto de dispositivo privado o de clase. Por ejemplo, el sistema usa contextos de dispositivo primarios para los controles de botón de inserción y edición. Los contextos de dispositivo primario están diseñados para usarse solo con ventanas secundarias, nunca con ventanas de nivel superior o emergentes. Para obtener más información; vea [Parent Display Device Contexts (Contextos de dispositivo de presentación primarios).](parent-display-device-contexts.md)

 

 
