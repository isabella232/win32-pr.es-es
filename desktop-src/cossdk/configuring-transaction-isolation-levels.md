---
description: COM+ proporciona a los desarrolladores más control sobre sus aplicaciones al permitir niveles de aislamiento de transacciones configurables.
ms.assetid: a59e262c-41f2-4c80-a04c-50a39af8b009
title: Configuración de los niveles de aislamiento de transacciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e91583df010669b9dfce092e5bb38490652b4bc407a4ec7b73c83da2078cf14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638115"
---
# <a name="configuring-transaction-isolation-levels"></a>Configuración de los niveles de aislamiento de transacciones

COM+ proporciona a los desarrolladores más control sobre sus aplicaciones al permitir niveles de aislamiento de transacciones configurables. Las versiones de COM+ anteriores a COM+ 1.5 siempre usaban el mayor nivel de aislamiento para las transacciones. Aunque este nivel garantiza que la integridad de los datos siempre se conserva, puede dar lugar a problemas de rendimiento, como tiempos de espera, cuando es necesario realizar muchas transacciones en una base de datos grande. Con los niveles de aislamiento configurables, los desarrolladores experimentados pueden aumentar la simultaneidad para mejorar el rendimiento y la escalabilidad.

COM+ proporciona los siguientes niveles de aislamiento de transacción.



| Nivel            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En serie       | Otra transacción no puede cambiar los datos leídos por una transacción actual hasta que finalice la transacción actual. No se puede insertar ningún dato nuevo que afecte a la transacción actual. Este es el nivel de aislamiento más seguro y es el predeterminado.                                                                                                                                                                                                                                                                                                                                                    |
| Lectura repetible  | Otra transacción no puede cambiar los datos leídos por una transacción actual hasta que finalice la transacción actual. Cualquier tipo de datos nuevos se puede insertar durante una transacción.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Lectura confirmada   | Una transacción no puede leer los datos que está modificando otra transacción que no se ha confirmado. Este es el nivel de aislamiento predeterminado en Microsoft SQL Server.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Lectura no confirmada | Una transacción puede leer cualquier dato, incluso si otra transacción lo está modificando. Este es el nivel de aislamiento menos seguro, pero permite la mayor simultaneidad.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Any              | Se admite cualquier nivel de aislamiento. Esta configuración la usan normalmente los componentes de nivel inferior para evitar conflictos. Esta configuración es útil porque cualquier componente de nivel inferior debe configurarse con un nivel de aislamiento igual o menor que el nivel de aislamiento de su componente ascendente inmediato. Por lo tanto, un componente de nivel inferior que tenga su nivel de aislamiento configurado como Cualquiera siempre usa el mismo nivel de aislamiento que su componente ascendente inmediato. Si el objeto raíz de una transacción tiene su nivel de aislamiento configurado en Cualquiera, su nivel de aislamiento se serializa. |



 

> [!Note]  
> Si un componente de nivel inferior se configura con un nivel de aislamiento mayor que un componente ascendente e intenta dar de alta en una transacción, se produce un error y se anula la transacción.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer el nivel de aislamiento de la transacción](setting-the-transaction-isolation-level.md)
</dt> </dl>

 

 



