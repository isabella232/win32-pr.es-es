---
description: Una aplicación puede usar una fuente para dibujar texto solo si esa fuente está en un dispositivo especificado o si está instalada en la tabla de fuentes del sistema.
ms.assetid: b422b981-8760-4484-9965-f212287c421e
title: Instalación y eliminación de fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 112cfbff6bebdfc2fa4d46993f1fa60dcc19285bc3e16ebc2fd929e3a43ba679
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037933"
---
# <a name="font-installation-and-deletion"></a>Instalación y eliminación de fuentes

Una aplicación puede usar una fuente para dibujar texto solo si esa fuente está en un dispositivo especificado o si está instalada en la tabla de fuentes del sistema. La tabla de fuentes es una matriz interna que identifica todas las fuentes que no son de dispositivo que están disponibles para una aplicación. Una aplicación puede recuperar los nombres de las fuentes instaladas actualmente en un dispositivo o almacenadas en la tabla de fuentes interna llamando a las funciones [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) o [**ChooseFont.**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85))

Para instalar temporalmente una fuente, llame a [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) o [**AddFontResourceEx.**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourceexa) Estas funciones cargan una fuente que se almacena en un archivo de recursos de fuente. Sin embargo, se trata de una instalación temporal porque después de reiniciar la fuente no estará presente.

Para instalar una fuente que permanecerá después de reiniciar el sistema, use uno de los métodos siguientes:

-   Vaya a la Panel de control, haga clic en el icono **Fuentes** y seleccione **Instalar nuevas fuentes en** el **menú** Archivo. La fuente está disponible para una aplicación incluso antes del reinicio. Sin embargo, en una situación de terminal server, la fuente está disponible para la sesión actual, pero no está disponible para otras sesiones hasta después de un reinicio.
-   Copie la fuente en la carpeta %windir% \\ fonts. A continuación, vaya a la Panel de control haga clic en el icono **Fuentes** o llame a [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) o [**AddFontResourceEx.**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) La fuente está disponible para una aplicación incluso antes del reinicio. Sin embargo, en una situación de terminal server, la fuente está disponible para la sesión actual, pero no está disponible para otras sesiones hasta después de un reinicio. Si solo copia la fuente en la carpeta %windir% fonts, la fuente estará disponible solo después de reiniciar \\ el sistema.

Cuando una aplicación termina de usar una fuente instalada, debe quitar esa fuente llamando a la [**función RemoveFontResource.**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)

Una fuente instalada desde una ubicación que no sea la carpeta %windir% fonts no se puede modificar cuando se carga en ninguna \\ sesión activa, incluida la sesión 0. Por lo tanto, cualquier intento de cambiar, reemplazar o eliminar se bloqueará. Si es necesario modificar una fuente:

-   *Las fuentes temporales* solo se cargan en la sesión actual. Antes de intentar cualquier modificación de fuente, llame [**a RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) para forzar que la sesión actual descargue la fuente.
-   *Las fuentes permanentes* permanecen instaladas después del reinicio y todas las sesiones creadas las cargan. Llame [**a RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) para forzar que la sesión actual descargue la fuente. A continuación, en la clave del Registro de fuentes (**HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Fonts**) busque y quite el valor del Registro asociado a la fuente. Por último, reinicie la máquina para asegurarse de que la fuente no se carga en ninguna sesión. Después del reinicio, continúe con la modificación o eliminación de la fuente.

Cada vez que una aplicación llama a las funciones que agregan y eliminan recursos de fuente, también debe llamar a la función [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) y enviar un mensaje [**\_ FONTCHANGE de WM**](wm-fontchange.md) a todas las ventanas de nivel superior del sistema. Este mensaje notifica a otras aplicaciones que una aplicación que agregó o quitó una fuente ha modificado la tabla de fuentes interna.

 

 
