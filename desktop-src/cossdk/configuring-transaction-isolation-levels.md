---
description: COM+ ofrece a los desarrolladores un mayor control sobre sus aplicaciones al permitir niveles de aislamiento de transacción configurables.
ms.assetid: a59e262c-41f2-4c80-a04c-50a39af8b009
title: Configuración de los niveles de aislamiento de transacción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d789b9eaed6dfdd2f2419c7eae391d628e75b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496043"
---
# <a name="configuring-transaction-isolation-levels"></a>Configuración de los niveles de aislamiento de transacción

COM+ ofrece a los desarrolladores un mayor control sobre sus aplicaciones al permitir niveles de aislamiento de transacción configurables. Las versiones de COM+ anteriores a COM+ 1,5 usaban siempre el mayor nivel de aislamiento para las transacciones. Aunque este nivel garantiza que siempre se conserva la integridad de los datos, puede provocar problemas de rendimiento, como tiempos de espera, cuando es necesario realizar muchas transacciones en una base de datos grande. Con los niveles de aislamiento configurables, los desarrolladores experimentados pueden aumentar la simultaneidad para mejorar el rendimiento y la escalabilidad.

COM+ proporciona los siguientes niveles de aislamiento de transacción.



| Nivel            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En serie       | Los datos leídos por una transacción actual no pueden ser modificados por otra transacción hasta que finalice la transacción actual. No se pueden insertar nuevos datos que afecten a la transacción actual. Este es el nivel de aislamiento más seguro y es el valor predeterminado.                                                                                                                                                                                                                                                                                                                                                    |
| Lectura repetible  | Los datos leídos por una transacción actual no pueden ser modificados por otra transacción hasta que finalice la transacción actual. Se puede insertar cualquier tipo de datos nuevos durante una transacción.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Lectura confirmada   | Una transacción no puede leer los datos modificados por otra transacción que no se ha confirmado. Este es el nivel de aislamiento predeterminado en Microsoft SQL Server.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Lectura no confirmada | Una transacción puede leer cualquier dato, incluso si lo está modificando otra transacción. Este es el nivel de aislamiento menos seguro, pero permite la simultaneidad más alta.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Any              | Se admite cualquier nivel de aislamiento. Este valor lo suelen usar los componentes de nivel inferior para evitar conflictos. Esta configuración es útil porque cualquier componente de nivel inferior debe configurarse con un nivel de aislamiento igual o menor que el nivel de aislamiento de su componente de nivel superior inmediato. Por lo tanto, un componente de nivel inferior que tenga su nivel de aislamiento configurado como Any siempre usa el mismo nivel de aislamiento que usa su componente de nivel superior inmediato. Si el objeto raíz de una transacción tiene su nivel de aislamiento configurado en cualquiera, se serializa su nivel de aislamiento. |



 

> [!Note]  
> Si un componente de nivel inferior se configura con un nivel de aislamiento mayor que un componente de nivel superior e intenta dar de alta en una transacción, se producirá un error y se anulará la transacción.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer el nivel de aislamiento de la transacción](setting-the-transaction-isolation-level.md)
</dt> </dl>

 

 



