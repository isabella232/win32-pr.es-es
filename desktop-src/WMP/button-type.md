---
title: Tipo de botón
description: Tipo de botón
ms.assetid: 0c9e72d5-5cc4-4d6f-b184-2c8c8487e366
keywords:
- Aspectos de Windows Media Player Mobile, tipos de botón
- máscaras, tipos de botón
- referencia de las máscaras, botones
- botones en máscaras, tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58eeb7402a13730fd7f4030d2e4326fe7f18e63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903243"
---
# <a name="button-type"></a>Tipo de botón

Los botones tienen dos tipos generales: ubicación y región. Cada tipo general tiene tres tipos específicos, lo que convierte seis tipos de botón en todos.

> [!Note]  
> Los tipos de botones están en desuso en las máscaras de Windows Media Player 10 Mobile o posterior.

 

Tipos de botón de ubicación

Los botones de ubicación usan coordenadas para definir sus ubicaciones en relación con el fondo. En la tabla siguiente se muestran los valores que son válidos para los tipos de botón de ubicación. No es necesario definir valores para los tipos que no se vayan a usar en la máscara.



| Value  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inserción   | Define un botón que desencadena un evento una vez. El botón se debe insertar cada vez para desencadenar eventos adicionales. Un ejemplo sería un botón que se desplaza al siguiente elemento de la lista de reproducción. La ubicación del botón se define mediante sus coordenadas.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Alternancia | Define un botón que desencadena un evento que cambia un estado. El estado permanecerá hasta que se vuelva a insertar el botón. Un ejemplo es un botón que reordena la lista de reproducción. Una vez que la lista de reproducción esté en un estado aleatorio, permanecerá en orden aleatorio hasta que el botón se vuelva a insertar. La ubicación del botón se define mediante sus coordenadas.                                                                                                                                                                                                                                                                                                                                                           |
| 2Push  | Define un botón que desencadena un evento y, a continuación, cambia a un estado que está listo para desencadenar un evento diferente. Los dos Estados se alternan cada vez que se inserta el botón. Un ejemplo es un botón que utiliza la función **playpause** para alternar entre reproducir y pausar el elemento multimedia actual. Cuando el botón se inserta por primera vez, se desencadena el estado de reproducción principal y se muestra una imagen secundaria para indicar que se puede desencadenar un evento de **pausa** . Cuando el botón se vuelve a insertar, se desencadena el estado de pausa y se muestra la imagen original para indicar que se puede desencadenar un evento de **reproducción** . La ubicación del botón se define mediante sus coordenadas. |



 

Tipos de botón de región

Los botones de región usan áreas de color de la imagen de región para definir dónde se procesarán los grifos para un botón concreto. En la tabla siguiente se muestran los valores que son válidos para los tipos de botón de región. No es necesario definir valores para los tipos que no se vayan a usar en la máscara.



| Value     | Descripción                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| PushHit   | Similar al valor del botón de la tecla de acceso, salvo que el área de aciertos del botón se define mediante el valor de color de la imagen de la región.   |
| ToggleHit | Similar al valor del botón de alternancia, salvo que el área de aciertos del botón se define mediante el valor de color de la imagen de la región. |
| 2PushHit  | Similar al valor del botón 2Push, excepto que el área de aciertos del botón se define mediante el valor de color de la imagen de la región.  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Botones**](buttons.md)
</dt> </dl>

 

 




