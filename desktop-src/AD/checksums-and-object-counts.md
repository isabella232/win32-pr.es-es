---
title: Sumas de comprobación y recuentos de objetos
description: Las sumas de comprobación y los recuentos de objetos son estrategias de detección que permiten a una aplicación detectar un estado de actualización parcial.
ms.assetid: 14829a74-c186-4250-beac-036c5ecc5913
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc643ec7cd896a7c73df0be5738887a330392140
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486539"
---
# <a name="checksums-and-object-counts"></a>Sumas de comprobación y recuentos de objetos

Las sumas de comprobación y los recuentos de objetos son estrategias de detección que permiten a una aplicación detectar un estado de actualización parcial. Las sumas de comprobación también se pueden usar para detectar incoherencias introducidas por la resolución de colisiones. Tanto las sumas de comprobación como los recuentos de objetos requieren un lugar para almacenar el valor que se usa para comprobar la suma de comprobación o el recuento de objetos. Puede tratarse de un objeto "principal" elegido entre los implicados en la relación específica de la aplicación o en un objeto primario bajo el que se almacenan los objetos relacionados.

En el caso de las sumas de comprobación, las aplicaciones que leen los objetos relacionados comprueban la suma de comprobación calculando un resultado local y comparándola con el valor almacenado. Si los valores no coinciden, la réplica está en un estado de actualización parcial y no se pueden usar los objetos.

Para los recuentos de objetos, las aplicaciones cuentan los objetos relacionados (normalmente los elementos secundarios de un único elemento primario) y comparan el recuento con el valor almacenado. Si los recuentos no coinciden, la réplica está en un estado de actualización parcial y no se pueden usar los objetos.

Algunas consideraciones importantes:

-   Para que el enfoque de suma de comprobación funcione, debe actualizarse uno o más atributos usados en el cálculo de la suma de comprobación. El algoritmo usado para calcular la suma de comprobación debe reflejar de forma confiable las diferencias en la entrada. Si hay muchas entradas diferentes en la misma suma de comprobación, el algoritmo no detectará actualizaciones parciales de forma confiable. "Salting" la entrada con valores como el **objectGUID** del equipo de origen y la fecha y hora de la actualización también es útil.
-   Los recuentos de objetos funcionan mejor cuando se usan con nuevos conjuntos de objetos o en combinación con los GUID de coherencia (consulte la sección siguiente para obtener más información). La aplicación que realiza la actualización debe saber, de antemano, el número de objetos que estarán en el contenedor cuando se complete la actualización o usar otros medios para marcar el contenedor como no válido mientras se realiza la actualización (por ejemplo, establecer el recuento en cero). Después de completar la actualización, la aplicación de origen marca el contenedor con el recuento de objetos incluidos.

 

 




