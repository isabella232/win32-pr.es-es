---
title: Documento ServiceInfo para una tienda en línea de tipo 2
description: Documento ServiceInfo para una tienda en línea de tipo 2
ms.assetid: ca83e9bf-c7fb-4212-8fa2-1fae11ed26e9
keywords:
- Reproductor de Windows Media tiendas en línea,documento ServiceInfo
- tiendas en línea,documento ServiceInfo
- tiendas en línea de tipo 2, documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd6830b4c54b037f254adb21624ed893ec16fa9b3973dfe1536170dff1b4f9e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995435"
---
# <a name="serviceinfo-document-for-a-type-2-online-store"></a>Documento ServiceInfo para una tienda en línea de tipo 2

Los proveedores de tiendas en línea de tipo 2 deben proporcionar a Microsoft la dirección URL de un documento XML que describe la tienda en línea. Reproductor de Windows Media 10 y Reproductor de Windows Media 11 usan este documento para determinar cómo configurar la interfaz de usuario para hospedar la tienda en línea.

En Reproductor de Windows Media 10, el documento ServiceInfo proporciona lo siguiente:

-   Información sobre cómo configurar los paneles de tareas que Reproductor de Windows Media cuando el almacén en línea está activo. Una tienda en línea puede tener uno, dos o tres paneles de tareas.
-   Información utilizada para configurar los botones del panel de tareas, como el texto del botón, el color del botón y las sugerencias de herramientas para los botones.
-   Direcciones URL de las imágenes que Reproductor de Windows Media muestran para identificar la tienda en línea.
-   Direcciones URL de páginas web, proporcionadas por la tienda en línea, que Reproductor de Windows Media hosts en su interfaz de usuario.
-   Información sobre cómo Reproductor de Windows Media configuración debe configurar la primera tienda en línea que ve el usuario.

En Reproductor de Windows Media 11, el documento ServiceInfo proporciona lo siguiente:

-   Información utilizada para configurar el botón para la pestaña Tiendas en línea, como el texto del botón y la información sobre herramientas del botón.
-   Direcciones URL de las imágenes que Reproductor de Windows Media muestran para identificar la tienda en línea.
-   Direcciones URL de páginas web, proporcionadas por la tienda en línea, que Reproductor de Windows Media hosts en su interfaz de usuario.

Cuando empiece a desarrollar su tienda en línea, debe proporcionar a Microsoft la dirección URL del documento ServiceInfo. Durante la fase de desarrollo, la tienda en línea aparecerá en Reproductor de Windows Media solo cuando se establezca una clave del Registro especial.

Una vez publicada la tienda en línea, el escenario ususal es que Reproductor de Windows Media el documento ServiceInfo de la Web automáticamente. En algunos casos, sin embargo, Reproductor de Windows Media recupera el documento ServiceInfo del equipo del usuario. Para obtener más información, vea [Setting the Initial Online Store](setting-the-initial-online-store.md).

Cuando Reproductor de Windows Media recupera el documento ServiceInfo de la Web, anexa una cadena de consulta a la dirección URL. La cadena de consulta contiene parámetros que proporcionan información sobre la configuración regional del usuario y la versión Reproductor de Windows Media usuario.

Puede crear documentos ServiceInfo estáticos o dinámicos. Un documento ServiceInfo estático tiene una extensión .xml de nombre de archivo. Un documento ServiceInfo dinámico es una página ASP y tiene una extensión de nombre de archivo .asp o .aspx.

No todos los elementos disponibles para su uso en el documento ServiceInfo se pueden usar en todas las tiendas en línea y algunos elementos son opcionales para todas las tiendas en línea. Para obtener información sobre los tipos de tiendas en línea que puede crear y las características disponibles para cada tipo, [vea Reproductor de Windows Media Online Stores](windows-media-player-online-stores.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Creación dinámica del documento ServiceInfo**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




