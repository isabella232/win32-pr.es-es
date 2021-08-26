---
description: Una cadena de intercambio es una colección de búferes que se usan para mostrar fotogramas al usuario.
ms.assetid: aefc0680-cbe6-42eb-8c00-eaa343eee469
title: ¿Qué es una cadena de intercambio? (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91666ffeb05dd7020a4caad1c11777842d7222cdc4cd6b04cd862edea5fff764
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068815"
---
# <a name="what-is-a-swap-chain-direct3d-9"></a>¿Qué es una cadena de intercambio? (Direct3D 9)

Una cadena de intercambio es una colección de búferes que se usan para mostrar fotogramas al usuario. Cada vez que una aplicación presenta un nuevo marco para su presentación, el primer búfer de la cadena de intercambio toma el lugar del búfer mostrado. Este proceso se denomina intercambio o volteo.

Un adaptador de gráficos contiene un puntero a una superficie que representa la imagen que se muestra en el monitor, denominada búfer frontal. A medida que se actualiza el monitor, la tarjeta gráfica envía el contenido del búfer frontal al monitor que se va a mostrar. Sin embargo, esto conduce a un problema al representar gráficos en tiempo real. El núcleo del problema es que las tasas de actualización de supervisión son muy lentas en comparación con el resto del equipo. Las tasas de actualización comunes oscilan entre 60 Hz (60 veces por segundo) y 100 Hz. Si la aplicación está actualizando el búfer frontal mientras el monitor está en medio de una actualización, la imagen que se muestra se cortará a la mitad con la mitad superior de la pantalla que contiene la imagen antigua y la mitad inferior que contiene la nueva imagen. Este problema se conoce como desmontado.

Direct3D implementa dos opciones para evitar el desmonteo:

-   Una opción para permitir solo las actualizaciones del monitor en la operación de seguimiento vertical (o sincronización vertical). Normalmente, un monitor actualiza su imagen moviendo un pin de luz horizontalmente, etiquetando desde la parte superior izquierda del monitor y terminando en la parte inferior derecha. Cuando el pin de luz llega a la parte inferior, el monitor vuelve a abrir el pin de luz al moverlo hacia la parte superior izquierda para que el proceso pueda iniciarse de nuevo. Esta reequilibración se denomina sincronización vertical. Durante una sincronización vertical, el monitor no dibuja nada, por lo que no se verá ninguna actualización del búfer frontal hasta que el monitor empiece a dibujarse de nuevo. La sincronización vertical es relativamente lenta; sin embargo, no es lo suficientemente lento como para representar una escena compleja mientras se espera. Lo que se necesita para evitar el desmonteo y poder representar escenas complejas es un proceso denominado almacenamiento en búfer de reserva.
-   Opción para usar una técnica denominada almacenamiento en búfer de reserva. El almacenamiento en búfer de reserva es el proceso de dibujar una escena en una superficie fuera de la pantalla, denominada búfer de reserva. Tenga en cuenta que cualquier superficie que no sea el búfer frontal se denomina superficie fuera de la pantalla porque el monitor nunca la ve directamente. Al usar un búfer de reserva, una aplicación tiene la libertad de representar una escena cada vez que el sistema está inactivo (es decir, no hay ningún mensaje de Windows en espera) sin tener que tener en cuenta la frecuencia de actualización del monitor. El almacenamiento en búfer de reserva supone una complicación adicional de cómo y cuándo mover el búfer de reserva al búfer front-and-buffer.

El proceso de mover el búfer de reserva al búfer frontal se denomina volteo de superficie. Dado que la tarjeta gráfica simplemente usa un puntero a una superficie para representar el búfer frontal, un cambio de puntero simple es todo lo que se necesita para establecer el búfer de reserva en el búfer frontal. Cuando una aplicación solicita a Direct3D que presente el búfer de reserva en el búfer frontal, Direct3D simplemente "voltea" los dos punteros de superficie. El resultado es que el búfer de reserva es ahora el nuevo búfer front-buffer y el búfer front-buffer antiguo es el nuevo búfer de reserva. Se invoca un volteo de superficie cada vez que una aplicación solicita al dispositivo Direct3D que presente el búfer de reserva; sin embargo, Direct3D se puede configurar para poner en cola las solicitudes hasta que se produzca una sincronización vertical. Esta opción se conoce como intervalo de presentación del dispositivo Direct3D. Tenga en cuenta que es posible que los datos del nuevo búfer de reserva no sean reutilizables, en función de cómo una aplicación especifique cómo direct3D debe controlar el volteo de la superficie. El volteo de superficie es clave en el software multimedia, de animación y de juegos. es equivalente a la forma en que se puede realizar la animación con un panel de papel. En cada página, el intérprete cambia ligeramente las figuras, de modo que cuando se voltea rápidamente entre hojas, el dibujo aparece animado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Superficies de Direct3D](direct3d-surfaces.md)
</dt> <dt>

[Volteo de superficies (Direct3D 9)](flipping-surfaces.md)
</dt> </dl>

 

 



