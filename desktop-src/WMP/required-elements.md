---
title: Elementos necesarios
description: Elementos necesarios
ms.assetid: 6aabbdcc-f834-4908-b25a-1dfce038132a
keywords:
- Aspectos móviles de Windows Media Player, elementos
- aspectos, elementos
- archivos de definición de máscara, elementos
- elementos, archivos de definición de máscara
- elementos, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1f05ba51b83fad6585d24c3ad19830598b8975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776411"
---
# <a name="required-elements"></a>Elementos necesarios

Debe proporcionar los elementos siguientes en el archivo de definición de máscara:

-   **Encabezado.** El encabezado principal del archivo de definición de máscara es obligatorio. Para obtener información sobre la versión de encabezado, vea la tabla en la sección [creación de un archivo de definición de máscara](creating-a-skin-definition-file.md) .
-   **Sección de descripción.** La sección Descripción es necesaria cuando se crean máscaras para Windows Media Player 9 series para Windows Mobile. Debe ser la primera sección del archivo de definición de máscara y debe especificar valores válidos para las dimensiones. Especificar un valor para la orientación es opcional.
-   **Sección de mapas de bits.** La sección de mapas de bits es obligatoria. Además, la sección de mapas de bits debe especificar nombres válidos para los archivos de fondo, deshabilitado, insertado, región y súper imagen.
-   **archivos de imagen.** Debe proporcionar los archivos Background, Disabled, Push, region y Super Image como parte de la máscara. Si va a crear máscaras para Windows Media Player 10 Mobile o posterior, no es necesario incluir archivos de región o de superimagen.

Si crea una máscara solo con imágenes definidas, la máscara será visible, pero no proporcionará ninguna funcionalidad significativa al usuario. Si decide crear una máscara sin botones, quizás para evitar que el usuario omita un determinado contenido, tenga en cuenta que todavía es posible asignar funcionalidad a los botones de hardware del dispositivo.

Los archivos Thumb son obligatorios y el trackbars no se puede usar sin Thumbs.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivo de definición de máscara**](skin-definition-file-mobile.md)
</dt> </dl>

 

 




