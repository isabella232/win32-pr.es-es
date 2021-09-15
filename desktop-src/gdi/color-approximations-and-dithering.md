---
description: Aunque una aplicación puede usar el color sin tener en cuenta las funcionalidades de color del dispositivo, es posible que la salida resultante no sea tan informativa y agradable como la salida para la que se elige cuidadosamente el color.
ms.assetid: 008c8a8e-3456-4727-9b27-00b20ae880a2
title: Aproximaciones y dithering de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a72e28dbc3ce20a42b53b5ff060d950719e2d861
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569224"
---
# <a name="color-approximations-and-dithering"></a>Aproximaciones y dithering de colores

Aunque una aplicación puede usar el color sin tener en cuenta las funcionalidades de color del dispositivo, es posible que la salida resultante no sea tan informativa y agradable como la salida para la que se elige cuidadosamente el color. Pocos dispositivos, si los hay, garantizan una coincidencia exacta para cada valor de color posible. por lo tanto, si una aplicación solicita un color que el dispositivo no puede generar, el sistema se aproxima a ese color mediante un color que el dispositivo puede generar. Por ejemplo, si una aplicación intenta crear un lápiz rojo para una impresora en blanco y negro, recibirá un lápiz negro en su lugar que el sistema usa el negro como aproximación para el rojo.

Una aplicación puede detectar si el sistema se aproximará a un color determinado mediante la [**función GetNearestColor.**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestcolor) La función toma un valor de color y devuelve el valor de color del color correspondiente más cercano que el dispositivo puede generar. El método que usa el sistema para determinar esta aproximación depende del controlador del dispositivo y de sus funcionalidades de color. En la mayoría de los casos, la intensidad general del color aproximado es más cercana a la del color solicitado.

Cuando una aplicación crea un lápiz o establece el color del texto, el sistema siempre se aproxima a un color si no existe ninguna coincidencia exacta. Cuando una aplicación crea un pincel sólido, el sistema puede intentar simular el color solicitado mediante la dithering. *El dithering* simula un color alternando dos o más colores en un patrón. Por ejemplo, se pueden simular diferentes tonalidades de rosa alternando diferentes combinaciones de rojo y blanco. En función de los colores y el patrón, la dithering puede generar simulaciones razonables. Es más útil para dispositivos monocromáticos, ya que expande el número de "colores" disponibles más allá del blanco y el negro simples.

El método usado para crear colores entrelazados depende del controlador del dispositivo. La mayoría de los controladores de dispositivo usan un algoritmo de dithering estándar, que genera un patrón basado en los valores de intensidad de los colores rojo, verde y azul solicitados. En general, cualquier color solicitado que no pueda generar el dispositivo está sujeto a simulación, pero no se notifica a una aplicación cuando el sistema simula un color. Además, una aplicación no puede modificar ni cambiar el algoritmo de dithering del controlador de dispositivo. Sin embargo, una aplicación puede omitir el algoritmo mediante la creación y el uso de pinceles de patrón. De esta manera, la aplicación crea sus propios colores de trama mediante la combinación de colores sólidos en el mapa de bits que usa para crear el pincel.

 

 



