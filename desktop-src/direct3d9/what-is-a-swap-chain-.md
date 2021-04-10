---
description: Una cadena de intercambio es una colección de búferes que se usan para mostrar fotogramas al usuario.
ms.assetid: aefc0680-cbe6-42eb-8c00-eaa343eee469
title: ¿Qué es una cadena de intercambio? (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8fc1fd2d313c70a680d9b276a3aabedc6d8cff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274661"
---
# <a name="what-is-a-swap-chain-direct3d-9"></a>¿Qué es una cadena de intercambio? (Direct3D 9)

Una cadena de intercambio es una colección de búferes que se usan para mostrar fotogramas al usuario. Cada vez que una aplicación presenta un nuevo fotograma para su presentación, el primer búfer de la cadena de intercambio ocupa el lugar del búfer mostrado. Este proceso se denomina intercambio o volteo.

Un adaptador de gráficos contiene un puntero a una superficie que representa la imagen que se muestra en el monitor, denominada búfer frontal. A medida que se actualiza el monitor, la tarjeta de gráficos envía el contenido del búfer frontal al monitor que se va a mostrar. Sin embargo, esto provoca un problema al representar gráficos en tiempo real. La esencia del problema es que la frecuencia de actualización de los monitores es muy lenta en comparación con el resto del equipo. Las frecuencias de actualización comunes van desde 60 Hz (60 veces por segundo) a 100 Hz. Si la aplicación está actualizando el búfer frontal mientras el monitor está en medio de una actualización, la imagen que se muestra se cortará en la mitad con la mitad superior de la pantalla que contiene la imagen anterior y la mitad inferior que contiene la imagen nueva. Este problema se conoce como desgarro.

Direct3D implementa dos opciones para evitar el desgarro:

-   Una opción para permitir solo las actualizaciones del monitor en la operación de reseguimiento vertical (o sincronización vertical). Normalmente, un monitor actualiza su imagen moviendo un PIN de luz horizontalmente, zigzagging desde la parte superior izquierda del monitor y terminando en la parte inferior derecha. Cuando el PIN de la luz alcanza la parte inferior, el monitor vuelve a calibrar el PIN de luz moviéndolo hacia la parte superior izquierda para que el proceso pueda volver a iniciarse. Esta recalibración se denomina sincronización vertical. Durante una sincronización vertical, el monitor no está dibujando nada, por lo que no se verá ninguna actualización en el búfer frontal hasta que el monitor se vuelva a dibujar. La sincronización vertical es relativamente lenta; sin embargo, no es suficiente para representar una escena compleja mientras se espera. Lo que se necesita para evitar el desgarro y poder representar escenas complejas es un proceso llamado almacenamiento en búfer de reserva.
-   Una opción para usar una técnica denominada almacenamiento en búfer de reserva. El almacenamiento en búfer de reserva es el proceso de dibujar una escena en una superficie fuera de la pantalla, denominada búfer de reserva. Tenga en cuenta que cualquier superficie que no sea el búfer frontal se denomina superficie fuera de la pantalla, ya que nunca la ve directamente el monitor. Mediante el uso de un búfer de reserva, una aplicación tiene la libertad de representar una escena cada vez que el sistema está inactivo (es decir, no hay mensajes de Windows en espera) sin tener que tener en cuenta la frecuencia de actualización del monitor. El almacenamiento en búfer de reserva conlleva una complicación adicional de cómo y cuándo se debe trasladar el búfer de reserva al búfer frontal.

El proceso de mover el búfer de reserva al búfer frontal se denomina volteo superficial. Dado que la tarjeta gráfica simplemente usa un puntero a una superficie para representar el búfer frontal, un cambio de puntero simple es todo lo que se necesita para establecer el búfer de reserva en el búfer frontal. Cuando una aplicación pide a Direct3D que presente el búfer de reserva en el búfer frontal, Direct3D simplemente "voltea" los dos punteros de la superficie. El resultado es que el búfer de reserva es ahora el nuevo búfer frontal y el antiguo búfer anterior es el nuevo búfer de reserva. Se invoca un volteo de superficie siempre que una aplicación pide al dispositivo Direct3D que presente el búfer de reserva; sin embargo, se puede configurar Direct3D para poner en cola las solicitudes hasta que se produzca una sincronización vertical. Esta opción se conoce como el intervalo de presentación del dispositivo Direct3D. Tenga en cuenta que es posible que los datos del nuevo búfer de reserva no se puedan volver a usar, en función de cómo una aplicación especifique cómo debe controlar Direct3D el volteo de la superficie. El volteo de Surface es clave en el software multimedia, de animación y de juegos. es equivalente a la manera en que se puede realizar la animación con un panel de papel. En cada página, el artista cambia ligeramente las figuras, de modo que cuando se gira rápidamente entre las hojas, el dibujo aparece animado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Superficies de Direct3D](direct3d-surfaces.md)
</dt> <dt>

[Voltear superficies (Direct3D 9)](flipping-surfaces.md)
</dt> </dl>

 

 



