---
title: Origen de la imagen inserda
description: Origen de la imagen inserda
ms.assetid: 6cc290d8-2c15-4789-970d-9a3663a64d08
keywords:
- Reproductor de Windows Media Máscaras móviles, origen de imagen de botón
- máscaras, origen de imagen de botón
- referencia de máscaras, botones
- botones en máscaras, origen de imagen
- origen de imagen para máscaras, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021c77a305e0f6981823c8a1e471862554c32e08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070956"
---
# <a name="pushed-image-source"></a>Origen de la imagen inserda

Debe definir el origen de la imagen que desea mostrar cuando el usuario presione un botón. La imagen procede del archivo que definió como Inserción en la sección Mapas de bits. Debe escribir el tipo de imagen seguido de un espacio, el símbolo @ y otro espacio. A continuación, debe escribir dos enteros positivos que definan las coordenadas superior e izquierda (en píxeles) de la imagen que desea usar dentro del archivo de imagen inserda. La ubicación en la que se mostrará la imagen procede de las coordenadas definidas para el botón en relación con la imagen de fondo. pero la ubicación de la que procede se define mediante los dos números siguientes a "Pushed @" y es relativa a la imagen pushed desde la que se lee la imagen.

Por ejemplo, para usar una imagen de la imagen pushed que se encuentra en el archivo pushed cuya ubicación superior izquierda es 50,60, usaría el código siguiente:


```C++
Pushed @ 50,60

```



Si no desea mostrar una imagen diferente, puede definir el mapa de bits Background (Fondo) como el mapa de bits Pushed (Inserción). Para ello, especifique el archivo en segundo plano como archivo de inserción y especifique el desplazamiento a la esquina superior izquierda del botón:


```C++
Pushed @ 50,60

```



Si lo hace, ninguno de los botones puede mostrar una imagen inserda. Se recomienda mostrar una imagen pushed para todos los botones para proporcionar al usuario una indicación visual, ya que no siempre está claro si una pulsación genera un resultado, especialmente cuando se reproduce la música o se apaga el sonido de pulsación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Botones**](buttons.md)
</dt> </dl>

 

 




