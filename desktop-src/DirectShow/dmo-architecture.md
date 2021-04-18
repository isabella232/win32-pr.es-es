---
description: Arquitectura de DMO
ms.assetid: f74b2d0f-b40c-4598-97a4-9c1dc71bbb1a
title: Arquitectura de DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93fcf7f4ef4528cd4d7949d804b149588075d5ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105651438"
---
# <a name="dmo-architecture"></a>Arquitectura de DMO

En esta sección se describe la arquitectura general de un DMO.

**Secuencias**

Un DMO es un objeto que toma *m* entradas y genera *n* salidas. Las entradas y salidas se denominan *secuencias*. Cada DMO tiene al menos un flujo. Las secuencias no son objetos; simplemente se hace referencia a ellos en la DMO según el número de índice. El número de flujos se fija en tiempo de diseño.

**Tipos de medios**

Todos los datos se escriben utilizando un *tipo de medio*, que define cómo interpretar el contenido de los datos. Por ejemplo, el vídeo RGB de 320 x 240 24 bits es un tipo; 44,1-kilohercios (kHz) audio PCM estéreo de 16 bits es otro tipo. Los tipos de medios se describen mediante la estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) . Para que el cliente pueda procesar los datos, debe establecer el tipo de medio para cada flujo de DMO.

Normalmente, un flujo puede aceptar un intervalo de tipos de medios. Algunos DMOs admiten una gama más amplia de tipos que otros. Las interfaces de DMO definen métodos para que el cliente detecte los tipos admitidos. Por ejemplo, un DMO podría admitir el vídeo RGB en cualquier profundidad de bits, mientras que otro podría admitir solo RGB de 24 bits. Además, una DMO podría estar limitada a determinadas combinaciones de entradas y salidas. Por ejemplo, si el tipo de entrada es un vídeo de 16 bits, el flujo de salida podría requerir la misma profundidad de bits. El cliente puede enumerar los tipos preferidos de cada flujo y probar combinaciones específicas.

**Búferes**

En el modelo DMO predeterminado, el cliente asigna búferes de entrada y búferes de salida independientes. Rellena los búferes de entrada con datos y los entrega a DMO, y el DMO escribe datos nuevos en los búferes de salida.

Opcionalmente, un DMO puede admitir el procesamiento "en contexto". Con el procesamiento en contexto, DMO escribe la salida directamente en el búfer de entrada, en los datos originales. El procesamiento en contexto elimina la necesidad de búferes independientes. Por otro lado, modifica los datos originales, que puede que no sean aceptables para algunas aplicaciones.

El modelo de almacenamiento en búfer predeterminado (no en contexto) se admite a través de la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) . Todos los DMOs deben implementar esta interfaz. Si un DMO admite el procesamiento en contexto, también expone la interfaz [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) . El cliente es responsable de la asignación de todos los búferes, tanto de entrada como de salida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de DMOs](about-dmos.md)
</dt> </dl>

 

 



