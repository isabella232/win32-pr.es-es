---
description: Propiedades de ejemplo MPEG
ms.assetid: 339aab84-e5ad-4071-8b67-2b04cb17e450
title: Propiedades de ejemplo MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c20df4b9285a77d00bd98bc6f21558f0d6b3c60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686361"
---
# <a name="mpeg-sample-properties"></a>Propiedades de ejemplo MPEG

Los ejemplos de MPEG tienen las siguientes características.

**Marcas de tiempo**

No todos los ejemplos tienen tiempos de inicio y detención. La hora de detención del ejemplo de los datos de paquete y carga no resulta útil; normalmente se establece en la hora de inicio más una. Los ejemplos de datos de paquetes o carga de MPEG tendrán establecido un tiempo de inicio y detención si el paquete de nivel de sistema del que se generan tiene un valor de PTS válido.

Para obtener más información acerca de las marcas de tiempo, consulte la sección 2.4.1 de ISO1-11172: "el encabezado del paquete puede contener decodificación y/o marcas de tiempo de presentación (DTS y PTS) que hacen referencia a la primera unidad de acceso del paquete".

En el caso de los \_ tipos principales de secuencia MPEG, la hora de inicio es la posición en byte del primer byte, clasificado en 1 byte por segundo. La hora de detención es la posición en bytes del último byte. Por lo tanto, las muestras consecutivas deben tener la hora de detención del primer paquete igual a la hora de inicio del siguiente paquete. En el caso de los datos de CD de vídeo, el origen del medio debe coincidir con el formato de un archivo de CD de vídeo expuesto por CDFS con el fragmento estándar RIFF en el inicio.

En el caso de los tipos de paquete y carga de vídeo MPEG, la marca de tiempo es el tiempo de presentación del primer fotograma de vídeo cuyo código de inicio de imagen comienza en el ejemplo.

En el caso de los tipos de paquete y carga de audio MPEG, la marca de tiempo es el tiempo de presentación del primer fotograma de audio cuyo código de sincronización comienza en el ejemplo.

Se supone que los filtros de control pueden realizar correctamente la reversión de los datos de carga y paquete sin marcas de tiempo.

**Discontinuidades**

Si hay una interrupción en la secuencia (por ejemplo, un hueco en los datos en tiempo real o un error en los datos o después de una búsqueda), se establece la propiedad discontinuidad en el siguiente ejemplo multimedia. Esto también permite una discontinuidad de la marca de tiempo.

**Notificaciones de final de secuencia**

Cuando el descodificador recibe esta notificación, debe procesar todos los datos almacenados en búfer. Los datos nuevos deben comenzar con la propiedad discontinuidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con MPEG-2 en DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



