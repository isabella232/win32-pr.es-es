---
title: Conversión de espacio de colores
description: Conversión de espacio de colores
ms.assetid: f5f1ec99-b3b9-4420-bf64-3872d9bbe650
keywords:
- SDK de Windows Media Format, conversión de espacio de colores
- Advanced Systems Format (ASF), conversión de espacio de colores
- ASF (formato de sistemas avanzados), conversión de espacio de colores
- conversión de espacio de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc284995cbc72aee148e12977dad9f4476b29c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268765"
---
# <a name="color-space-conversion"></a>Conversión de espacio de colores

A menudo hay una diferencia entre la profundidad de color del formato de vídeo comprimido en el perfil y el formato de entrada. Cuando esto sucede, el vídeo de origen se debe convertir para ajustarse al espacio de colores del destino. El escritor controla este proceso y se comunica con un convertidor de espacio de colores interno.

El lector también se comunica con el convertidor de espacio de colores para reconciliar las diferencias entre el formato comprimido y el formato de salida.

Como con todas las transformaciones realizadas en los datos, la conversión entre profundidades de color puede reducir la calidad del resultado. Cuando sea posible, debe usar los formatos de entrada y salida con la misma profundidad de color que el formato comprimido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de escritura de archivos**](file-writing-features.md)
</dt> <dt>

[**Trabajar con entradas**](working-with-inputs.md)
</dt> <dt>

[**Trabajar con salidas**](working-with-outputs.md)
</dt> </dl>

 

 




