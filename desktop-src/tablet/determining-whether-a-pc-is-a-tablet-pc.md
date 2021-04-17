---
description: En ocasiones, es posible que necesite determinar si la aplicación se ejecuta en un Tablet PC porque puede que desee que las aplicaciones aprovechen las capacidades inherentes de tinta, reconocimiento y lápiz.
ms.assetid: 86a3eddb-6541-4b73-b2ca-6adedad1a1e5
title: Determinar si un equipo es Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c793d5531d6091d4bce73d99bfa32d100c2b9304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716721"
---
# <a name="determining-whether-a-pc-is-a-tablet-pc"></a>Determinar si un equipo es Tablet PC

En ocasiones, es posible que necesite determinar si la aplicación se ejecuta en un Tablet PC porque puede que desee que las aplicaciones aprovechen las capacidades inherentes de tinta, reconocimiento y lápiz. Para ayudarle a determinar si la aplicación tiene acceso a las características de Tablet PC, puede usar la llamada de la API de Windows GetSystemMetrics () tal y como se describe en este tema.

## <a name="client-side-applications"></a>Aplicaciones Client-Side

Puede usar las técnicas siguientes para determinar si el código se ejecuta en un Tablet PC.

-   [Uso de GetSystemMetrics (SM \_ TABLETPC)](/windows)
-   [Usar la presencia de archivos binarios de la plataforma de tableta](#using-the-presence-of-tablet-platform-binaries)
-   [Aplicaciones basadas en Web](#web-based-applications)

### <a name="using-getsystemmetrics-sm_tabletpc"></a>Uso de GetSystemMetrics (SM \_ TABLETPC)

### <a name="windows-xp-tablet-pc-edition"></a>Windows XP Tablet PC Edition

En Microsoft Windows XP Tablet PC Edition, utilice la función GetSystemMetrics (SM \_ TABLETPC) para determinar si un equipo es un Tablet PC. GetSystemMetrics (SM \_ TABLETPC) está diseñado para que devuelva true en un equipo con Windows XP Tablet PC Edition.

### <a name="windows-vista"></a>Windows Vista

En Windows Vista, ya no hay un SDK de Tablet PC diferente. El Windows SDK contiene ahora una sección denominada "Tablet PC y tecnología táctil" y la lógica de GetSystemMetrics (SM \_ TABLETPC) ha cambiado para reflejar esto. GetSystemMetrics (SM \_ TABLETPC) ahora devuelve true si se cumplen todas las condiciones siguientes:

-   Hay un digitalizador integrado, ya sea Pen o Touch, en el sistema.
-   El componente opcional de Tablet PC está instalado. Este componente contiene características como el panel de entrada de Tablet PC y Windows Journal.
-   El equipo tiene licencia para usar el componente opcional. Las versiones Premium de Windows Vista, como Windows Vista Home Premium, Windows Vista Small Business, Windows Vista Professional, Windows Vista Enterprise y Windows Vista Ultimate, tienen licencia para usar el componente opcional.
-   Se está ejecutando el servicio de entrada de Tablet PC. El servicio de entrada de Tablet PC es un nuevo servicio para Windows Vista que controla la entrada de Tablet PC.

Con esta mayor precisión, GetSystemMetrics (SM \_ TABLETPC) sigue siendo la forma recomendada de determinar si un equipo que ejecuta Windows Vista es un Tablet PC.

### <a name="using-the-presence-of-tablet-platform-binaries"></a>Usar la presencia de archivos binarios de la plataforma de tableta

En Windows XP Tablet PC Edition y Windows Vista, puede buscar la presencia de los archivos binarios de tinta, como inkobj.dll y Microsoft.Ink.dll, y usar su funcionalidad compatible si están presentes.

En Windows Vista, los archivos binarios de la plataforma de Tablet PC se instalan de forma predeterminada en todas las versiones de cliente. La funcionalidad de entrada y de entrada manuscrita está disponible en esas versiones. El reconocimiento solo está disponible en las versiones Premium de Windows Vista.

### <a name="web-based-applications"></a>Aplicaciones Web-Based

En Windows Vista, la cadena User-Agent indicada por Internet Explorer incluye "Tablet PC 2,0" si, según GetSystemMetrics (SM \_ TABLETPC), el dispositivo es un Tablet PC.

En Windows XP Tablet PC Edition 2005, la cadena User-Agent incluye Tablet PC 1,7. La cadena User-Agent tiene un aspecto similar al siguiente:

`Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; .NET CLR 1.0.3705; Tablet PC 2.0)`

Use este valor para determinar si el equipo cliente es un Tablet PC y admite controles de entrada de lápiz basados en Web.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> </dl>

 

 
