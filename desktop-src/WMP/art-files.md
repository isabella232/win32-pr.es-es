---
title: Archivos de arte
description: Archivos de arte
ms.assetid: 93893610-de8d-4b9a-b23d-75ddb3e1e557
keywords:
- Reproductor de Windows Media máscaras, archivos art
- skins,art files
- archivos para máscaras, arte
- archivos de arte para máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89ccf07757e511f7717cbe3bbeff2cdacee004da8d3b64d27ddcef7ae2199a29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956375"
---
# <a name="art-files"></a>Archivos de arte

Debe crear uno o varios archivos de arte para la máscara. Sin arte, el usuario no tendrá nada que ver. Podría crear una máscara invisible, pero nadie la vería. E incluso entonces, tendría que crear archivos de arte para contener las imágenes invisibles, ya que el archivo de definición de máscara requiere archivos de arte para elementos específicos.

Hay tres usos de arte en máscaras: imágenes principales, imágenes de asignación e imágenes alternativas.

## <a name="primary-images"></a>Imágenes principales

Debe crear una imagen principal para la máscara. Esto es lo que verán los usuarios cuando instalen la máscara. La imagen principal se compone de una o varias imágenes creadas por controles de máscara específicos.

Si tiene más de un control, debe especificar el orden Z, que define qué controles se muestran delante de otros controles. Cada **elemento View** tendrá una imagen de fondo a la que puede agregar otras imágenes de elemento, lo que le permite crear una imagen compuesta principal.

También puede tener imágenes secundarias, como una bandeja deslizante, que no se muestran cuando aparece la máscara por primera vez, pero que se muestran cuando el usuario realiza alguna acción. Siguen las mismas reglas que las imágenes principales, en que se crean con un conjunto de controles.

## <a name="mapping-images"></a>Asignar imágenes

Una de las características más eficaces de las máscaras de Reproductor de Windows Media es que puede usar la asignación de imágenes para desencadenar eventos para la máscara. Los mapas de imágenes son archivos que contienen imágenes especiales. Sin embargo, las imágenes de un archivo de mapa de imagen no están pensadas para que las vea el usuario, sino que las usa Reproductor de Windows Media para tomar medidas cuando el usuario hace clic en la máscara.

Los distintos controles necesitan diferentes tipos de mapas de imágenes. Por ejemplo, si la parte de color de una imagen asigna un valor rojo específico y el usuario hace clic en el área correspondiente de la imagen principal, un botón mostrará un evento. El color se usa para definir qué eventos se desencadenan haciendo clic en un área determinada de la máscara.

## <a name="alternate-images"></a>Imágenes alternativas

También puede configurar imágenes alternativas para mostrar cuando un usuario hace algo. Por ejemplo, puede crear una imagen alternativa de un botón que se mostrará solo cuando el mouse mantenga el mouse sobre el botón. Esta es una buena manera de permitir que los usuarios sepan lo que pueden hacer y también permite una interfaz de usuario muy reconocible. Mediante el uso de información sobre herramientas y mantener el puntero de las imágenes con cuidado, puede crear interfaces de usuario inusuales que todavía dan comentarios al usuario sobre qué opciones están disponibles.

En las secciones siguientes se proporciona más información sobre los archivos de arte:

-   [Imágenes principales](primary-images.md)
-   [Asignar imágenes](mapping-images.md)
-   [Imágenes alternativas](alternate-images.md)
-   [Formatos de archivo art](art-file-formats.md)
-   [Ejemplo de arte simple](simple-art-example.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de máscara**](skin-files.md)
</dt> </dl>

 

 




