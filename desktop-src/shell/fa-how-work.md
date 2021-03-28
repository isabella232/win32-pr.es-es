---
description: Las asociaciones de archivo definen cómo el shell trata un tipo de archivo en el sistema.
ms.assetid: A1C05857-26F8-4d4a-977B-4782E8AFA317
title: Cómo funcionan las asociaciones de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cf307e40bb6165da4a2547fb8dafc1791a11ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276767"
---
# <a name="how-file-associations-work"></a>Cómo funcionan las asociaciones de archivos

Las asociaciones de archivo definen cómo el shell trata un [tipo de archivo](fa-file-types.md) en el sistema.

Este tema se organiza de la siguiente manera:

-   [Acerca de las asociaciones de archivos](#about-file-associations)
-   [Cuándo debe implementar o modificar las asociaciones de archivos](#when-you-should-implement-or-modify-file-associations)
-   [Cómo funcionan las asociaciones de archivos](#how-file-associations-work)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="about-file-associations"></a>Acerca de las asociaciones de archivos

Las asociaciones de archivos controlan la siguiente funcionalidad:

-   La aplicación que se inicia cuando un usuario hace doble clic en un archivo.
-   El icono que aparece para un archivo de forma predeterminada.
-   Cómo aparece el tipo de archivo cuando se ve en el explorador de Windows.
-   Qué comandos aparecen en el menú contextual de un archivo.
-   Otras características de la interfaz de usuario, como información sobre herramientas, información de mosaico y el panel de detalles.

Los desarrolladores de aplicaciones pueden usar asociaciones de archivos para controlar el modo en que el shell trata los tipos de archivo personalizados o para asociar una aplicación a los tipos de archivo existentes. Por ejemplo, cuando se instala una aplicación, la aplicación puede comprobar la presencia de las asociaciones de archivos existentes y crear o invalidar esas asociaciones de archivo.

Los usuarios pueden controlar algunos aspectos de las asociaciones de archivos para personalizar el modo en que el shell trata un tipo de archivo mediante la interfaz de usuario **abrir con** o editando el registro.

En la ventana del explorador de Windows que se muestra en la captura de pantalla siguiente, el shell muestra iconos diferentes para cada archivo, en función del icono asociado al tipo de archivo. Si el usuario hace doble clic en la **imagen de mapa de bits de ejemplo** de archivo, el shell inicia Paint y lo usa para abrir el archivo porque en este sistema, Paint está asociado a archivos. bmp. Las personas pueden controlar estas acciones mediante asociaciones de archivo.

![Ilustración de cómo funcionan las asociaciones de archivos en la práctica](images/file-assoc/fileassoc-icons.png)

## <a name="when-you-should-implement-or-modify-file-associations"></a>Cuándo debe implementar o modificar las asociaciones de archivos

Las aplicaciones pueden usar archivos para varios propósitos: algunos archivos se usan exclusivamente en la aplicación y no suelen tener acceso a ellos los usuarios, mientras que otros archivos son creados por el usuario y se suelen abrir, buscar y ver desde el shell.

A menos que la aplicación use exclusivamente el tipo de archivo personalizado, debe implementar las asociaciones de archivo para él. Como norma general, implemente asociaciones de archivo para el tipo de archivo personalizado si espera que el usuario interactúe directamente con estos archivos de cualquier manera. Esto incluye el uso del shell para examinar y abrir los archivos, buscar el contenido o las propiedades de los archivos y obtener una vista previa de los archivos.

Si la aplicación controla un tipo de archivo existente, no modifique la Asociación de archivo a menos que desee modificar la forma en que el shell controla todos los archivos de este tipo.

## <a name="how-file-associations-work"></a>Cómo funcionan las asociaciones de archivos

Los archivos se exponen en el shell como elementos de Shell. Para controlar las asociaciones de archivos, los desarrolladores de aplicaciones pueden registrar una asignación entre el tipo de archivo y los controladores (objetos COM que proporcionan funcionalidad para los elementos de Shell del tipo de archivo). Cuando el shell necesita consultar las asociaciones de archivo de un tipo de archivo, crea una matriz de claves del registro que contienen las asociaciones para el tipo de archivo y comprueba estas claves para que las asociaciones de archivos correspondientes las utilicen.

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener información conceptual sobre las asociaciones de archivos, vea [información general sobre verbos y asociaciones de archivo](fa-verbs.md).

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

[Controladores de tipo de archivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores de programación](fa-progids.md)
</dt> <dt>

[Tipos percibidos](fa-perceivedtypes.md)
</dt> <dt>

[Matrices de asociación](fa-associationarray.md)
</dt> </dl>

 

 



