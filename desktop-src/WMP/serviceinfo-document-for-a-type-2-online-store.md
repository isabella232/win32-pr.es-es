---
title: Documento ServiceInfo para una tienda en línea de tipo 2
description: Documento ServiceInfo para una tienda en línea de tipo 2
ms.assetid: ca83e9bf-c7fb-4212-8fa2-1fae11ed26e9
keywords:
- Windows Media Player tiendas en línea, documento de ServiceInfo
- tiendas en línea, documento de ServiceInfo
- tipo 2 tiendas en línea, documento de ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fb558661332ab08edd2057fa024a1a0e2034b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075867"
---
# <a name="serviceinfo-document-for-a-type-2-online-store"></a>Documento ServiceInfo para una tienda en línea de tipo 2

Los proveedores de tiendas en línea de tipo 2 deben proporcionar a Microsoft la dirección URL de un documento XML que describa la tienda en línea. Windows Media Player 10 y Windows Media Player 11 Use este documento para determinar cómo configurar la interfaz de usuario para hospedar la tienda en línea.

En Windows Media Player 10, el documento ServiceInfo proporciona lo siguiente:

-   Información sobre cómo configurar los paneles de tareas que Windows Media Player muestra cuando la tienda en línea está activa. Una tienda en línea puede tener uno, dos o tres paneles de tareas.
-   Información utilizada para configurar los botones del panel de tareas, como el texto del botón, el color del botón y la información sobre herramientas de los botones.
-   Direcciones URL para las imágenes que Windows Media Player muestra para identificar la tienda en línea.
-   Direcciones URL de páginas web, proporcionadas por la tienda en línea, que Windows Media Player hospeda en su interfaz de usuario.
-   Información sobre cómo el programa de instalación de Windows Media Player debe configurar la primera tienda en línea que el usuario ve.

En Windows Media Player 11, el documento ServiceInfo proporciona lo siguiente:

-   Información utilizada para configurar el botón para la pestaña tiendas en línea, como el texto del botón y la información sobre herramientas para el botón.
-   Direcciones URL para las imágenes que Windows Media Player muestra para identificar la tienda en línea.
-   Direcciones URL de páginas web, proporcionadas por la tienda en línea, que Windows Media Player hospeda en su interfaz de usuario.

Al empezar a desarrollar la tienda en línea, debe proporcionar a Microsoft la dirección URL del documento ServiceInfo. Durante la fase de desarrollo, la tienda en línea aparecerá en Windows Media Player solo cuando se establezca una clave del registro especial.

Una vez publicada la tienda en línea, el escenario ususal es que Windows Media Player recupera el documento ServiceInfo de la web automáticamente. En algunos casos, sin embargo, Windows Media Player recupera el documento ServiceInfo del equipo del usuario. Para obtener más información, consulte [configuración de la tienda en línea inicial](setting-the-initial-online-store.md).

Cuando Windows Media Player recupera el documento ServiceInfo de la web, anexa una cadena de consulta a la dirección URL. La cadena de consulta contiene parámetros que proporcionan información sobre la configuración regional del usuario y la versión de Windows Media Player.

Puede crear documentos de ServiceInfo estáticos o dinámicos. Un documento de ServiceInfo estático tiene una extensión de nombre de archivo. Xml. Un documento de ServiceInfo dinámico es una página ASP y tiene una extensión de nombre de archivo. asp o. aspx.

No todos los elementos disponibles para su uso en el documento ServiceInfo se pueden usar en cada tienda en línea y algunos elementos son opcionales para todas las tiendas en línea. Para obtener información acerca de los tipos de tiendas en línea que puede crear y las características disponibles para cada tipo, consulte [Windows Media Player tiendas en línea](windows-media-player-online-stores.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Creación dinámica del documento ServiceInfo**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




