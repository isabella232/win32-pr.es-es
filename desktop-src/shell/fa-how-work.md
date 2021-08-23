---
description: Las asociaciones de archivo definen cómo el Shell trata un tipo de archivo en el sistema.
ms.assetid: A1C05857-26F8-4d4a-977B-4782E8AFA317
title: Cómo funcionan las asociaciones de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd12386ec7e850d160a6377ddff9b807e6dccfe101ad45285bdc9d7f2661a0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032734"
---
# <a name="how-file-associations-work"></a>Cómo funcionan las asociaciones de archivos

Las asociaciones de archivo definen cómo el Shell trata un [tipo de archivo](fa-file-types.md) en el sistema.

Este tema se organiza de la siguiente manera:

-   [Acerca de las asociaciones de archivos](#about-file-associations)
-   [Cuándo debe implementar o modificar asociaciones de archivo](#when-you-should-implement-or-modify-file-associations)
-   [Cómo funcionan las asociaciones de archivos](#how-file-associations-work)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="about-file-associations"></a>Acerca de las asociaciones de archivos

Las asociaciones de archivo controlan la funcionalidad siguiente:

-   La aplicación se inicia cuando un usuario hace doble clic en un archivo.
-   El icono que aparece para un archivo de forma predeterminada.
-   Cómo aparece el tipo de archivo cuando se ve en Windows Explorer.
-   Qué comandos aparecen en el menú contextual de un archivo.
-   Otras características de la interfaz de usuario, como información sobre herramientas, información de icono y el panel de detalles.

Los desarrolladores de aplicaciones pueden usar asociaciones de archivo para controlar cómo el Shell trata los tipos de archivo personalizados o para asociar una aplicación a los tipos de archivo existentes. Por ejemplo, cuando se instala una aplicación, la aplicación puede comprobar la presencia de asociaciones de archivo existentes y crear o invalidar esas asociaciones de archivo.

Los usuarios pueden controlar algunos aspectos de las asociaciones de archivo  para personalizar cómo el Shell trata un tipo de archivo mediante la interfaz de usuario Abrir con o editando el Registro.

En la Windows Explorer que se muestra en la captura de pantalla siguiente, el Shell muestra iconos diferentes para cada archivo, en función del icono asociado al tipo de archivo. Si el usuario hace doble clic en el archivo Imagen de mapa de bits de ejemplo **,** el shell inicia Paint y lo usa para abrir el archivo porque en este sistema, Paint está asociado a .bmp archivos. Los usuarios pueden controlar estas acciones mediante asociaciones de archivo.

![ilustración de cómo funcionan las asociaciones de archivos en la práctica](images/file-assoc/fileassoc-icons.png)

## <a name="when-you-should-implement-or-modify-file-associations"></a>Cuándo debe implementar o modificar asociaciones de archivo

Las aplicaciones pueden usar archivos para varios propósitos: algunos archivos los usa exclusivamente la aplicación y los usuarios no suelen tener acceso a ellos, mientras que otros archivos los crea el usuario y a menudo se abren, buscan y ven desde el Shell.

A menos que la aplicación utilice exclusivamente el tipo de archivo personalizado, debe implementar asociaciones de archivo para él. Como regla general, implemente asociaciones de archivo para el tipo de archivo personalizado si espera que el usuario interactúe directamente con estos archivos de cualquier manera. Esto incluye el uso del Shell para examinar y abrir los archivos, buscar el contenido o las propiedades de los archivos y obtener una vista previa de los archivos.

Si la aplicación controla un tipo de archivo existente, no modifique la asociación de archivos a menos que desee modificar la forma en que el Shell controla todos los archivos de este tipo.

## <a name="how-file-associations-work"></a>Cómo funcionan las asociaciones de archivos

Los archivos se exponen en el shell como elementos de Shell. Para controlar las asociaciones de archivo, los desarrolladores de aplicaciones pueden registrar una asignación entre el tipo de archivo y los controladores (objetos COM que proporcionan funcionalidad para los elementos shell del tipo de archivo). Cuando el Shell necesita consultar las asociaciones de archivo de un tipo de archivo, crea una matriz de claves del Registro que contiene las asociaciones para el tipo de archivo y comprueba estas claves para las asociaciones de archivo adecuadas que se usarán.

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener información conceptual sobre las asociaciones de archivos, vea [Información general de verbos y asociaciones de archivo.](fa-verbs.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones](app-registration.md)
</dt> <dt>

[Tipos de archivo](fa-file-types.md)
</dt> <dt>

[Vista de contenido por tipo de archivo o tipo](prophand-content-view.md)
</dt> <dt>

[Comprobador de tipo de archivo](file-type-verifier.md)
</dt> <dt>

[Controladores de tipos de archivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores de programación](fa-progids.md)
</dt> <dt>

[Tipos percibidos](fa-perceivedtypes.md)
</dt> <dt>

[Matrices de asociación](fa-associationarray.md)
</dt> </dl>

 

 



