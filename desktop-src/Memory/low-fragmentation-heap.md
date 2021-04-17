---
description: La fragmentación del montón es un estado en el que la memoria disponible se divide en pequeños bloques no contiguos.
ms.assetid: d10abf82-423c-4942-b05e-55de3a5c4219
title: Montón de baja fragmentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad14a97fa6d95b663f63b21f0982332ba0de01e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687445"
---
# <a name="low-fragmentation-heap"></a>Montón de baja fragmentación

\[La información de este tema se aplica a Windows Server 2003 y Windows XP. A partir de Windows Vista, el sistema usa el montón de baja fragmentación (LFH) según sea necesario para atender las solicitudes de asignación de memoria. Las aplicaciones no necesitan habilitar LFH para sus montones.\]

La fragmentación del montón es un estado en el que la memoria disponible se divide en pequeños bloques no contiguos. Cuando se fragmenta un montón, se puede producir un error en la asignación de memoria incluso cuando la memoria total disponible en el montón es suficiente para satisfacer una solicitud, ya que ningún bloque de memoria único es lo suficientemente grande. El montón de baja fragmentación (LFH) ayuda a reducir la fragmentación del montón.

LFH no es un montón independiente. En su lugar, se trata de una directiva que las aplicaciones pueden habilitar para sus montones. Cuando el LFH está habilitado, el sistema asigna memoria en ciertos tamaños predeterminados. Cuando una aplicación solicita una asignación de memoria de un montón que tiene habilitada la LFH, el sistema asigna el bloque más pequeño de memoria que es lo suficientemente grande como para contener el tamaño solicitado. El sistema no usa LFH para las asignaciones mayores de 16 KB, tanto si el LFH está habilitado como si no.

Una aplicación solo debe habilitar LFH para el montón predeterminado del proceso de llamada o para los [montones privados](heap-functions.md) que ha creado la aplicación. Para habilitar LFH para un montón, use la función [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) para obtener un identificador para el montón predeterminado del proceso de llamada, o bien use el identificador para un montón privado creado por la función [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) . A continuación, llame a la función [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) con el identificador.

LFH no se puede habilitar para montones creados con el **montón \_ no \_ SERIALIZE** o para montones creados con un tamaño fijo. LFH tampoco se puede habilitar si usa las herramientas de depuración del montón en [herramientas de depuración para Windows](/windows-hardware/drivers/debugger/) o [Microsoft comprobador de aplicaciones](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&displaylang=en).

Una vez que se ha habilitado LFH para un montón, no se puede deshabilitar.

Las aplicaciones que se benefician de la mayoría de los LFH son aplicaciones multiproceso que asignan memoria con frecuencia y usan una variedad de tamaños de asignación de 16 KB. Sin embargo, no todas las aplicaciones se benefician de LFH. Para evaluar los efectos de habilitar LFH en la aplicación, use los datos de generación de perfiles de rendimiento.

 

 
