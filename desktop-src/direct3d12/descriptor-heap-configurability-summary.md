---
title: Resumen de la capacidad de configuración del montón de descriptores
description: En la tabla siguiente se resume información sobre la compatibilidad con el montón visible de sombreador y no sombreador.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c974516a09552fc5e3b301ca3ef91a3aea3d1752d0177f34d5fc94928ee8f293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530557"
---
# <a name="descriptor-heap-configurability-summary"></a>Resumen de la capacidad de configuración del montón de descriptores

En la tabla siguiente se resume información sobre la compatibilidad con el montón visible de sombreador y no sombreador.



|                               | Montón de descriptores visibles del sombreador                                                 | Montón de descriptores visibles que no son de sombreador                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tipos de montón admitidos**          | CBV \_ SRV \_ UAV, Sampler                                                         | All                                                                                                                                                                                                                                                                                                                                                                 |
| **Propiedades de página de CPU admitidas** | NO \_ DISPONIBLE, COMBINACIÓN DE \_ ESCRITURA                                                 | \_REESCRIBA                                                                                                                                                                                                                                                                                                                                                         |
| **Administración de residencias por aplicación**   | Sí, aplicación responsable                                                           | No aplicable (no visible para GPU).                                                                                                                                                                                                                                                                                                                                   |
| **Compatibilidad con la edición de descriptores**       | Copiar solo el destino, mediante la actualización de la lista de comandos o la copia de CPU si la CPU está visible. | Solo lectura y escritura de CPU. Sin acceso directo a GPU. Se puede usar para la copia inmediata de CPU (como origen y destino). Se puede usar como origen de actualización en una lista de comandos: copiará los descriptores en el almacenamiento de la lista de comandos durante el registro de la lista de comandos. En la ejecución, la copia almacenada se copiará en el destino, que debe ser un montón visible del sombreador. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Montones de descriptores](descriptor-heaps.md)
</dt> </dl>

 

 




