---
description: Una aplicación obtiene un controlador de dominio de visualización mediante una llamada a la función BeginPaint, GetDC o GetDCEx e identifica la ventana en la que aparecerá el resultado correspondiente.
ms.assetid: 8f952d68-ee52-4e63-9f09-80a14c755d31
title: Mostrar contextos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d0eeb3055209ad99a6a50fd129f9f9c064bf52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811984"
---
# <a name="display-device-contexts"></a>Mostrar contextos de dispositivo

Una aplicación obtiene un controlador de dominio de visualización mediante una llamada a la función [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) e identifica la ventana en la que aparecerá el resultado correspondiente. Normalmente, una aplicación obtiene un controlador de dominio de visualización solo cuando se debe dibujar en el área de cliente. Sin embargo, puede obtener un [contexto de dispositivo de ventana](#window-device-contexts) mediante una llamada a la función [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) . Cuando finaliza el dibujo de la aplicación, debe liberar el controlador de dominio mediante una llamada a la función [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) o [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) .

Hay cinco tipos de controladores de DC para presentaciones de vídeo:

-   Clase
-   Comunes
-   Private
-   Periodo
-   Parent

## <a name="class-device-contexts"></a>Contextos de dispositivo de clase

Los *contextos de dispositivo de clase* se admiten estrictamente por compatibilidad con las versiones de 16 bits de Windows. Al escribir la aplicación, evite usar el contexto de dispositivo de clase. en su lugar, use un contexto de dispositivo privado.

## <a name="common-device-contexts"></a>Contextos de dispositivo comunes

Los *contextos de dispositivo comunes* son los controladores de dispositivos que el sistema mantiene en una memoria caché especial. Los contextos de dispositivo comunes se utilizan en aplicaciones que realizan operaciones de dibujo poco frecuentes. Antes de que el sistema devuelva el identificador de controlador de dominio, inicializa el contexto de dispositivo común con los objetos, atributos y modos predeterminados. Cualquier operación de dibujo realizada por la aplicación utiliza estos valores predeterminados, a menos que se llame a una de las funciones GDI para seleccionar un nuevo objeto, cambiar los atributos de un objeto existente o seleccionar un nuevo modo.

Dado que solo existe un número limitado de contextos de dispositivo comunes, una aplicación debe liberarlos una vez que haya terminado de dibujar. Cuando la aplicación libera un contexto de dispositivo común, se pierden los cambios realizados en los datos predeterminados.

## <a name="private-device-contexts"></a>Contextos de dispositivo privados

Los *contextos de dispositivo privados* son controladores de eventos que, a diferencia de los contextos de dispositivos comunes, conservan los cambios en los datos predeterminados incluso después de que una aplicación los libere. Los contextos de dispositivo privados se usan en aplicaciones que realizan numerosas operaciones de dibujo, como aplicaciones de diseño asistido por PC (CAD), aplicaciones de publicación de escritorio, aplicaciones de dibujo y pintado, etc. Los contextos de dispositivos privados no forman parte de la memoria caché del sistema y, por tanto, no es necesario liberarlos después del uso. El sistema quita automáticamente un contexto de dispositivo privado después de que se haya destruido la última ventana de esa clase.

Una aplicación crea un contexto de dispositivo privado especificando primero el \_ estilo de clase de ventana CS OWNDC cuando inicializa el miembro de **estilo** de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) y llama a la función [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . (Para obtener más información sobre las clases de ventana, vea [clases de ventana](../winmsg/window-classes.md)).

Después de crear una ventana con el \_ estilo CS OWNDC, una aplicación puede llamar a la función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc), [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)o [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) una vez para obtener un identificador que identifique un contexto de dispositivo privado. La aplicación puede seguir usando este identificador (y el controlador de dominio asociado) hasta que se elimina la ventana creada con esta clase. Los cambios realizados en los objetos gráficos y sus atributos, o en los modos gráficos se retienen en el sistema hasta que se elimina la ventana.

## <a name="window-device-contexts"></a>Contextos de dispositivo de ventana

Un *contexto de dispositivo de ventana* permite a una aplicación dibujar en cualquier parte de una ventana, incluido el área no cliente. Los contextos de dispositivo de ventana suelen usarse en aplicaciones que procesan los mensajes de [**WM \_ NCPAINT**](wm-ncpaint.md) y [**WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) para Windows con áreas no cliente personalizadas. No se recomienda usar un contexto de dispositivo de ventana para ningún otro propósito. Para obtener más información, vea [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc).

## <a name="parent-device-contexts"></a>Contextos de dispositivo primarios

Un *contexto de dispositivo primario* permite a una aplicación minimizar el tiempo necesario para configurar la región de recorte de una ventana. Normalmente, una aplicación usa contextos de dispositivo primarios para acelerar el dibujo de ventanas de control sin necesidad de un contexto de dispositivo privado o de clase. Por ejemplo, el sistema utiliza contextos de dispositivo primarios para los controles de botón de control y edición. Los contextos de dispositivos primarios están pensados para usarse solo con ventanas secundarias, nunca con ventanas emergentes o de nivel superior. Para obtener más información, vea [contextos de dispositivo de pantalla primaria](parent-display-device-contexts.md).

 

 
