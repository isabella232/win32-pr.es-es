---
title: Indicadores de creación de transformación de CMM
description: CMMs usar marcas de creación de transformación como sugerencias para crear una transformación de color. Depende de la CMM determinar el mejor modo de usar estas marcas.
ms.assetid: f3942929-272c-4f08-98ac-a4d14d2f6ac4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852ef5c080c361bfffb6915d808787d46e63ba5c
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/02/2021
ms.locfileid: "105721163"
---
# <a name="cmm-transform-creation-flags"></a>Indicadores de creación de transformación de CMM

CMMs usar marcas de creación de transformación como sugerencias para crear una transformación de color. Depende de la CMM determinar el mejor modo de usar estas marcas.

Todas las funciones que utilizan estas marcas pasan o reciben valores de marca a través de un parámetro denominado *dwFlags*. La **palabra** de orden superior de *dwFlags* debe establecerse en un valor de la tabla siguiente.



| Constante                    | Descripción                                                                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| HABILITAR la comprobación de la \_ gama \_     | Use esta transformación para la comprobación de la gama.                                                                                                       |
| USAR \_ \_ colorimétrico relativo | No conserve el punto blanco. Si la gama de salida no admite un color determinado, use el color compatible más cercano. Consulte representación de los intentos. |
| \_traducción rápida             | Solo buscar color. No interpole el color.                                                                                            |
| PRESERVEBLACK               | Inserta la generación de negro adecuada GMMP como el último GMMP de la secuencia de transformación.                                                     |
| WCS \_ siempre                 | Use la ruta de acceso del código WCS incluso para las transformaciones ICC.                                                                                               |
| \_transformación secuencial       | Marca de creación de transformación para crear una transformación de color secuencial (no optimizado).                                                           |



 

La **palabra** de orden inferior puede tener uno de los siguientes valores constantes.



| Constante     | Descripción                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------|
| modo de prueba \_  | La transformación se usará para obtener una vista previa de la imagen. Calidad de imagen baja.                                    |
| \_modo normal | La transformación se usará para la presentación de imágenes normal. Calidad media de la imagen.                            |
| MEJOR \_ modo   | La transformación se usará para mostrar la imagen de mayor calidad posible en el dispositivo de destino. |



 

Al pasar del \_ modo de prueba al \_ modo mejor, la calidad de salida suele mejorar y transformar la disminución de velocidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos básicos de la administración del color](basic-color-management-concepts.md)
</dt> <dt>

[Constantes de ICM](wcs-constants.md)
</dt> </dl>

 

 




