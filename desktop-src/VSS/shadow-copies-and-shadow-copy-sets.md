---
description: Una instantánea es una instantánea de un volumen que duplica todos los datos que se mantienen en ese volumen en un instante bien definido en el tiempo. VSS identifica cada instantánea mediante un GUID persistente.
ms.assetid: 8ef2478a-c8bc-4517-9a14-e1d9226ec4cd
title: Instantáneas y conjuntos de instantáneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764478c371cf4a622612865ef7a529955780d82847125874253533d331c195f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998164"
---
# <a name="shadow-copies-and-shadow-copy-sets"></a>Instantáneas y conjuntos de instantáneas

Una [*instantánea es*](vssgloss-s.md) una instantánea de un volumen que duplica todos los datos que se mantienen en ese volumen en un instante bien definido en el tiempo. VSS identifica cada instantánea mediante un GUID persistente.

Un [*conjunto de instantáneas*](vssgloss-s.md) es una colección de instantáneas de varios volúmenes que se toman al mismo tiempo. VSS identifica cada conjunto de instantáneas mediante un GUID persistente.

La forma en que un determinado proveedor de hardware o software decide implementar instantáneas está completamente a su entera discreción. Una vez creada una instantánea, hay dos imágenes del volumen de instantáneas disponibles para el sistema: el volumen original, al que se puede acceder de forma convencional. y los datos copiados, a los que se puede acceder a través de la API de VSS.

Esto permite que dos conjuntos de actividades se lleve a cabo al mismo tiempo:

-   Las aplicaciones normales del sistema pueden continuar o reanudarse rápidamente con el volumen original, actualizando los datos en el disco.
-   Las aplicaciones que usan la API del solicitante de VSS para acceder al volumen de instantáneas pueden realizar copias de seguridad u operaciones similares.

Las instantáneas no deben implementarse de la misma manera para todos los archivos, directorios o volúmenes. Las distintas implementaciones del mecanismo de [*instantáneas (proveedores*](vssgloss-p.md)) pueden usar enfoques diferentes para crear una instantánea. Sin embargo, para todas las aplicaciones que usan la API de VSS, todas las instantáneas deben aparecer igual.

Para obtener información sobre la implementación predeterminada Windows proveedor de sistemas, vea [Proveedor de sistema](providers.md).

## <a name="default-shadow-copy-state"></a>Estado predeterminado de la instantánea

Aunque el sistema de archivos vacía todos los búferes de E/S antes de crear una instantánea, esto no garantizará que la E/S incompleta se controle correctamente.

Por lo tanto, suponiendo que el sistema no tenga aplicaciones habilitadas para VSS, se dice que los datos de una instantánea están en un estado coherente con los [*bloqueos.*](vssgloss-c.md) Una instantánea en un estado coherente con los bloqueos contiene una imagen del disco que es la misma que la que existiría después de un apagado catastrófico del sistema. Todos los archivos que estaban abiertos seguirán existiendo en el volumen, pero no se garantiza que estén libres de operaciones de E/S incompletas o daños en los datos.

Aunque el estado coherente con los bloqueos no trata completamente todos los problemas asociados a la definición de un conjunto de copia de seguridad estable (consulte Problemas comunes de copia de seguridad de [volumen),](common-volume-backup-issues.md)tiene varias ventajas con respecto al conjunto de copia de seguridad que tendrían que usar las operaciones de copia de seguridad convencionales:

-   Un volumen contenido en una instantánea, incluso en un estado coherente con los bloqueos, todavía contiene todos los archivos. Un conjunto de copia de seguridad creado sin una instantánea no contendrá todos los archivos abiertos en el momento de la copia de seguridad. Los archivos que se mantienen abiertos en el momento de la operación de copia de seguridad se excluyen de la copia de seguridad.
-   La instantánea del volumen se crea en un momento en el tiempo y no recorriendo un sistema de archivos activo, que normalmente requiere mucho más tiempo.

Las aplicaciones de un sistema que no son compatibles con VSS (procesadores de palabras, editores, entre otros) probablemente tendrán sus archivos en un estado coherente con los bloqueos. Sin embargo, las aplicaciones compatibles con VSS (escritores) pueden coordinar sus acciones para que el estado de sus archivos en la instantánea sea bien definido y coherente.

## <a name="shadow-copy-freeze-and-thaw"></a>Inmovilización y descongelización de instantáneas

La creación de cada operación de instantánea de VSS está entre corchetes por los eventos [*Freeze*](vssgloss-f.md) y [*Thaw,*](vssgloss-t.md) que los escritores usan para colocar sus archivos en un estado estable antes de la instantánea.

Tener eventos Freeze y Thaw como parte del modelo de VSS significa:

-   Controlar el evento Freeze significa que los que desarrollan escritores deben tener un punto claramente delineado en el ciclo de copia de seguridad donde se aseguren de que todas las operaciones de escritura en el disco se detienen y que los archivos están en un estado bien definido para la copia de seguridad.
-   El control del evento Thaw proporciona el mecanismo para que los escritores reanuden las escrituras en el disco y limpien los archivos temporales u otra información de estado temporal que se crearon en asociación con la instantánea.
-   La ventana predeterminada entre los eventos Freeze y Thaw es corta (normalmente 60 segundos); Por lo tanto, se puede minimizar la interrupción real de cualquier servicio que proporciona un escritor.
-   El control de otros eventos (como PrepareForSnapshot) anteriores y adicionales a los eventos Freeze y Thaw, respectivamente, proporciona la flexibilidad necesaria para permitir que los escritores completen operaciones complicadas para admitir instantáneas.

 

 



