---
description: Un espacio de coordenadas es un espacio planar basado en el sistema de coordenadas cartesiano.
ms.assetid: 1a232030-8561-4b57-b274-dca0a8b3e3a1
title: Transformación de espacios de coordenadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27ffaec6a6dab09b841f95f4704048a4145d2b2bd84c232658b2b659d26d37be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965165"
---
# <a name="transformation-of-coordinate-spaces"></a>Transformación de espacios de coordenadas

Un *espacio de coordenadas* es un espacio planar basado en el sistema de coordenadas cartesiano. Este sistema proporciona un medio para especificar la ubicación de cada punto en un plano. Requiere dos ejes que son iguales de longitud. En la ilustración siguiente se muestra un espacio de coordenadas.

![ilustración de un espacio de coordenadas, que muestra el origen, ambos ejes y los valores máximo y mínimo de cada eje](images/cstrn-07.png)

El sistema admite cuatro espacios de coordenadas, como se describe en la tabla siguiente.



| Espacio de coordenadas | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| world            | Se usa opcionalmente como espacio de coordenadas inicial para transformaciones de gráficos. Permite el escalado, la traducción, la rotación, la cizallamiento y la reflexión. El espacio mundial mide 2^32 unidades de alto por 2^32 unidades de ancho.                                                                                                                                                                                                                                                                |
| página             | Se usa como el siguiente espacio después del espacio del mundo o como espacio inicial para las transformaciones de gráficos. Establece el modo de asignación. El espacio de página también mide 2^32 unidades de alto por 2^32 unidades de ancho.                                                                                                                                                                                                                                                                              |
| device           | Se usa como el siguiente espacio después del espacio de página. Solo permite la traducción, lo que garantiza que el origen del espacio del dispositivo se asigna a la ubicación adecuada en el espacio del dispositivo físico. El espacio del dispositivo mide 2^27 unidades de alto por 2^27 unidades de ancho.                                                                                                                                                                                                                                          |
| dispositivo físico  | Espacio final (salida) para transformaciones de gráficos. Normalmente hace referencia al área de cliente de la ventana de la aplicación; sin embargo, también puede incluir todo el escritorio, una ventana completa (incluido el marco, la barra de título y la barra de menús) o una página de papel de impresora o trazador, en función de la función que obtuvo el identificador para el contexto del dispositivo. Las dimensiones del dispositivo físico varían según las dimensiones establecidas por la tecnología de visualización, impresora o trazador. |



 

El espacio de página funciona con el espacio del dispositivo para proporcionar a las aplicaciones unidades independientes del dispositivo, como milímetros y pulgadas. Esta información general hace referencia tanto al espacio global como al espacio de página como espacio lógico.

Para representar la salida en un dispositivo físico, el sistema copia (o asigna) una región rectangular de un espacio de coordenadas en el siguiente mediante una transformación hasta que la salida aparece en su totalidad en el dispositivo físico. La asignación comienza en el espacio del mundo de la aplicación si la aplicación ha llamado a la [**función SetWorldTransform.**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) De lo contrario, la asignación se produce en el espacio de página. Como el sistema copia cada punto dentro de la región rectangular de un espacio en otro, aplica un algoritmo denominado transformación. Una *transformación* modifica (o transforma) el tamaño, la orientación y la forma de los objetos que se copian de un espacio de coordenadas en otro. Aunque una transformación afecta a un objeto en su conjunto, se aplica a cada punto o a cada línea del objeto.

En la ilustración siguiente se muestra una transformación típica realizada mediante la [**función SetWorldTransform.**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform)

![ilustración en la que se muestra un rectángulo que cambia de tamaño y posición a medida que aparece en el espacio del mundo, el espacio de página, el espacio del dispositivo y el dispositivo](images/cstrn-08.png)

 

 



