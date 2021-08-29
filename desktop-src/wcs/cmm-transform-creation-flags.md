---
title: Indicadores de creación de transformación de CMM
description: Las CMM usan marcas de creación de transformaciones como sugerencias para crear una transformación de color. Es la CMM la que determina la mejor manera de usar estas marcas.
ms.assetid: f3942929-272c-4f08-98ac-a4d14d2f6ac4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5b9e8ca5ba6ed9960ba819a417c7cbfe994a9cda1cdb81f3d1b855144a5f6a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934995"
---
# <a name="cmm-transform-creation-flags"></a>Indicadores de creación de transformación de CMM

Las CMM usan marcas de creación de transformaciones como sugerencias para crear una transformación de color. Es la CMM la que determina la mejor manera de usar estas marcas.

Todas las funciones que usan estas marcas pasan o reciben valores de marca a través de un parámetro denominado *dwFlags*. La palabra de **orden superior** de *dwFlags* debe establecerse en un valor de la tabla siguiente.



| Constante                    | Descripción                                                                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| HABILITACIÓN \_ DE LA COMPROBACIÓN DE \_ GAMUT     | Use esta transformación para la comprobación de la gama.                                                                                                       |
| USO \_ DE \_ COLORIMETRIC RELATIVO | No conserve el punto blanco. Si la gama de salida no admite un color determinado, use el color admitido más cercano. Vea Rendering Intents(Intenciones de representación). |
| \_FAST Traducir             | Buscar solo color. No interpola el color.                                                                                            |
| PRESERVEBLACK               | Inserta el GMMP de generación negra adecuado como el último GMMP en la secuencia de transformación.                                                     |
| WCS \_ ALWAYS                 | Use la ruta de acceso del código WCS incluso para las transformaciones DE LAN.                                                                                               |
| TRANSFORMACIÓN \_ SECUENCIAL       | Marca de creación de transformación para crear una transformación de color secuencial (no optimizada).                                                           |



 

WORD de orden **bajo** puede tener uno de los siguientes valores constantes.



| Constante     | Descripción                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------|
| MODO DE \_ PRUEBA  | La transformación se usará para obtener una vista previa de la imagen. Calidad de imagen baja.                                    |
| MODO \_ NORMAL | La transformación se usará para mostrar imágenes normales. Calidad media de la imagen.                            |
| MEJOR \_ MODO   | La transformación se usará para mostrar la imagen de mayor calidad posible en el dispositivo de destino. |



 

Al pasar del MODO DE PRUEBA al MEJOR MODO, la calidad de salida \_ generalmente mejora y disminuye la velocidad de \_ transformación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos básicos de administración de colores](basic-color-management-concepts.md)
</dt> <dt>

[ICM constantes](wcs-constants.md)
</dt> </dl>

 

 




