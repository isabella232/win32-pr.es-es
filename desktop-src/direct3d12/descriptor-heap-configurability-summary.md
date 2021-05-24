---
title: Resumen de la capacidad de configuración del montón de descriptores
description: En la tabla siguiente se resume información sobre la compatibilidad del montón visible de sombreador y no sombreador.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cfef479e88e5c77df0732113597a4742ecb909c
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335578"
---
# <a name="descriptor-heap-configurability-summary"></a>Resumen de la capacidad de configuración del montón de descriptores

En la tabla siguiente se resume información sobre la compatibilidad del montón visible de sombreador y no sombreador.



|                               | Montón de descriptores visibles del sombreador                                                 | Montón de descriptores visibles que no son de sombreador                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tipos de montón admitidos**          | CBV \_ SRV \_ UAV, Sampler                                                         | Todo                                                                                                                                                                                                                                                                                                                                                                 |
| **Propiedades de página de CPU admitidas** | NO \_ DISPONIBLE, COMBINACIÓN DE \_ ESCRITURA                                                 | \_REESCRIBA                                                                                                                                                                                                                                                                                                                                                         |
| **Administración de residencias por aplicación**   | Sí, aplicación responsable                                                           | No aplicable (no visible para GPU).                                                                                                                                                                                                                                                                                                                                   |
| **Compatibilidad con la edición de descriptores**       | Copiar solo el destino, a través de la actualización de la lista de comandos o la copia de CPU si la CPU está visible. | Solo lectura y escritura de CPU. Sin acceso directo a GPU. Se puede usar para la copia inmediata de CPU (como origen y destino). Se puede usar como origen de actualización en una lista de comandos: copiará los descriptores en el almacenamiento de la lista de comandos durante el registro de la lista de comandos. En la ejecución, la copia almacenada se copiará en el destino, que debe ser un montón visible del sombreador. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Montones de descriptores](descriptor-heaps.md)
</dt> </dl>

 

 




