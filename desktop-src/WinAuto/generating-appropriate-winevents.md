---
title: Generación de WinEvents adecuados
description: Los desarrolladores de servidores deben asegurarse de que se generan winevents adecuados para todos los elementos de la interfaz de usuario, incluidos elementos de interfaz de usuario basados en ventanas, elementos de interfaz de usuario sin ventanas y elementos de interfaz de usuario con comportamientos altamente personalizados.
ms.assetid: 253e0162-20e6-4e89-b563-aae9cf7e53a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e148578f55f59d2827fd13a637baf5139c3f934ddf24059e437185c15349b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860395"
---
# <a name="generating-appropriate-winevents"></a>Generación de WinEvents adecuados

Los desarrolladores de servidores deben asegurarse de que se generan winevents adecuados para todos los elementos de la interfaz de usuario, incluidos elementos de interfaz de usuario basados en ventanas, elementos de interfaz de usuario sin ventanas y elementos de interfaz de usuario con comportamientos altamente personalizados.

USER proporciona compatibilidad predeterminada de WinEvent con elementos de interfaz de usuario estándar basados en **HWND.** Dado que USER genera estos eventos automáticamente, los servidores solo deben generar eventos para controles personalizados, elementos sin ventanas o controles cuyos eventos aún no haya generado USER.

Para enviar un evento, los servidores llaman a [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) y pasan la constante de evento, un identificador de objeto y **el HWND** para una ventana que puede responder a las solicitudes de cliente para obtener más información. Los eventos que deben desencadenarse varían según el tipo de elemento de la interfaz de usuario. Hay eventos generales que se deben enviar para todos los controles y eventos específicos que solo se deben enviar para el elemento de interfaz de usuario adecuado.

## <a name="general-events"></a>Eventos generales.

Se pueden enviar WinEvents generales para todos los elementos de la interfaz de usuario. Estos incluyen las siguientes:

-   [**EVENTO \_ OBJECT \_ CREATE**](event-constants.md) (cuando se crea un objeto)
-   [**EVENTO \_ OBJECT \_ DESTROY**](event-constants.md) (cuando se destruye un objeto)
-   [**EVENTO \_ OBJECT \_ SHOW**](event-constants.md) (cuando se muestra un objeto)
-   [**EVENTO \_ OBJECT \_ HIDE**](event-constants.md) (cuando un objeto está oculto)

## <a name="specific-events"></a>Eventos específicos

También hay winevents específicos que se pueden enviar para un tipo determinado de elemento de interfaz de usuario. Por ejemplo, use [**EVENT \_ OBJECT SELECTION \_ para**](event-constants.md) los controles que permiten al usuario realizar una selección, como un cuadro de lista.

Para obtener más información sobre qué eventos se esperan para un tipo determinado de elemento de interfaz de usuario, vea los siguientes recursos:

-   [Apéndice A: Referencia Interfaz de usuario elementos admitidos](appendix-a--supported-user-interface-elements-reference.md). En este apéndice se incluye información sobre los elementos de la interfaz de usuario generados por el sistema que expone Microsoft Active Accessibility. La documentación de cada control incluye información sobre los eventos que puede generar el elemento de interfaz de usuario.
-   [Constantes de evento](event-constants.md). En este tema se incluye información sobre los eventos generados por el sistema operativo y las aplicaciones de servidor.
-   Event Watcher accesible (AccEvent.exe). Esta herramienta muestra los eventos que user envía para un elemento de interfaz de usuario determinado. Puede usar esta herramienta para saber qué eventos puede esperar para un elemento de interfaz de usuario. Para obtener más información, vea [Accessible Event Watcher](accessible-event-watcher.md).

 

 




