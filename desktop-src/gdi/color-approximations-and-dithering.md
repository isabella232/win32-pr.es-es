---
description: Aunque una aplicación puede usar el color sin tener en cuenta las capacidades de color del dispositivo, es posible que la salida resultante no sea tan informativa y agradable como resultado para qué color se elige cuidadosamente.
ms.assetid: 008c8a8e-3456-4727-9b27-00b20ae880a2
title: Aproximaciones de color y interpolación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a72e28dbc3ce20a42b53b5ff060d950719e2d861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155669"
---
# <a name="color-approximations-and-dithering"></a>Aproximaciones de color y interpolación

Aunque una aplicación puede usar el color sin tener en cuenta las capacidades de color del dispositivo, es posible que la salida resultante no sea tan informativa y agradable como resultado para qué color se elige cuidadosamente. Algunos dispositivos, si los hay, garantizan una coincidencia exacta para cada valor de color posible; por lo tanto, si una aplicación solicita un color que el dispositivo no puede generar, el sistema lo aproxima mediante el uso de un color que el dispositivo puede generar. Por ejemplo, si una aplicación intenta crear un lápiz rojo para una impresora en blanco y negro, recibirá un lápiz negro en su lugar, el sistema utilizará el negro como aproximación de rojo.

Una aplicación puede detectar si el sistema va a aproximar un color determinado mediante la función [**GetNearestColor**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestcolor) . La función toma un valor de color y devuelve el valor de color del color de coincidencia más cercano que el dispositivo puede generar. El método que utiliza el sistema para determinar esta aproximación depende del controlador del dispositivo y de sus capacidades de color. En la mayoría de los casos, la intensidad total del color aproximado es la más cercana a la del color solicitado.

Cuando una aplicación crea un lápiz o establece el color del texto, el sistema siempre aproxima un color si no existe ninguna coincidencia exacta. Cuando una aplicación crea un pincel sólido, el sistema puede intentar simular el color solicitado mediante la interpolación. La *interpolación* simula un color alternando dos o más colores en un patrón. Por ejemplo, se pueden simular diferentes tonalidades de color rosa alternando diferentes combinaciones de rojo y blanco. En función de los colores y del modelo, el tramado puede producir simulaciones razonables. Resulta muy útil para los dispositivos monocromáticos, ya que amplía el número de "colores" disponibles más allá del blanco y negro sencillos.

El método que se usa para crear colores proexistente depende del controlador del dispositivo. La mayoría de los controladores de dispositivos usan un algoritmo de interpolación estándar, que genera un patrón basado en los valores de intensidad de los colores rojo, verde y azul solicitados. En general, cualquier color solicitado que el dispositivo no pueda generar está sujeto a simulación, pero no se notificará a una aplicación cuando el sistema simule un color. Además, una aplicación no puede modificar ni cambiar el algoritmo de interpolación del controlador de dispositivo. Sin embargo, una aplicación puede omitir el algoritmo mediante la creación y el uso de pinceles de patrón. De esta manera, la aplicación crea sus propios colores transformados combinando colores sólidos en el mapa de bits que usa para crear el pincel.

 

 



