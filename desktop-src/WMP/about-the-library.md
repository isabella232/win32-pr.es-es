---
title: Acerca de la biblioteca
description: Acerca de la biblioteca
ms.assetid: a43c57ac-deb4-4c86-a8a2-bcfd214b9d0a
keywords:
- Reproductor de Windows Media,library
- Reproductor de Windows Media modelo de objetos,library
- object model,library
- Reproductor de Windows Media ActiveX control,library para el modelo de objetos
- ActiveX control,library para el modelo de objetos
- Reproductor de Windows Media Control de ActiveX móvil, biblioteca para el modelo de objetos
- Reproductor de Windows Media Móvil, biblioteca para el modelo de objetos
- Reproductor de Windows Media biblioteca, acerca de
- library,about
- metadata,Reproductor de Windows Media library
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1781329a78bcb2e9cb25c45135e03465b9d63df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073295"
---
# <a name="about-the-library"></a>Acerca de la biblioteca

La biblioteca es una base de datos de información, o *metadatos,* sobre el contenido multimedia digital que está disponible para Reproductor de Windows Media. Parte de la información se muestra en el panel **Biblioteca** del reproductor; más está disponible a través del código.

(En Reproductor de Windows Media serie 9 y versiones anteriores, esta característica se denomina **Biblioteca multimedia).**

La biblioteca proporciona a los usuarios una manera sencilla de organizar y acceder al contenido multimedia digital. Por ejemplo, los usuarios pueden ver la música organizada por álbum, por intérprete, por género o simplemente como una lista de todas las músicas. Puede usar el modelo de objetos del SDK de Reproductor de Windows Media para acceder a la biblioteca para reproducir contenido, recuperar listas de reproducción, agregar contenido, quitar contenido y cambiar los metadatos asociados. Reproductor de Windows Media proteger la privacidad de los usuarios al restringir la capacidad de acceder a la biblioteca desde el código en determinadas condiciones. Para obtener más información sobre los derechos de acceso, vea [Acceso a la biblioteca](library-access.md).

La biblioteca almacena metadatos sobre dos tipos básicos de contenido multimedia digital. El primer tipo, los elementos multimedia digitales, son archivos de contenido individuales, como una pista de música o una foto. El segundo tipo, listas de reproducción, son archivos que representan un grupo de elementos multimedia digitales, normalmente diseñados para reproducirse en un orden especificado. Los metadatos asociados con el contenido multimedia digital se almacenan como pares nombre-valor. Por ejemplo, los metadatos que describen la persona que realizó una canción se denominan "Artist" y el valor asociado a ella suele ser una cadena de texto que contiene el nombre del intérprete. Cada nombre de metadatos único se denomina *atributo*. Para obtener una lista de los atributos admitidos, vea [la Referencia de atributos](attribute-reference.md). Para obtener información sobre el uso de atributos en el código, vea [Atributos de elementos multimedia](media-item-attributes.md).

En las secciones siguientes se proporciona más información sobre cómo trabajar con la biblioteca:

-   [Acceso a la biblioteca mediante programación](accessing-the-library-programmatically.md)
-   [Acerca de los servicios de biblioteca](about-library-services.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos del reproductor**](about-the-player-object-model.md)
</dt> </dl>

 

 




