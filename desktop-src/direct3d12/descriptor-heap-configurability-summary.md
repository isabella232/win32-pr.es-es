---
title: Resumen de la capacidad de configurar el montón de descriptores
description: En la tabla siguiente se resume la información sobre el sombreador y la compatibilidad con el montón visible de no sombreador.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ce6718e95b774f83d25a84476616643c77c119
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105186"
---
# <a name="descriptor-heap-configurability-summary"></a>Resumen de la capacidad de configurar el montón de descriptores

En la tabla siguiente se resume la información sobre el sombreador y la compatibilidad con el montón visible de no sombreador.



|                               | Montón de descriptor visible del sombreador                                                 | Montón de descriptor visible sin sombreador                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipos de montones admitidos          | CBV \_ SRV \_ UAV, muestra                                                         | All                                                                                                                                                                                                                                                                                                                                                                 |
| Propiedades de la página de CPU admitidas | NO \_ disponible, combinación de escritura \_                                                 | ESCRITURA \_ inversa                                                                                                                                                                                                                                                                                                                                                         |
| Administración de la residencia por aplicación   | Sí, responsable de la aplicación                                                           | No es aplicable (no es visible para GPU).                                                                                                                                                                                                                                                                                                                                   |
| Compatibilidad con la edición de descriptores       | Solo destino de copia, a través de la actualización de la lista de comandos o la copia de la CPU si la CPU es visible. | Solo lectura y escritura de CPU. No hay acceso directo a la GPU. Se puede usar para la copia de CPU inmediata (como origen y destino). Se puede usar como origen de actualización en una lista de comandos: esto copiará los descriptores en el almacenamiento de la lista de comandos durante el registro de la lista de comandos. En la ejecución, la copia almacenada se copiará en el destino, que debe ser un montón visible de sombreador. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Montones de descriptores](descriptor-heaps.md)
</dt> </dl>

 

 




