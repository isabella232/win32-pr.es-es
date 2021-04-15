---
title: Acerca de la biblioteca
description: Acerca de la biblioteca
ms.assetid: a43c57ac-deb4-4c86-a8a2-bcfd214b9d0a
keywords:
- Windows Media Player, biblioteca
- Modelo de objetos de Windows Media Player, biblioteca
- modelo de objetos, biblioteca
- Control ActiveX de Windows Media Player, biblioteca para el modelo de objetos
- Control ActiveX, biblioteca para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, biblioteca para el modelo de objetos
- Windows Media Player Mobile, biblioteca para el modelo de objetos
- Biblioteca de Media Player de Windows, acerca de
- Biblioteca, acerca de
- metadatos, biblioteca de Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1781329a78bcb2e9cb25c45135e03465b9d63df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695232"
---
# <a name="about-the-library"></a>Acerca de la biblioteca

La biblioteca es una base de datos de información, o *metadatos*, sobre el contenido multimedia digital que está disponible para Windows Media Player. Parte de la información se muestra en el panel **biblioteca** del reproductor; hay más disponible a través del código.

(En Windows Media Player serie 9 y versiones anteriores, esta característica se denomina **biblioteca multimedia**).

La biblioteca ofrece a los usuarios una forma sencilla de organizar y acceder al contenido multimedia digital. Por ejemplo, los usuarios pueden ver música organizada por álbum, por intérprete, por género o simplemente como una lista de toda la música. Puede usar el modelo de objetos del SDK de Windows Media Player para tener acceso a la biblioteca para reproducir contenido, recuperar listas de reproducción, agregar contenido, quitar contenido y cambiar los metadatos asociados. Windows Media Player protege la privacidad de los usuarios al restringir la capacidad de obtener acceso a la biblioteca desde el código bajo ciertas condiciones. Para obtener más información sobre los derechos de acceso, consulte [acceso a la biblioteca](library-access.md).

La biblioteca almacena metadatos acerca de dos tipos básicos de contenido multimedia digital. El primer tipo, los elementos multimedia digitales, son archivos de contenido individuales, como una pista de música o una fotografía. El segundo tipo, las listas de reproducción, son archivos que representan un grupo de elementos multimedia digitales, que normalmente se prevé que se reproduzcan en un orden especificado. Los metadatos asociados con el contenido multimedia digital se almacenan como pares de nombre y valor. Por ejemplo, los metadatos que describen a la persona que realizó una canción se denominan "intérprete" y el valor asociado a él normalmente es una cadena de texto que contiene el nombre del remitente. Cada nombre de metadatos único se denomina *atributo*. Para obtener una lista de atributos admitidos, vea la [referencia de atributo](attribute-reference.md). Para obtener información sobre el uso de atributos en el código, vea [atributos de elemento multimedia](media-item-attributes.md).

En las secciones siguientes se proporciona más información sobre cómo trabajar con la biblioteca:

-   [Obtener acceso a la biblioteca mediante programación](accessing-the-library-programmatically.md)
-   [Acerca de los servicios de biblioteca](about-library-services.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos de Player**](about-the-player-object-model.md)
</dt> </dl>

 

 




