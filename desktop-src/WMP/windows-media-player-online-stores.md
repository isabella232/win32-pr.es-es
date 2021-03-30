---
title: Windows Media Player tiendas en línea
description: Windows Media Player tiendas en línea
ms.assetid: 81009d7b-5c2a-4447-a85e-138ab7834b7a
keywords:
- Windows Media Player tiendas en línea, acerca de
- tiendas en línea, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55046508b1e3a4d0a3a254fd294e5f271a2802f5
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789202"
---
# <a name="windows-media-player-online-stores"></a>Windows Media Player tiendas en línea

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

Windows Media Player proporciona una funcionalidad que permite a los proveedores de contenido multimedia digital integrar sus servicios con Windows Media Player. La integración entre el reproductor y un almacén multimedia en línea proporciona una experiencia muy agradable y completa para el usuario, lo que incluye la capacidad de buscar contenido, descargar y administrar archivos, reproducir contenido y copiar contenido en CDs o dispositivos.

## <a name="contacting-microsoft"></a>Contacto con Microsoft

Si desea que el almacén multimedia en línea se integre con Windows Media Player, pero aún no se ha puesto en contacto con Microsoft, puede empezar por enviar un correo electrónico al equipo virtual de Windows Media Player Services. La dirección de correo electrónico del equipo es mpsvctm@microsoft.com .

## <a name="for-more-information"></a>Para obtener más información

Para obtener orientación técnica sobre el uso de una variedad de SDK de Windows Media para crear un servicio que ofrezca contenido multimedia digital con licencia, vaya al [Centro para desarrolladores de Microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx) y busque "crear una tienda en línea de suscripciones de Windows Media Player 10".

## <a name="online-stores-in-windows-media-player-9-series"></a>Tiendas en línea en Windows Media Player 9 series

Windows Media Player 9 series presentó el concepto de tiendas en línea. En Windows Media Player 9 series, los proveedores de tiendas en línea podían integrar sus servicios en la característica **Premium Services** de Windows Media Player.

## <a name="online-stores-in-windows-media-player-10"></a>Tiendas en línea en Windows Media Player 10

En Windows Media Player 10, los servicios Premium se denominaban tiendas en línea y se agregaron las siguientes características nuevas:

-   Windows Media Player proporciona hasta tres paneles de tareas para su uso en la tienda en línea.
-   Cuando un usuario elige, en la interfaz de usuario del reproductor, para ver más información sobre el contenido multimedia digital, Windows Media Player llama a en la tienda en línea para proporcionar la información.
-   Cuando el usuario elige, en la interfaz de usuario del reproductor, para comprar un elemento multimedia, Windows Media Player llamada en la tienda en línea para administrar la compra.
-   La tienda en línea puede proporcionar un complemento al que Windows Media Player llama para obtener ayuda con la administración de derechos digitales y el tiempo de procesamiento en segundo plano.
-   Las tiendas en línea se pueden integrar con el programa de instalación de Windows Media Player.

## <a name="online-stores-in-windows-media-player-11"></a>Tiendas en línea en Windows Media Player 11

Windows Media Player 11 incorpora un nuevo tipo de tienda de música en línea, que se integra más profundamente en la interfaz de usuario del reproductor. En Windows Media Player 11, se han agregado las siguientes características nuevas para admitir este nuevo tipo de tienda en línea.

-   Windows Media Player descarga el catálogo multimedia de la tienda en línea, por lo que el usuario puede examinar el contenido de la tienda en línea rápidamente.
-   Windows Media Player muestra el contenido de música de la tienda en línea en el control de vista de árbol de la biblioteca.
-   Cuando el usuario navega en la interfaz de usuario del reproductor, el reproductor llama a en la tienda en línea para proporcionar páginas web que mejoran la experiencia del usuario.
-   La tienda en línea proporciona un complemento que controla todos los aspectos de la comunicación entre Windows Media Player y la tienda en línea. Por ejemplo, el complemento controla el inicio de sesión, la renovación de licencias, la actualización del catálogo, la descarga de contenido y la compra de contenido.
-   Windows Media Player proporciona una comunicación mejorada entre el reproductor y las páginas web proporcionadas por la tienda en línea y hospedadas en el reproductor.

## <a name="types-of-online-stores"></a>Tipos de tiendas en línea

Hay dos tipos de tiendas en línea: tipo 1 y tipo 2.

Un almacén de tipo 1 proporciona el nivel más avanzado de integración con Windows Media Player. Proporciona un catálogo de música descargable y está profundamente integrado en la interfaz de usuario del reproductor. Windows Media Player 11 y versiones posteriores admiten los almacenes de tipo 1.

Los almacenes de tipo 2, que son compatibles con Windows Media Player 9 series y versiones posteriores, tienen dos subcategorías: tiendas de comercio y almacenes de música.

Una tienda de comercio proporciona la experiencia más básica al proporcionar hasta tres paneles de tareas de servicio que muestran las páginas web del almacén.

Una tienda de música proporciona una experiencia más integrada para el usuario que una tienda de comercio. En una tienda de música, los usuarios pueden hacer clic en los botones y vínculos de Windows Media Player (fuera de las páginas web proporcionadas por el almacén) para realizar acciones como comprar un CD o DVD, obtener más información acerca de un elemento multimedia determinado o mostrar el panel de información de la vista del centro. En cada caso, Windows Media Player llama al almacén de música actual para controlar estas solicitudes.

> [!Note]  
> Algunos documentos hacen referencia a las tiendas de comercio como servicios comerciales básicos y hacen referencia a las tiendas de música como servicios de música integrados.

 

En la tabla siguiente se muestran las características disponibles para los diferentes tipos de tiendas en línea.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Característica</th>
<th>Tipo 2 de almacén de comercio</th>
<th>Tipo 2 de la tienda de música</th>
<th>Tipo 1 almacén</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Paneles de tareas crear servicio
<blockquote>
[!Note]<br />
Windows Media Player 10 tiene hasta tres paneles de tareas de servicio. Windows Media Player 11 solo tiene uno.
</blockquote>
<br/></td>
<td>Sí</td>
<td>Sí</td>
<td>Sí</td>
</tr>
<tr class="even">
<td>Cambie la apariencia del almacén cambiando los atributos como el color del botón, el color de la barra de tareas y el texto del botón.</td>
<td>Sí</td>
<td>Sí</td>
<td>Sí</td>
</tr>
<tr class="odd">
<td>Agregue imágenes de logotipo al menú y la barra de tareas de la tienda Windows Media Player online.</td>
<td>Sí</td>
<td>Sí</td>
<td>Sí</td>
</tr>
<tr class="even">
<td>Navegue desde HTMLView a la tienda en línea.</td>
<td>Sí</td>
<td>Sí</td>
<td>Sí</td>
</tr>
<tr class="odd">
<td>Administrar las solicitudes de Media Player de Windows para comprar un CD o DVD.</td>
<td>No</td>
<td>Sí</td>
<td>Sí</td>
</tr>
<tr class="even">
<td>Controlar las solicitudes de Media Player de Windows para proporcionar información de álbum enriquecida.</td>
<td>No</td>
<td>Sí</td>
<td>Sí</td>
</tr>
<tr class="odd">
<td>Proporcione la Página Web de la vista del centro de información.</td>
<td>No</td>
<td>Sí</td>
<td>Sí</td>
</tr>
<tr class="even">
<td>Personalizar Windows Media Player el programa de instalación para especificar una tienda en línea inicial.</td>
<td>No</td>
<td>Sí</td>
<td>Sí</td>
</tr>
<tr class="odd">
<td>Proporcione un complemento que implemente <a href="/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice"><strong>IWMPSubscriptionService</strong></a>.
<blockquote>
[!Note]<br />
En Windows Media Player 10 y versiones posteriores, este complemento también puede implementar <a href="/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2"><strong>IWMPSubscriptionService2</strong></a>.
</blockquote>
<br/></td>
<td>No</td>
<td>Sí</td>
<td>No</td>
</tr>
<tr class="even">
<td>Proporcionar un catálogo de música que descargue Windows Media Player</td>
<td>No</td>
<td>No</td>
<td>Sí</td>
</tr>
<tr class="odd">
<td>Proporcione páginas web personalizadas y menús contextuales basados en la navegación del usuario a través de la interfaz de usuario del reproductor.</td>
<td>No</td>
<td>No</td>
<td>Sí</td>
</tr>
<tr class="even">
<td>Proporcione un complemento que implemente <a href="/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner"><strong>IWMPContentPartner</strong></a>.</td>
<td>No</td>
<td>No</td>
<td>Sí</td>
</tr>
</tbody>
</table>



 

El resto de la documentación sobre las tiendas en línea se divide en las secciones siguientes.



| Sección                                                                                                                              | Descripción                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Kit de bienvenida de tiendas en línea](online-stores-welcome-kit.md)                                                                           | Contiene información acerca de cómo incorporar un almacén multimedia digital en línea en el panel de Windows Media Player.             |
| [Tipo 1 tiendas en línea](type-1-online-stores.md)                                                                                     | Contiene las secciones acerca de, guía y referencia de las tiendas en línea de tipo 1.                                             |
| [Tipo 2 tiendas en línea](type-2-online-stores.md)                                                                                     | Contiene las secciones acerca de, guía y referencia de las tiendas en línea de tipo 2.                                             |
| [Información común para las tiendas en línea de tipo 1 y 2](information-common-to-type-1-and-type-2-online-stores.md)                   | Contiene información que se aplica tanto a las tiendas en línea de tipo 1 como a las de tipo 2.                                          |
| [Actualización de licencias para almacenes que tienen el logotipo de PlaysForSure](refreshing-licenses-for-stores-that-have-the-playsforsure-logo.md) | Contiene información sobre cómo las tiendas en línea que no están integradas con Windows Media Player pueden actualizar licencias. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**SDK de Media Player de Windows**](windows-media-player-sdk.md)
</dt> </dl>

 

 





