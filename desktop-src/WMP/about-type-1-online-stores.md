---
title: Acerca de las tiendas en línea de tipo 1
description: Acerca de las tiendas en línea de tipo 1
ms.assetid: 754b0097-5d28-4c1f-9847-a19cf23beaea
keywords:
- Reproductor de Windows Media en línea, escriba 1 tienda en línea
- tiendas en línea, escriba 1 tienda en línea
- tiendas en línea de tipo 1, acerca de
- Reproductor de Windows Media, escriba 1 tienda en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ecd939a03734fed121dcaa22c0d7ae89127476
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068493"
---
# <a name="about-type-1-online-stores"></a>Acerca de las tiendas en línea de tipo 1

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

Microsoft Reproductor de Windows Media 11 admite dos tipos de tiendas en línea: tipo 1 y tipo 2. Los almacenes de tipo 1 están más integrados en Reproductor de Windows Media que los almacenes de tipo 2. Una tienda en línea de tipo 1 proporciona un catálogo de música descargable para que Reproductor de Windows Media pueda hacer que el contenido de la tienda esté disponible para el usuario como si el contenido estuviera en la biblioteca multimedia local del usuario.

Un almacén en línea de tipo 1 debe proporcionar un complemento que implemente la [interfaz IWMPContentPartner.](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) A medida que el usuario navega en la interfaz de usuario de Reproductor de Windows Media, el reproductor llama al complemento para que la tienda en línea pueda mejorar la experiencia del usuario proporcionando páginas web que se muestran en el reproductor.

Entre las características de las tiendas en línea de tipo 1 que las distinguen de las tiendas de tipo 2 se incluyen las siguientes:

-   **Facilidad de uso.** Los usuarios pueden buscar música en el catálogo de la tienda en línea con la misma interfaz de usuario Reproductor de Windows Media que usan actualmente para administrar su biblioteca personal. Los usuarios solo pueden ver un único catálogo de tiendas en línea en la característica Examinar en un momento determinado.
-   **Conveniencia.** Los usuarios pueden muestrear o comprar música sin cambiar de la característica Examinar a otra parte de la interfaz Reproductor de Windows Media usuario.
-   **Características enriquecciones.** Dado que el catálogo de la tienda en línea se almacena de forma similar a la biblioteca del usuario, muchas de las características de la biblioteca Reproductor de Windows Media se pueden aplicar al catálogo. Por ejemplo, los usuarios pueden usar la rueda de palabras de la característica Examinar para filtrar el catálogo de tiendas en línea.

Para un proveedor de tienda en línea, las ventajas de proporcionar una tienda de tipo 1 en lugar de una tienda de tipo 2 incluyen las siguientes:

-   Nodo personalizado altamente visible en el árbol Reproductor de Windows Media biblioteca.
-   Un sistema diseñado para compras de música.
-   Conexiones mejoradas a los procesos del reproductor.
-   Un administrador de descarga mejor y más fácil de usar.
-   La capacidad de navegar entre varias características del Reproductor (incluida la apertura de nodos de árbol de biblioteca específicos).
-   Notificaciones sobre la expiración de la licencia para el contenido de la suscripción.
-   Notificaciones para trabajar con reproductores de música portátiles conectados.

En las secciones siguientes se proporciona información general sobre las tiendas en línea de tipo 1.



| Sección                                                                                              | Descripción                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Música Catálogo](music-catalog.md)                                                                   | Describe el catálogo de música proporcionado por la tienda en línea. Describe el compilador de catálogo proporcionado por Microsoft.                                                                     |
| [Contenedores de contenido](content-containers.md)                                                         | Describe la interfaz de contenedor de contenido ([IWMPContentContainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)), que se usa para representar una colección de elementos multimedia que se va a comprar o descargar. |
| [Integración de bibliotecas](library-integration.md)                                                       | Describe cómo se integra el catálogo de música de la tienda en línea en la vista de biblioteca del reproductor.                                                                                        |
| [Páginas de detección](discovery-pages.md)                                                               | Describe la interacción entre las Reproductor de Windows Media y las páginas web proporcionadas por la tienda en línea.                                                                                   |
| [Menús contextuales](context-menus.md)                                                                   | Describe cómo la tienda en línea puede proporcionar menús contextuales a medida que el usuario navega por la interfaz de usuario del reproductor.                                                                         |
| [Audio Secuencias](audio-streams.md)                                                                   | Describe cómo la tienda en línea proporciona Reproductor de Windows Media la dirección URL para el streaming de contenido de audio.                                                                              |
| [Documento ServiceInfo para una tienda en línea de tipo 1](serviceinfo-document-for-a-type-1-online-store.md) | Describe el documento XML ServiceInfo proporcionado por un almacén en línea de tipo 1.                                                                                                           |
| [Complemento de tienda en línea de tipo 1](type-1-online-store-plug-in.md)                                       | Describe el complemento que debe proporcionar una tienda en línea de tipo 1.                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tiendas en línea de tipo 1**](type-1-online-stores.md)
</dt> </dl>

 

 




