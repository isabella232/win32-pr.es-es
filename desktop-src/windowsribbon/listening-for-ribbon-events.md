---
title: Escuchar eventos de la cinta de opciones
description: El marco Windows cinta de opciones de Windows usa la infraestructura de seguimiento de eventos para Windows (ETW) para permitir a los desarrolladores aprender cómo interactúan los usuarios con la cinta de opciones de su aplicación.
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Windows Cinta de opciones, eventos
- Cinta de opciones, eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf28052aa741437a7f96f90ddb1b4a773ae4c4a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473041"
---
# <a name="listening-for-ribbon-events"></a>Escuchar eventos de la cinta de opciones

El marco Windows cinta de opciones de Windows usa la infraestructura de seguimiento de eventos para [Windows (ETW)](../etw/event-tracing-portal.md) para permitir que los desarrolladores aprendan cómo interactúan los usuarios con la cinta de opciones de su aplicación.

## <a name="introduction"></a>Introducción

El mecanismo de eventos del marco de la cinta de opciones está diseñado de forma que el marco informa de eventos de la interfaz de usuario de la cinta de opciones a la aplicación para que pueda supervisar la actividad del usuario, conocer sus patrones de interacción y evaluar las tendencias de uso. Esta información se puede usar para refinar la experiencia del usuario para futuras iteraciones de la aplicación de cinta de opciones.

El uso de los eventos del marco de la cinta implica lo siguiente:

1.  La aplicación de cinta de opciones debe registrar un agente de escucha de Seguimiento de eventos [Windows (ETW)](../etw/event-tracing-portal.md) para recibir notificaciones de eventos de la cinta de opciones desde el marco de la cinta de opciones.
2.  El marco de la cinta de opciones activa devoluciones de llamada de eventos de la interfaz de usuario de la cinta en tiempo de ejecución, si la aplicación ha registrado un agente de escucha de seguimiento de eventos Windows [(ETW).](../etw/event-tracing-portal.md)

## <a name="supported-events"></a>Eventos admitidos

Los eventos expuestos a las aplicaciones de cinta de opciones se describen en la tabla siguiente. 


| Evento | Informe de eventos | 
|-------|--------------|
| Pestaña activada | Identificador de comando<br /> Nombre de comando<br /> Verbo de evento<br /> | 
| Pestaña contextual activada | Identificador de comando<br /> Nombre de comando<br /> Verbo de evento<br /> | 
| Menú de la aplicación abierto | Verbo de evento<br /> | 
| Menú de la aplicación cerrado | Verbo de evento<br /> | 
| Menú (normal o galería) abierto | Identificador de comando<br /> Nombre de comando<br /> Verbo de evento<br /><blockquote>[!Note]<br />Los eventos de menú QAT no se exponen.</blockquote><br /> | 
| Menú (normal o galería) cerrado | Identificador de comando<br /> Nombre de comando<br /> Verbo de evento<br /><blockquote>[!Note]<br />Los eventos de menú QAT no se exponen.</blockquote><br /> | 
| Comando | Identificador de comando<br /> Nombre de comando<br /> Verbo de evento<br /> Una de las siguientes ubicaciones de eventos:<ul><li>CINTA</li><li>QUICKACCESSTOOLBAR</li><li>APPLICATIONMENU</li><li>CONTEXTPOPUP</li></ul><br /> Identificador de comando primario<br /> Nombre del comando primario<br /> Uno de los métodos de invocación siguientes:<ul><li>HAGA CLIC</li><li>KEYTIP</li><li>TECLADO</li><li>TOCAR</li></ul><br /><blockquote>[!Note]<br />Las galerías de elementos y los cuadros combinados incluyen el índice de elemento seleccionado, pero no incluyen valores de cadena ni enteros. Los spinners no incluyen el valor entero.</blockquote><br /> | 
| Cinta minimizada | Verbo de evento<br /> | 
| Cinta expandida (botón Expandir clic o pulsar anclado) | Verbo de evento<br /> | 
| Modo de aplicación cambiado | Verbo de evento<br /> Id. de modo (valor establecido a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>través de SetModes)</strong></a><br /><blockquote>[!Note]<br />La aplicación es responsable de desempaquetar este entero para determinar qué modos se han establecido.</blockquote><br /> | 
| Información sobre herramientas mostrada | Verbo de evento<br /> Identificador de comando primario<br /> Nombre del comando primario<br /> | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Guías para desarrolladores de Ribbon Framework](windowsribbon-guides-entry.md)
</dt> <dt>

[Declarar comandos y controles con marcado de cinta](./windowsribbon-schema.md)
</dt> <dt>

[Directrices de la experiencia del usuario de la cinta de opciones](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Proceso de diseño de la cinta de opciones](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

