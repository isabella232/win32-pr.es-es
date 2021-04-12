---
title: Generar WinEvents adecuados
description: Los desarrolladores de servidores deben asegurarse de que se generan WinEvents adecuados para todos los elementos de la interfaz de usuario, incluidos los elementos de interfaz de usuario basados en ventanas, los elementos de interfaz de usuario sin ventanas y los elementos de interfaz de usuario con comportamientos muy personalizados.
ms.assetid: 253e0162-20e6-4e89-b563-aae9cf7e53a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6273411115e908303e863a34908e15ef91b19c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269180"
---
# <a name="generating-appropriate-winevents"></a>Generar WinEvents adecuados

Los desarrolladores de servidores deben asegurarse de que se generan WinEvents adecuados para todos los elementos de la interfaz de usuario, incluidos los elementos de interfaz de usuario basados en ventanas, los elementos de interfaz de usuario sin ventanas y los elementos de interfaz de usuario con comportamientos muy personalizados.

El usuario proporciona compatibilidad predeterminada de WinEvent para los elementos de interfaz de usuario estándar y basados en **hWnd**. Dado que el usuario genera estos eventos automáticamente, los servidores solo deben generar eventos para los controles personalizados, los elementos sin ventanas o los controles cuyos eventos no se hayan generado ya por el usuario.

Para enviar un evento, los servidores llaman a [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) y pasan la constante de evento, un identificador de objeto y el **hWnd** para una ventana que puede responder a las solicitudes de cliente para obtener más información. Los eventos que deben activarse varían según el tipo de elemento de la interfaz de usuario. Hay eventos generales que se deben enviar para todos los controles y eventos específicos que se deben enviar solo para el elemento de la interfaz de usuario adecuado.

## <a name="general-events"></a>Eventos generales.

WinEvents general se puede enviar para todos los elementos de la interfaz de usuario. Entre ellas se incluyen las siguientes:

-   [**Evento \_ de \_Creación de objeto**](event-constants.md) (cuando se crea un objeto)
-   [**Evento \_ de \_Destrucción de objetos**](event-constants.md) (cuando se destruye un objeto)
-   [**Evento \_ de OBJETO \_ Show**](event-constants.md) (cuando se muestra un objeto)
-   [**Evento \_ de \_Ocultar objeto**](event-constants.md) (cuando un objeto está oculto)

## <a name="specific-events"></a>Eventos específicos

También hay WinEvents específicos que se pueden enviar para un tipo concreto de elemento de la interfaz de usuario. Por ejemplo, use [**la \_ \_ selección de objetos de eventos**](event-constants.md) para los controles que permiten al usuario hacer una selección, como un cuadro de lista.

Para obtener más información sobre los eventos que se esperan para un tipo concreto de elemento de la interfaz de usuario, vea los siguientes recursos:

-   [Apéndice A: referencia de elementos de la interfaz de usuario compatibles](appendix-a--supported-user-interface-elements-reference.md). Este apéndice incluye información sobre los elementos de interfaz de usuario generados por el sistema que expone Microsoft Active Accessibility. La documentación de cada control incluye información sobre los eventos que se pueden generar mediante el elemento de la interfaz de usuario.
-   [Constantes de evento](event-constants.md). En este tema se incluye información acerca de los eventos generados por el sistema operativo y las aplicaciones de servidor.
-   Monitor de eventos accesible (AccEvent.exe). Esta herramienta muestra los eventos que el usuario envía para un elemento de la interfaz de usuario determinado. Puede usar esta herramienta para saber qué eventos puede esperar para un elemento de la interfaz de usuario. Para más información, consulte [monitor de eventos accesibles](accessible-event-watcher.md).

 

 




