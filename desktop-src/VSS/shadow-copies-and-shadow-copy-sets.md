---
description: Una instantánea es una instantánea de un volumen que duplica todos los datos que se encuentran en ese volumen en un instante bien definido en el tiempo. VSS identifica cada instantánea mediante un GUID persistente.
ms.assetid: 8ef2478a-c8bc-4517-9a14-e1d9226ec4cd
title: Instantáneas y conjuntos de instantáneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18709842b1fb0fbf6d6cce2557b51042dfb024ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696967"
---
# <a name="shadow-copies-and-shadow-copy-sets"></a>Instantáneas y conjuntos de instantáneas

Una [*instantánea es una instantánea de*](vssgloss-s.md) un volumen que duplica todos los datos que se encuentran en ese volumen en un instante bien definido en el tiempo. VSS identifica cada instantánea mediante un GUID persistente.

Un [*conjunto de instantáneas*](vssgloss-s.md) es una colección de instantáneas de varios volúmenes que se han realizado al mismo tiempo. VSS identifica cada instantánea establecida por un GUID persistente.

El modo en que un determinado proveedor de hardware o software decida implementar instantáneas está completamente a su discreción. Una vez creada una instantánea, hay dos imágenes del volumen de copia de instantáneas disponibles en el sistema: el volumen original, al que se puede tener acceso de forma convencional. y los datos copiados, a los que se puede tener acceso a través de la API de VSS.

Esto permite que se lleven a cabo dos conjuntos de actividades al mismo tiempo:

-   Las aplicaciones normales del sistema pueden continuar o reanudar rápidamente el uso del volumen original, actualizando los datos en el disco.
-   Las aplicaciones que usan la API de solicitante de VSS para tener acceso al volumen de copia sombra pueden realizar copias de seguridad o operaciones similares.

No es necesario implementar instantáneas de la misma manera para todos los archivos, directorios o volúmenes. Diferentes implementaciones del mecanismo de instantáneas ([*proveedores*](vssgloss-p.md)) pueden utilizar diferentes enfoques para crear una instantánea. Sin embargo, para todas las aplicaciones que usan la API de VSS, todas las instantáneas deben aparecer igual.

Para obtener información sobre la implementación predeterminada del proveedor de Windows, vea [proveedor del sistema](providers.md).

## <a name="default-shadow-copy-state"></a>Estado predeterminado de la instantánea

Aunque el sistema de archivos vacíe todos los búferes de e/s antes de crear una instantánea, esto no garantizará que las e/s incompletas se controlen correctamente.

Por lo tanto, suponiendo que el sistema no tiene ninguna aplicación habilitada para VSS, se dice que los datos de una instantánea están en un [*estado coherente con el bloqueo*](vssgloss-c.md). Una instantánea en un estado coherente con el bloqueo contiene una imagen del disco que es la misma que la que existía después de un cierre catastrófico del sistema. Todos los archivos abiertos seguirán existiendo en el volumen, pero no se garantiza que estén libres de operaciones de e/s incompletas o daños en los datos.

Aunque el estado coherente con el bloqueo no soluciona todos los problemas asociados con la definición de un conjunto de copia de seguridad estable (consulte los [problemas comunes de copia](common-volume-backup-issues.md)de seguridad del volumen), tiene varias ventajas sobre el conjunto de copia de seguridad que tendrían que usar las operaciones de copia de seguridad convencionales:

-   Un volumen incluido en una instantánea, incluso en un estado coherente con el bloqueo, todavía contiene todos los archivos. Un conjunto de copia de seguridad creado sin una instantánea no contendría todos los archivos abiertos en el momento de la copia de seguridad. Los archivos mantenidos abiertos en el momento de la operación de copia de seguridad se excluyen de la copia de seguridad.
-   La instantánea del volumen se crea en un instante en el tiempo, no atravesando un sistema de archivos activo, que normalmente requiere mucho más tiempo.

Las aplicaciones de un sistema que no son compatibles con VSS (procesadores de texto, editores, etc.) probablemente tendrán sus archivos en un estado coherente con el bloqueo. Sin embargo, las aplicaciones compatibles con VSS (escritores) pueden coordinar sus acciones para que el estado de sus archivos en la instantánea esté bien definido y sea coherente.

## <a name="shadow-copy-freeze-and-thaw"></a>Inmovilización e reanudación de instantáneas

La creación de todas las operaciones de instantáneas de VSS está [*entre corchetes y se*](vssgloss-f.md) [*reanudan*](vssgloss-t.md) los eventos, que los escritores usan para poner sus archivos en un estado estable antes de la instantánea.

Tener inmovilizar y reanudar eventos como parte del modelo de VSS significa:

-   Controlar el evento Freeze significa que los usuarios que desarrollan escritores deben tener un punto claramente delineado en el ciclo de copia de seguridad en el que se aseguren de que se detienen todas las operaciones de escritura en el disco y que los archivos están en un estado bien definido para la copia de seguridad.
-   Controlar el evento reanudar proporciona el mecanismo para que los escritores reanuden las escrituras en el disco y limpien los archivos temporales u otra información de estado temporal creada en asociación con la instantánea.
-   La ventana predeterminada entre los eventos Freeze y procongele es corta (normalmente 60 segundos); por lo tanto, se puede minimizar la interrupción real de cualquier servicio que proporcione un escritor.
-   El control de otros eventos (como PrepareForSnapshot) anterior y después de los eventos Freeze y reanudación, respectivamente, proporciona la flexibilidad necesaria para permitir que los escritores realicen operaciones complicadas para admitir las instantáneas.

 

 



