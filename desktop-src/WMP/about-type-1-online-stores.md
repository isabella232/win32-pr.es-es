---
title: Acerca de las tiendas en línea de tipo 1
description: Acerca de las tiendas en línea de tipo 1
ms.assetid: 754b0097-5d28-4c1f-9847-a19cf23beaea
keywords:
- Windows Media Player tiendas en línea, escriba 1 tiendas en línea
- tiendas en línea, tipo 1 tiendas en línea
- tipo 1 tiendas en línea, acerca de
- Windows Media Player, escriba 1 tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ecd939a03734fed121dcaa22c0d7ae89127476
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695556"
---
# <a name="about-type-1-online-stores"></a>Acerca de las tiendas en línea de tipo 1

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

Microsoft Windows Media Player 11 admite dos tipos de tiendas en línea: tipo 1 y tipo 2. Los almacenes de tipo 1 se integran más profundamente en Windows Media Player que los almacenes de tipo 2. Una tienda en línea de tipo 1 proporciona un catálogo de música descargable para que Windows Media Player pueda hacer que el contenido de la tienda esté disponible para el usuario como si estuviera en la biblioteca multimedia local del usuario.

Una tienda en línea de tipo 1 debe proporcionar un complemento que implemente la interfaz [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) . Cuando el usuario navega en la interfaz de usuario de Windows Media Player, el reproductor llama al complemento para que la tienda en línea pueda mejorar la experiencia del usuario al proporcionar páginas web que se muestran en el reproductor.

Entre las características de las tiendas en línea de tipo 1 que las distinguen de los almacenes de tipo 2 se incluyen las siguientes:

-   **Facilidad de uso.** Los usuarios pueden buscar música desde el catálogo de la tienda en línea con la misma interfaz de usuario conocida de Windows Media Player que usan actualmente para administrar su biblioteca personal. Los usuarios solo pueden ver un catálogo de la tienda en línea en la característica de exploración en un momento determinado.
-   **Prácticos.** Los usuarios pueden hacer un muestreo o comprar música sin cambiar de la característica de exploración a otra parte de la interfaz de usuario de Windows Media Player.
-   **Características enriquecidas.** Dado que el catálogo de la tienda en línea se almacena de manera similar a la biblioteca del usuario, muchas de las características de la biblioteca de Windows Media Player se pueden aplicar al catálogo. Por ejemplo, los usuarios pueden usar la rueda de palabras de la característica examinar para filtrar el catálogo de la tienda en línea.

Para un proveedor de tienda en línea, las ventajas de proporcionar un almacén de tipo 1 en lugar de un almacén de tipo 2 incluyen lo siguiente:

-   Un nodo personalizado muy visible en el árbol de la biblioteca de Media Player de Windows.
-   Un sistema diseñado para compras de música.
-   Conexiones mejoradas para los procesos del reproductor.
-   Un administrador de descargas mejor y más fácil de usar.
-   La capacidad de navegar entre varias características del reproductor (incluida la apertura de nodos de árbol de biblioteca específicos).
-   Notificaciones sobre la expiración de la licencia para el contenido de la suscripción.
-   Notificaciones para trabajar con reproductores de música portátiles conectados.

En las secciones siguientes se proporciona información general sobre las tiendas en línea de tipo 1.



| Sección                                                                                              | Descripción                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Catálogo de música](music-catalog.md)                                                                   | Describe el catálogo de música proporcionado por la tienda en línea. Describe el compilador de catálogo proporcionado por Microsoft.                                                                     |
| [Contenedores de contenido](content-containers.md)                                                         | Describe la interfaz de contenedor de contenido ([IWMPContentContainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)), que se usa para representar una colección de elementos multimedia que se van a comprar o descargar. |
| [Integración de biblioteca](library-integration.md)                                                       | Describe cómo se integra el catálogo de música de la tienda en línea en la vista biblioteca del reproductor.                                                                                        |
| [Páginas de detección](discovery-pages.md)                                                               | Describe la interacción entre Windows Media Player y las páginas web proporcionadas por la tienda en línea.                                                                                   |
| [Menús contextuales](context-menus.md)                                                                   | Describe cómo la tienda en línea puede proporcionar menús contextuales a medida que el usuario navega por la interfaz de usuario del reproductor.                                                                         |
| [Secuencias de audio](audio-streams.md)                                                                   | Describe cómo la tienda en línea proporciona Windows Media Player con la dirección URL para el contenido de audio de transmisión por secuencias.                                                                              |
| [Documento ServiceInfo para una tienda en línea de tipo 1](serviceinfo-document-for-a-type-1-online-store.md) | Describe el documento XML ServiceInfo proporcionado por un almacén en línea de tipo 1.                                                                                                           |
| [Escriba 1 complemento de tienda en línea](type-1-online-store-plug-in.md)                                       | Describe el complemento que debe proporcionar un almacén en línea de tipo 1.                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tipo 1 tiendas en línea**](type-1-online-stores.md)
</dt> </dl>

 

 




