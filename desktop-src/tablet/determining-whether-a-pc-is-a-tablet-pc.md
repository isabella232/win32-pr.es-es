---
description: En ocasiones, es posible que tenga que determinar si la aplicación se ejecuta en un tablet PC, ya que es posible que quiera que las aplicaciones aprovechen las funcionalidades inherentes de lápiz, reconocimiento y lápiz.
ms.assetid: 86a3eddb-6541-4b73-b2ca-6adedad1a1e5
title: Determinar si un equipo es un tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4672f450f23fd3ed6a6ad45df0c74ca23328b0b3735e66fceef6713a4c96a3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940915"
---
# <a name="determining-whether-a-pc-is-a-tablet-pc"></a>Determinar si un equipo es un tablet PC

En ocasiones, es posible que tenga que determinar si la aplicación se ejecuta en un tablet PC, ya que es posible que quiera que las aplicaciones aprovechen las funcionalidades inherentes de lápiz, reconocimiento y lápiz. Para ayudarle a determinar si la aplicación tiene acceso a las características de Tablet PC, puede usar la llamada API getSystemMetrics() Windows, como se describe en este tema.

## <a name="client-side-applications"></a>Client-Side aplicaciones

Puede usar las técnicas siguientes para determinar si el código se ejecuta en un tablet PC.

-   [Uso de GetSystemMetrics (SM \_ TABLETPC)](/windows)
-   [Uso de la presencia de binarios de la plataforma de tabletas](#using-the-presence-of-tablet-platform-binaries)
-   [Aplicaciones basadas en web](#web-based-applications)

### <a name="using-getsystemmetrics-sm_tabletpc"></a>Uso de GetSystemMetrics (SM \_ TABLETPC)

### <a name="windows-xp-tablet-pc-edition"></a>Windows XP Tablet PC Edition

En Microsoft Windows XP Tablet PC Edition, use la función GetSystemMetrics(SM TABLETPC) para determinar si un equipo \_ es un tablet PC. GetSystemMetrics(SM TABLETPC) está diseñado para devolver TRUE en un equipo que \_ ejecuta Windows XP Tablet PC Edition.

### <a name="windows-vista"></a>Windows Vista

En Windows Vista, ya no hay un SDK de Tablet PC distinto. El SDK Windows ahora contiene una sección denominada "Tablet PC y tecnología táctil" y la lógica de GetSystemMetrics(SM TABLETPC) se ha cambiado para reflejar \_ esto. GetSystemMetrics(SM \_ TABLETPC) ahora devuelve true si se cumplen todas las condiciones siguientes:

-   Hay un digitalizador integrado, ya sea lápiz o táctil, en el sistema.
-   El componente opcional Tablet PC está instalado. Este componente contiene características como panel de entrada de Tablet PC y Windows Journal.
-   El equipo tiene licencia para usar el componente opcional. Premium versiones de Windows Vista, como Windows Vista Home Premium, Windows Vista Small Business, Windows Vista Professional, Windows Vista Enterprise y Windows Vista Ultimate, tienen licencia para usar el componente opcional.
-   Se está ejecutando el servicio de entrada de Tablet PC. Tablet PC Input Service es un nuevo servicio para Windows Vista que controla la entrada de Tablet PC.

Con esta mayor precisión, GetSystemMetrics(SM TABLETPC) sigue siendo la manera recomendada de determinar si un equipo que ejecuta Windows Vista es \_ un tablet PC.

### <a name="using-the-presence-of-tablet-platform-binaries"></a>Uso de la presencia de binarios de la plataforma de tabletas

En Windows XP Tablet PC Edition y Windows Vista, puede buscar la presencia de los archivos binarios de entrada de lápiz (como inkobj.dll y Microsoft.Ink.dll) y usar su funcionalidad admitida si están presentes.

En Windows Vista, los archivos binarios de la plataforma de Tablet PC se instalan en todas las versiones de cliente de forma predeterminada. La funcionalidad de entrada e entrada de entrada está disponible en esas versiones. El reconocimiento solo está disponible en las versiones Premium de Windows Vista.

### <a name="web-based-applications"></a>Web-Based aplicaciones

En Windows Vista, la cadena de agente de usuario notificada por Internet Explorer incluye "Tablet PC 2.0" si, según GetSystemMetrics(SM TABLETPC), el dispositivo es un \_ tablet PC.

En Windows XP Tablet PC Edition 2005, la cadena de agente de usuario incluye Tablet PC 1.7. La cadena user-agent tiene un aspecto similar al siguiente:

`Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; .NET CLR 1.0.3705; Tablet PC 2.0)`

Use este valor para determinar si el equipo cliente es un tablet PC y admite controles de entrada en pantalla basados en Web.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> </dl>

 

 
