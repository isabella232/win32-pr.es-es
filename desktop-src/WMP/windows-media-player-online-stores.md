---
title: Reproductor de Windows Media Tiendas en línea
description: Reproductor de Windows Media Tiendas en línea
ms.assetid: 81009d7b-5c2a-4447-a85e-138ab7834b7a
keywords:
- Reproductor de Windows Media en línea, acerca de
- tiendas en línea, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11cba4cabcaaae5e55a4e93dbbfe9e4c19e73b37
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478590"
---
# <a name="windows-media-player-online-stores"></a>Reproductor de Windows Media Tiendas en línea

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

Reproductor de Windows Media proporciona funcionalidad que permite a los proveedores de contenido multimedia digital integrar sus servicios con Reproductor de Windows Media. La integración entre el reproductor y un almacén de medios digitales en línea proporciona una experiencia completa y cómoda para el usuario, incluida la capacidad de buscar contenido, descargar y administrar archivos, reproducir contenido y copiar contenido en CD o dispositivos.

## <a name="contacting-microsoft"></a>Ponerse en contacto con Microsoft

Si desea que el almacén de medios digitales en línea se integre con Reproductor de Windows Media, pero aún no se ha puesto en contacto con Microsoft, puede empezar enviando un correo electrónico al equipo virtual de Reproductor de Windows Media Services. La dirección de correo electrónico del equipo es mpsvctm@microsoft.com .

## <a name="for-more-information"></a>Para obtener más información

Para obtener instrucciones técnicas sobre el uso de diversos SDK de Windows Media para crear un servicio que ofrece contenido multimedia digital con licencia, vaya al Centro para desarrolladores de [Microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx) y busque "Creación de una tienda en línea de suscripción a Reproductor de Windows Media 10".

## <a name="online-stores-in-windows-media-player-9-series"></a>Tiendas en línea de Reproductor de Windows Media serie 9

Reproductor de Windows Media serie 9 introdujo el concepto de tiendas en línea. En Reproductor de Windows Media serie 9, los proveedores de tiendas en línea podían integrar sus servicios en la **característica Premium Services** de Reproductor de Windows Media.

## <a name="online-stores-in-windows-media-player-10"></a>Tiendas en línea en Reproductor de Windows Media 10

En Reproductor de Windows Media 10, se cambió el nombre de los servicios Premium a las tiendas en línea y se agregaron las siguientes características nuevas:

-   Reproductor de Windows Media proporciona hasta tres paneles de tareas para que los use el almacén en línea.
-   Cuando un usuario elige, en la interfaz de usuario del reproductor, ver más información sobre el contenido multimedia digital, Reproductor de Windows Media llamadas a en la tienda en línea para proporcionar la información.
-   Cuando el usuario elige, en la interfaz de usuario del reproductor, comprar un elemento multimedia, Reproductor de Windows Media llamar a en la tienda en línea para controlar la compra.
-   La tienda en línea puede proporcionar un complemento que requiere Reproductor de Windows Media ayuda con la administración de derechos digitales y el tiempo de procesamiento en segundo plano.
-   Las tiendas en línea se pueden integrar Reproductor de Windows Media configuración.

## <a name="online-stores-in-windows-media-player-11"></a>Tiendas en línea en Reproductor de Windows Media 11

Reproductor de Windows Media 11 presenta un nuevo tipo de tienda de música en línea, que está más integrado en la interfaz de usuario del reproductor. En Reproductor de Windows Media 11, se han agregado las siguientes características nuevas para admitir este nuevo tipo de tienda en línea.

-   Reproductor de Windows Media el catálogo multimedia de la tienda en línea, para que el usuario pueda examinar rápidamente el contenido de la tienda en línea.
-   Reproductor de Windows Media muestra el contenido de música de la tienda en línea en el control de vista de árbol de biblioteca.
-   A medida que el usuario navega en la interfaz de usuario del reproductor, el reproductor llama a en la tienda en línea para proporcionar páginas web que mejoren la experiencia del usuario.
-   La tienda en línea proporciona un complemento que controla todos los aspectos de la comunicación entre Reproductor de Windows Media y la tienda en línea. Por ejemplo, el complemento controla el inicio de sesión, la renovación de licencias, la actualización del catálogo, la descarga de contenido y la compra de contenido.
-   Reproductor de Windows Media proporciona una comunicación mejorada entre el reproductor y las páginas web proporcionadas por la tienda en línea y hospedadas en el reproductor.

## <a name="types-of-online-stores"></a>Tipos de tiendas en línea

Hay dos tipos de tiendas en línea: tipo 1 y tipo 2.

Un almacén de tipo 1 proporciona el nivel más avanzado de integración con Reproductor de Windows Media. Proporciona un catálogo de música descargable y está profundamente integrado en la interfaz de usuario del reproductor. Los almacenes de tipo 1 son compatibles con Reproductor de Windows Media 11 y versiones posteriores.

Las tiendas de tipo 2, que son compatibles con Reproductor de Windows Media serie 9 y versiones posteriores, tienen dos subcategorías: tiendas de comercio y tiendas de música.

Una tienda de comercio proporciona la experiencia más básica al proporcionar hasta tres paneles de tareas de servicio que muestran las páginas web de la tienda.

Una tienda de música proporciona una experiencia más integrada para el usuario que una tienda de comercio. En una tienda de música, los usuarios pueden hacer clic en botones y vínculos en Reproductor de Windows Media (fuera de las páginas web proporcionadas por la tienda) para realizar acciones como comprar un CD o DVD, obtener más información sobre un elemento multimedia determinado o mostrar el panel Vista del Centro de información. En cada caso, Reproductor de Windows Media llama a la tienda de música actual para controlar estas solicitudes.

> [!Note]  
> Algunos documentos hacen referencia a las tiendas comerciales como servicios comerciales básicos y hacen referencia a las tiendas de música como servicios de música integrados.

 

En la tabla siguiente se muestran las características disponibles para los distintos tipos de tiendas en línea.




| Característica | Tienda de comercio de tipo 2 | Tienda de música de tipo 2 | Almacén de tipo 1 | 
|---------|-----------------------|--------------------|--------------|
| Crear paneles de tareas de servicio<blockquote>[!Note]<br />Reproductor de Windows Media 10 tiene hasta tres paneles de tareas de servicio. Reproductor de Windows Media 11 solo tiene uno.</blockquote><br /> | Sí | Sí | Sí | 
| Cambie la apariencia del almacén cambiando atributos como el color del botón, el color de la barra de tareas y el texto del botón. | Sí | Sí | Sí | 
| Agregue imágenes de logotipo al menú Reproductor de Windows Media y la barra de tareas de la tienda en línea. | Sí | Sí | Sí | 
| Vaya de HTMLView a la tienda en línea. | Sí | Sí | Sí | 
| Controle Reproductor de Windows Media solicitudes para comprar un CD o DVD. | No | Sí | Sí | 
| Controle Reproductor de Windows Media solicitudes para proporcionar información completa del álbum. | No | Sí | Sí | 
| Proporcione la página web vista del Centro de información. | No | Sí | Sí | 
| Personalice Reproductor de Windows Media configuración para especificar una tienda en línea inicial. | No | Sí | Sí | 
| Proporcione un complemento que implemente <a href="/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice"><strong>IWMPSubscriptionService</strong></a>.<blockquote>[!Note]<br />En Reproductor de Windows Media 10 y versiones posteriores, este complemento también puede implementar <a href="/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2"><strong>IWMPSubscriptionService2</strong></a>.</blockquote><br /> | No | Sí | No | 
| Proporcione un catálogo de música descargado por Reproductor de Windows Media | No | No | Sí | 
| Proporcione páginas web personalizadas y menús contextuales basados en la navegación del usuario a través de la interfaz de usuario del reproductor. | No | No | Sí | 
| Proporcione un complemento que implemente <a href="/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner"><strong>IWMPContentPartner</strong></a>. | No | No | Sí | 




 

El resto de la documentación sobre las tiendas en línea se divide en las secciones siguientes.



| Sección                                                                                                                              | Descripción                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Kit de bienvenida de tiendas en línea](online-stores-welcome-kit.md)                                                                           | Contiene información sobre cómo traer un almacén de medios digitales en línea a Reproductor de Windows Media.             |
| [Tiendas en línea de tipo 1](type-1-online-stores.md)                                                                                     | Contiene las secciones Acerca de, Guía y Referencia de las tiendas en línea de tipo 1.                                             |
| [Tiendas en línea de tipo 2](type-2-online-stores.md)                                                                                     | Contiene las secciones Acerca de, Guía y Referencia de las tiendas en línea de tipo 2.                                             |
| [Información común a las tiendas en línea de tipo 1 y tipo 2](information-common-to-type-1-and-type-2-online-stores.md)                   | Contiene información que se aplica a las tiendas en línea de tipo 1 y tipo 2.                                          |
| [Actualizar licencias para tiendas que tienen el logotipo PlaysForSure](refreshing-licenses-for-stores-that-have-the-playsforsure-logo.md) | Contiene información sobre cómo las tiendas en línea que no están integradas con Reproductor de Windows Media pueden actualizar las licencias. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Reproductor de Windows Media SDK**](windows-media-player-sdk.md)
</dt> </dl>

 

 





