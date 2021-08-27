---
description: Propiedades de ejemplo MPEG
ms.assetid: 339aab84-e5ad-4071-8b67-2b04cb17e450
title: Propiedades de ejemplo MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78872b41c579f6af594280b064bfbefc65ef13e8b9d4abf8c21ba9b19613bcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075795"
---
# <a name="mpeg-sample-properties"></a>Propiedades de ejemplo MPEG

Los ejemplos mpeg tienen las siguientes características.

**Marcas de tiempo**

No todos los ejemplos tienen tiempos de inicio y de detenerse. El tiempo de detenerse de ejemplo para los datos de paquete y carga útil no es útil; normalmente se establece en la hora de inicio más una. Los ejemplos de datos de carga o paquete MPEG tendrán una hora de inicio y de detenerse establecida si el paquete de la capa del sistema desde el que se generan tenía un PTS válido.

Para obtener más información sobre las marcas de tiempo, vea la sección 2.4.1 de ISO1-11172: "El encabezado de paquete puede contener marcas de tiempo de descodización o presentación (DTS y PTS) que hacen referencia a la primera unidad de acceso del paquete".

Para los tipos principales de MPEG Stream, la hora de inicio es la posición del byte del primer byte, clasificado \_ en 1 byte por segundo. La hora de detenerse es la posición del byte del último byte. Por lo tanto, los ejemplos consecutivos deben tener la hora de detenerse del primer paquete igual a la hora de inicio del paquete siguiente. Para CD de vídeo (VCD) datos, el origen del medio debe coincidir con el formato de un archivo de vídeo-CD expuesto por CDFS con el fragmento RIFF estándar al principio.

En el caso de los paquetes de vídeo MPEG y los tipos de carga, la marca de tiempo es el tiempo de presentación del primer fotograma de vídeo cuyo código de inicio de imagen comienza en el ejemplo.

En el caso de los paquetes de audio MPEG y los tipos de carga, la marca de tiempo es el tiempo de presentación del primer fotograma de audio cuyo código de sincronización se inicia en el ejemplo.

Se supone que los filtros de control pueden inscribir correctamente los datos de paquetes y cargas útiles sin marcas de tiempo.

**Discontinuidades**

Si hay una interrupción en la secuencia (por ejemplo, una brecha en los datos en tiempo real o un error en los datos o después de una búsqueda), la propiedad discontinuidad se establece en el siguiente ejemplo multimedia. Esto también permite una discontinuidad de marca de tiempo.

**Notificaciones de fin de flujo**

Cuando el descodificador recibe esta notificación, debe procesar los datos almacenados en búfer. Los datos nuevos deben comenzar con la propiedad discontinuidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con MPEG-2 en DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



