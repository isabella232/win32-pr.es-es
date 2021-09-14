---
title: Tipo de botón
description: Tipo de botón
ms.assetid: 0c9e72d5-5cc4-4d6f-b184-2c8c8487e366
keywords:
- Reproductor de Windows Media Máscaras móviles, tipos de botón
- máscaras, tipos de botón
- referencia de máscaras, botones
- botones en máscaras, tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58eeb7402a13730fd7f4030d2e4326fe7f18e63
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889380"
---
# <a name="button-type"></a>Tipo de botón

Los botones se incluyen en dos tipos generales: ubicación y región. Cada tipo general tiene tres tipos específicos, lo que hace seis tipos de botón en total.

> [!Note]  
> Los tipos de botones están en desuso en las máscaras Reproductor de Windows Media 10 Mobile o posterior.

 

Tipos de botón de ubicación

Los botones de ubicación usan coordenadas para definir sus ubicaciones en relación con el fondo. En la tabla siguiente se muestran los valores que son válidos para los tipos de botón de ubicación. No es necesario definir valores para los tipos que no va a usar en la máscara.



| Value  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inserción   | Define un botón que desencadena un evento una vez. El botón debe insertarse cada vez para desencadenar más eventos. Un ejemplo sería un botón que se mueve al siguiente elemento de la lista de reproducción. La ubicación del botón se define mediante sus coordenadas.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Alternancia | Define un botón que desencadena un evento que cambia un estado. El estado permanece hasta que se vuelve a insertar el botón. Un ejemplo es un botón que ordena aleatoriamente la lista de reproducción. Una vez que la lista de reproducción está en un estado aleatorio, permanecerá aleatoria hasta que se vuelva a insertar el botón. La ubicación del botón se define mediante sus coordenadas.                                                                                                                                                                                                                                                                                                                                                           |
| 2Push  | Define un botón que desencadena un evento y, a continuación, cambia a un estado que está listo para desencadenar un evento diferente. Los dos estados se alternan cada vez que se inserta el botón. Un ejemplo es un botón que usa la **función PlayPause** para alternar entre reproducir y pausar el elemento multimedia actual. Cuando se inserta el botón por primera vez, se desencadena el estado de reproducción principal y se muestra una imagen secundaria para indicar que se puede desencadenar un evento **de** pausa. Cuando se vuelve a insertar el botón, se desencadena el estado Pausar y se muestra la imagen original para indicar que se puede desencadenar un evento **De** reproducción. La ubicación del botón se define mediante sus coordenadas. |



 

Tipos de botones de región

Los botones de región usan áreas de color en la imagen región para definir dónde se procesarán las pulsaciones para un botón determinado. En la tabla siguiente se muestran los valores que son válidos para los tipos de botón de región. No es necesario definir valores para los tipos que no va a usar en la máscara.



| Value     | Descripción                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| PushHit   | Similar al valor del botón Insertar, salvo que el área de pulsación del botón se define mediante el valor de color de la imagen Región.   |
| ToggleHit | Similar al valor del botón Alternar, salvo que el área de pulsación del botón está definida por el valor de color de la imagen Región. |
| 2PushHit  | Similar al valor del botón 2Push, salvo que el área de pulsación del botón se define mediante el valor de color de la imagen Región.  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Botones**](buttons.md)
</dt> </dl>

 

 




