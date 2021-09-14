---
description: DMO Arquitectura
ms.assetid: f74b2d0f-b40c-4598-97a4-9c1dc71bbb1a
title: DMO Arquitectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93fcf7f4ef4528cd4d7949d804b149588075d5ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169998"
---
# <a name="dmo-architecture"></a>DMO Arquitectura

En esta sección se describe la arquitectura general de un DMO.

**Secuencias**

Un DMO es un objeto que toma *m* entradas y genera *n* salidas. Las entradas y salidas se denominan *flujos*. Cada DMO tiene al menos una secuencia. Secuencias no son objetos; Simplemente se hace referencia a ellos en el DMO por número de índice. El número de secuencias se fija en tiempo de diseño.

**Tipos de medios**

Todos los datos se escriben mediante un *tipo de medio*, que define cómo interpretar el contenido de los datos. Por ejemplo, el vídeo RGB de 320 x 240 de 24 bits es de un tipo; Audio PCM estéreo de 44,1 kilohercios (kHz) de 16 bits es otro tipo. Los tipos de medios se describen [**mediante DMO estructura MEDIA \_ \_ TYPE.**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Para que el cliente pueda procesar datos, debe establecer el tipo de medio para cada secuencia en el DMO.

Normalmente, una secuencia puede aceptar un intervalo de tipos de medios. Algunas DDO admiten una gama más amplia de tipos que otras. Las DMO definen métodos para que el cliente detecte los tipos admitidos. Por ejemplo, una DMO puede admitir vídeo RGB a cualquier profundidad de bits, mientras que otra podría admitir solo RGB de 24 bits. Además, un DMO puede limitarse a determinadas combinaciones de entradas y salidas. Por ejemplo, si el tipo de entrada es vídeo de 16 bits, el flujo de salida podría requerir la misma profundidad de bits. El cliente puede enumerar los tipos preferidos de cada secuencia y, a continuación, probar combinaciones específicas.

**Búferes**

En el modelo DMO predeterminado, el cliente asigna búferes de entrada y búferes de salida independientes. Rellena los búferes de entrada con datos y los entrega al DMO y el DMO escribe datos nuevos en los búferes de salida.

Opcionalmente, un DMO puede admitir el procesamiento "en el lugar". Con el procesamiento local, el DMO escribe la salida directamente en el búfer de entrada, sobre los datos originales. El procesamiento local elimina la necesidad de búferes independientes. Por otro lado, modifica los datos originales, que pueden no ser aceptables para algunas aplicaciones.

El modelo de almacenamiento en búfer predeterminado (no local) se admite a través de la [**interfaz IMediaObject.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) Todas las DDO deben implementar esta interfaz. Si un DMO admite el procesamiento local, también expone la [**interfaz IMediaObjectInPlace.**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) El cliente es responsable de asignar todos los búferes, tanto de entrada como de salida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las DDO](about-dmos.md)
</dt> </dl>

 

 



