---
description: Una aplicación puede usar una fuente para dibujar texto solo si dicha fuente reside en un dispositivo especificado o instalado en la tabla de fuentes del sistema.
ms.assetid: b422b981-8760-4484-9965-f212287c421e
title: Instalación y eliminación de fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0184054973c769462ed8c1620e5534ff909576ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997377"
---
# <a name="font-installation-and-deletion"></a>Instalación y eliminación de fuentes

Una aplicación puede usar una fuente para dibujar texto solo si dicha fuente reside en un dispositivo especificado o instalado en la tabla de fuentes del sistema. La tabla de fuentes es una matriz interna que identifica todas las fuentes que no son de dispositivo disponibles para una aplicación. Una aplicación puede recuperar los nombres de las fuentes actualmente instaladas en un dispositivo o almacenadas en la tabla de fuentes internas llamando a las funciones [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) o [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) .

Para instalar temporalmente una fuente, llame a [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) o [**AddFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourceexa). Estas funciones cargan una fuente que se almacena en un archivo de recursos de fuente. Sin embargo, se trata de una instalación temporal porque, después de un reinicio, la fuente no estará presente.

Para instalar una fuente que permanecerá después de reiniciar el sistema, use uno de los métodos siguientes:

-   Vaya al panel de control, haga clic en el icono **fuentes** y seleccione **instalar nuevas fuentes** en el menú **archivo** . La fuente está disponible para una aplicación incluso antes del reinicio. Sin embargo, en una situación de Terminal Server, la fuente está disponible para la sesión actual, pero no está disponible para otras sesiones hasta después de un reinicio.
-   Copie la fuente en la carpeta% WINDIR% \\ Fonts. A continuación, vaya al panel de control y haga clic en el icono **fuentes** , o bien llame a [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) o [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa). La fuente está disponible para una aplicación incluso antes del reinicio. Sin embargo, en una situación de Terminal Server, la fuente está disponible para la sesión actual, pero no está disponible para otras sesiones hasta después de un reinicio. Si solo copia la fuente en la carpeta% WINDIR% \\ Fonts, la fuente solo estará disponible después de reiniciar el sistema.

Cuando una aplicación termina de usar una fuente instalada, debe quitar esa fuente mediante una llamada a la función [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) .

Una fuente instalada desde una ubicación distinta de la carpeta% WINDIR% \\ Fonts no se puede modificar cuando se carga en una sesión activa, incluida la sesión 0. Por lo tanto, se bloqueará cualquier intento de cambiar, reemplazar o eliminar. Si es necesario modificar una fuente:

-   Las *fuentes temporales* se cargan solo en la sesión actual. Antes de intentar realizar alguna modificación en la fuente, llame a [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) para forzar que la sesión actual Descargue la fuente.
-   Las *fuentes permanentes* permanecen instaladas después del reinicio y se cargan en todas las sesiones creadas. Llame a [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) para forzar que la sesión actual Descargue la fuente. A continuación, en la clave del registro de fuentes (**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Fonts**) Busque y quite el valor del registro asociado a la fuente. Por último, reinicie el equipo para asegurarse de que la fuente no se carga en ninguna sesión. Después del reinicio, continúe con la modificación o eliminación de fuentes.

Siempre que una aplicación llama a las funciones que agregan y eliminan recursos de fuente, también debe llamar a la función [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) y enviar un mensaje de [**WM \_ FONTCHANGE**](wm-fontchange.md) a todas las ventanas de nivel superior del sistema. Este mensaje notifica a otras aplicaciones que la tabla de fuentes internas ha sido modificada por una aplicación que ha agregado o quitado una fuente.

 

 
