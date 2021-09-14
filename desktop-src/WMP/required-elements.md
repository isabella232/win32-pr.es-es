---
title: Elementos necesarios
description: Elementos necesarios
ms.assetid: 6aabbdcc-f834-4908-b25a-1dfce038132a
keywords:
- Reproductor de Windows Media Máscaras móviles, elementos
- skins,elements
- archivos de definición de máscara, elementos
- elementos, archivos de definición de máscara
- elements,Reproductor de Windows Media Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1f05ba51b83fad6585d24c3ad19830598b8975
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070903"
---
# <a name="required-elements"></a>Elementos necesarios

Debe proporcionar los siguientes elementos en el archivo de definición de máscara:

-   **Rúbrica.** Se requiere el encabezado del archivo de definición de máscara principal. Para obtener información sobre la versión del encabezado, vea la tabla de la [sección Creación de un archivo de definición de máscara.](creating-a-skin-definition-file.md)
-   **Sección Descripción.** La sección Descripción es necesaria al crear máscaras para Reproductor de Windows Media serie 9 para Windows Mobile. Debe ser la primera sección del archivo de definición de máscara y debe especificar valores válidos para Dimensiones. Especificar un valor para Orientation es opcional.
-   **Sección Mapas de bits.** Se requiere la sección Mapas de bits. Además, la sección Mapas de bits debe especificar nombres válidos para los archivos background, disabled, pushed, region y super image.
-   **archivos de imagen.** Debe proporcionar los archivos background, Disabled, Pushed, Region y Super image como parte de la máscara. Si va a crear máscaras para Reproductor de Windows Media 10 Mobile o posterior, no es necesario incluir archivos de región o de imagen super.

Si crea una máscara con solo imágenes definidas, la máscara estará visible, pero no ofrecerá ninguna funcionalidad significativa al usuario. Si decide crear una máscara sin botones, quizás para evitar que el usuario omita cierto contenido, tenga en cuenta que todavía es posible asignar funcionalidad a los botones de hardware del dispositivo.

Los archivos thumb son necesarios y las barras de seguimiento no se pueden usar sin thumbs.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivo de definición de máscara**](skin-definition-file-mobile.md)
</dt> </dl>

 

 




