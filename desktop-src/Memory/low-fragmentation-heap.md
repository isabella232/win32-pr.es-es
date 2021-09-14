---
description: La fragmentación del montón es un estado en el que la memoria disponible se divide en bloques pequeños y no contráguos.
ms.assetid: d10abf82-423c-4942-b05e-55de3a5c4219
title: Montón de baja fragmentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad14a97fa6d95b663f63b21f0982332ba0de01e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159850"
---
# <a name="low-fragmentation-heap"></a>Montón de baja fragmentación

\[La información de este tema se aplica a Windows Server 2003 y Windows XP. A partir Windows Vista, el sistema usa el montón de baja fragmentación (LFH) según sea necesario para dar servicio a las solicitudes de asignación de memoria. Las aplicaciones no necesitan habilitar lfh para sus montones.\]

La fragmentación del montón es un estado en el que la memoria disponible se divide en bloques pequeños y no contráguos. Cuando un montón está fragmentado, la asignación de memoria puede producir un error incluso cuando la memoria total disponible en el montón es suficiente para satisfacer una solicitud, ya que ningún bloque de memoria es lo suficientemente grande. El montón de baja fragmentación (LFH) ayuda a reducir la fragmentación del montón.

El LFH no es un montón independiente. En su lugar, es una directiva que las aplicaciones pueden habilitar para sus montones. Cuando el LFH está habilitado, el sistema asigna memoria en determinados tamaños predeterminados. Cuando una aplicación solicita una asignación de memoria de un montón que tiene el LFH habilitado, el sistema asigna el bloque de memoria más pequeño que es lo suficientemente grande como para contener el tamaño solicitado. El sistema no usa LFH para asignaciones de más de 16 KB, independientemente de si el LFH está habilitado o no.

Una aplicación debe habilitar lfh solo para el montón predeterminado del proceso de llamada o para los [montones](heap-functions.md) privados que la aplicación ha creado. Para habilitar lfh para un montón, use la función [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) para obtener un identificador para el montón predeterminado del proceso de llamada o use el identificador para un montón privado creado por la [**función HeapCreate.**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) A continuación, [**llame a la función HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) con el identificador .

El LFH no se puede habilitar para los montones creados con **HEAP \_ NO \_ SERIALIZE** o para los montones creados con un tamaño fijo. El LFH tampoco se puede habilitar si usa las herramientas de depuración del montón en Herramientas de depuración [para Windows](/windows-hardware/drivers/debugger/) o [Microsoft Application Verifier](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&displaylang=en).

Una vez que el LFH se ha habilitado para un montón, no se puede deshabilitar.

Las aplicaciones que más se benefician de LFH son las aplicaciones multiproceso que asignan memoria con frecuencia y usan una variedad de tamaños de asignación por debajo de 16 KB. Sin embargo, no todas las aplicaciones se benefician de LFH. Para evaluar los efectos de habilitar lfh en la aplicación, use los datos de generación de perfiles de rendimiento.

 

 
