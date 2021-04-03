---
description: El operador ISA es un operador específico de WQL que se puede usar en consultas de eventos. Cuando ISA se incluye en la cláusula WHERE de una consulta de evento, solicita una notificación de eventos para todas las clases de una jerarquía de clases, en lugar de una clase de eventos específica.
ms.assetid: 68b7a903-a206-4491-95c4-4a412537f6f5
ms.tgt_platform: multiple
title: Operador ISA para consultas de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0acdd262492bfd876867bdfa7e13fd50e5380270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083071"
---
# <a name="isa-operator-for-event-queries"></a>Operador ISA para consultas de eventos

El operador ISA es un operador específico de WQL que se puede usar en consultas de eventos. Cuando ISA se incluye en la [cláusula WHERE](where-clause.md) de una consulta de evento, solicita una notificación de eventos para todas las clases de una jerarquía de clases, en lugar de una clase de eventos específica.

En el ejemplo siguiente se solicita la notificación cada 10 minutos de eventos de modificación de instancia para todas las instancias que son miembros de cualquier clase derivada de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



Para obtener más información sobre el uso de ISA con una consulta de eventos, vea [crear un evento de temporizador con Win32 \_ localtime o Win32 \_ UTCTime](./creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).

 

 
