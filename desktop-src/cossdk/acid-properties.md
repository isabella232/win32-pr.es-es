---
description: Acuñado por los pioneros del procesamiento de transacciones, el acrónimo ACID significa atomic, consistent, isolated y durable.
ms.assetid: 857d145c-710d-4097-8ed6-df11e8d52228
title: Propiedades ACID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2e725cae75b4aa80d25f2959d474e8baa05f70
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073026"
---
# <a name="acid-properties"></a>Propiedades ACID

Acuñado por los pioneros del procesamiento de transacciones, el acrónimo ACID significa atomic, consistent, isolated y durable. Para garantizar un comportamiento predecible, todas las transacciones deben poseer estas propiedades básicas, lo que refuerza el rol de las transacciones críticas como propuestas de todas o ninguna.

La lista siguiente contiene una definición y una descripción de cada propiedad ACID:

<dl> <dt>

<span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atómica
</dt> <dd>

Una transacción debe ejecutarse exactamente una vez y debe ser atómica, ya sea que todo el trabajo se haya realizado o que ninguna de ellas. Las operaciones implicadas en una transacción suelen compartir una intención común y son interdependientes. Al realizar solo un subconjunto de estas operaciones, el sistema podría poner en peligro la intención general de la transacción. Atomicidad elimina la posibilidad de procesar solo un subconjunto de operaciones.

</dd> <dt>

<span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Consistente
</dt> <dd>

Una transacción debe conservar la coherencia de los datos, transformando un estado coherente de los datos en otro estado coherente de los datos. Gran parte de la responsabilidad de mantener la coherencia corresponde al desarrollador de aplicaciones.

</dd> <dt>

<span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>Aislado
</dt> <dd>

Una transacción debe ser una unidad de aislamiento, lo que significa que las transacciones simultáneas deben comportarse como si cada una fuera la única transacción que se ejecuta en el sistema. Dado que un alto grado de aislamiento puede limitar el número de transacciones simultáneas, algunas aplicaciones reducen el nivel de aislamiento a cambio de un mejor rendimiento. Vea [Configuring Transaction Isolation Levels (Configuración de niveles de aislamiento de](configuring-transaction-isolation-levels.md) transacciones) para obtener más información.

</dd> <dt>

<span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Durable
</dt> <dd>

Una transacción debe ser recuperable y, por tanto, debe tener durabilidad. Si se confirma una transacción, el sistema garantiza que sus actualizaciones pueden persistir incluso si el equipo se bloquea inmediatamente después de la confirmación. El registro especializado permite que el procedimiento de reinicio del sistema complete las operaciones sin terminar que requiere la transacción, lo que hace que la transacción sea duradera.

</dd> </dl>

 

 



