---
description: Un espacio de coordenadas es un espacio plano basado en el sistema de coordenadas cartesiano.
ms.assetid: 1a232030-8561-4b57-b274-dca0a8b3e3a1
title: Transformación de espacios de coordenadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1bca3d7190c4566ea7548166134ff745cc5e2d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913741"
---
# <a name="transformation-of-coordinate-spaces"></a>Transformación de espacios de coordenadas

Un *espacio de coordenadas* es un espacio plano basado en el sistema de coordenadas cartesiano. Este sistema proporciona un medio para especificar la ubicación de cada punto en un plano. Requiere dos ejes que son perpendiculares y tienen la misma longitud. En la ilustración siguiente se muestra un espacio de coordenadas.

![Ilustración de un espacio de coordenadas, que muestra el origen, ambos ejes y los valores máximo y mínimo de cada eje](images/cstrn-07.png)

El sistema admite cuatro espacios de coordenadas, tal y como se describe en la tabla siguiente.



| Espacio de coordenadas | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| world            | Se utiliza opcionalmente como el espacio de coordenadas inicial para las transformaciones de gráficos. Permite el escalado, la traslación, la rotación, la cizalla y la reflexión. El espacio universal mide 2 ^ 32 unidades de alto por 2 ^ 32 unidades de ancho.                                                                                                                                                                                                                                                                |
| página             | Se usa como el siguiente espacio después del espacio universal o como espacio inicial para las transformaciones de gráficos. Establece el modo de asignación. El espacio de página también mide 2 ^ 32 unidades de alto por 2 ^ 32 unidades de ancho.                                                                                                                                                                                                                                                                              |
| device           | Se utiliza como espacio siguiente después del espacio de página. Solo permite la traducción, lo que garantiza que el origen del espacio del dispositivo se asigna a la ubicación adecuada en el espacio físico del dispositivo. El espacio de dispositivo mide 2 ^ 27 unidades de alto por 2 ^ 27 unidades de ancho.                                                                                                                                                                                                                                          |
| dispositivo físico  | El espacio final (de salida) para las transformaciones de gráficos. Normalmente hace referencia al área cliente de la ventana de la aplicación. sin embargo, también puede incluir todo el escritorio, una ventana completa (que incluye el marco, la barra de título y la barra de menús), o una página de papel de impresora o de trazado, dependiendo de la función que haya obtenido el identificador del contexto del dispositivo. Las dimensiones del dispositivo físico varían según las dimensiones establecidas por la tecnología de pantalla, impresora o trazador. |



 

El espacio de la página funciona con el espacio del dispositivo para proporcionar a las aplicaciones unidades independientes del dispositivo, como milímetros y pulgadas. En esta información general se hace referencia tanto al espacio universal como al espacio de página como espacio lógico.

Para describir la salida en un dispositivo físico, el sistema copia (o asigna) una región rectangular de un espacio de coordenadas en el siguiente utilizando una transformación hasta que la salida aparece en su totalidad en el dispositivo físico. La asignación comienza en el espacio global de la aplicación si la aplicación ha llamado a la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) . de lo contrario, la asignación se produce en el espacio de la página. A medida que el sistema copia cada punto dentro de la región rectangular de un espacio en otro, aplica un algoritmo denominado transformación. Una *transformación* modifica (o transforma) el tamaño, la orientación y la forma de los objetos que se copian de un espacio de coordenadas en otro. Aunque una transformación afecta a un objeto en su totalidad, se aplica a cada punto o a cada línea en el objeto.

En la ilustración siguiente se muestra una transformación típica realizada mediante la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) .

![Ilustración en la que se muestra un rectángulo que cambia el tamaño y la posición tal como aparece en el espacio universal, el espacio de la página, el espacio del dispositivo y el dispositivo.](images/cstrn-08.png)

 

 



