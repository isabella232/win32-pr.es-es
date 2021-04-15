---
title: Archivos de imagen
description: Archivos de imagen
ms.assetid: 93893610-de8d-4b9a-b23d-75ddb3e1e557
keywords:
- Aspectos de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a246ac411a3dfe2c5bab529ddcccce5596434617
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695460"
---
# <a name="art-files"></a>Archivos de imagen

Debe crear uno o varios archivos de imagen para la máscara. Sin arte, el usuario no tendrá nada que ver. Podría crear una máscara invisible, pero nadie la verá. E incluso después, todavía tendría que crear archivos de imagen para almacenar las imágenes invisibles, ya que el archivo de definición de máscara requiere archivos de imagen para elementos específicos.

Hay tres usos para las ilustraciones en las máscaras: imágenes principales, imágenes de asignación e imágenes alternativas.

## <a name="primary-images"></a>Imágenes principales

Debe crear una imagen primaria para la máscara. Esto es lo que verán los usuarios cuando instalen la máscara. La imagen principal se compone de una o varias imágenes que se crean mediante controles de máscara concretos.

Si tiene más de un control, debe especificar el orden z, que define los controles que se muestran delante de otros controles. Cada elemento de **vista** tendrá una imagen de fondo a la que puede agregar otras imágenes de elementos, lo que le permitirá crear una imagen compuesta principal.

También puede tener imágenes secundarias, como una bandeja deslizante, que no se muestran cuando se muestra la máscara por primera vez, pero que se muestran cuando el usuario realiza alguna acción. Estos siguen las mismas reglas que las imágenes principales, ya que se crean con un conjunto de controles.

## <a name="mapping-images"></a>Asignar imágenes

Una de las características más eficaces de las máscaras de Windows Media Player es que puede usar la asignación de imágenes para desencadenar eventos para su máscara. Los mapas de imágenes son archivos que contienen imágenes especiales. Sin embargo, las imágenes de un archivo de mapa de imágenes no están destinadas a ser vistas por el usuario, pero las usa Windows Media Player para realizar acciones cuando el usuario hace clic en la máscara.

Los distintos controles necesitan distintos tipos de mapas de imagen. Por ejemplo, si hace color de una parte de un mapa de imágenes un valor rojo específico y el usuario hace clic en el área correspondiente de la imagen principal, un botón activará un evento. El color se usa para definir qué eventos se desencadenan haciendo clic en un área determinada de la máscara.

## <a name="alternate-images"></a>Imágenes alternativas

También puede configurar imágenes alternativas para que se muestren cuando un usuario realiza alguna acción. Por ejemplo, puede crear una imagen alternativa de un botón que se mostrará solo cuando se mantenga el mouse sobre el botón. Esta es una buena manera de permitir que los usuarios sepan lo que pueden hacer y también permite una interfaz de usuario muy reconocible. Mediante el uso de la información sobre herramientas y las imágenes de desplazamiento detenidamente, puede crear interfaces de usuario inusuales que aún proporcionan los comentarios de los usuarios sobre las opciones disponibles.

En las secciones siguientes se proporciona más información acerca de los archivos de imagen:

-   [Imágenes principales](primary-images.md)
-   [Asignar imágenes](mapping-images.md)
-   [Imágenes alternativas](alternate-images.md)
-   [Formatos de archivo de imagen](art-file-formats.md)
-   [Ejemplo de arte sencillo](simple-art-example.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de máscara**](skin-files.md)
</dt> </dl>

 

 




