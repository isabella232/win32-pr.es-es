---
description: El identificador conocido CLASS hace \_ \_ referencia a una pseudo-propiedad en cada objeto WMI que indica la clase del objeto actual.
ms.assetid: a1d0e934-c5b5-4554-9d6e-3881064419ca
ms.tgt_platform: multiple
title: __CLASS identificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa2f40d95d0476bf139aebd3cc6eefe8a34782a48bec311f2a40e1f861ec27c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110749"
---
# <a name="__class-identifier"></a>\_\_Identificador DE CLASE

El identificador conocido CLASS hace \_ \_ referencia a una pseudo-propiedad en cada objeto WMI que indica la clase del objeto actual.

Use \_ \_ CLASS en una cláusula [WHERE](where-clause.md) para filtrar los objetos de las clases derivadas del conjunto de resultados. Por ejemplo, el conjunto de resultados de la consulta siguiente contiene no solo objetos cuya clase es [**Win32 \_ LogicalDisk,**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)sino también objetos cuya clase se deriva de **Win32 \_ LogicalDisk**.


```sql
SELECT * FROM Win32_LogicalDisk
```



En el ejemplo siguiente, el uso de CLASS en la cláusula WHERE filtra todos los objetos de clases derivadas de \_ \_ [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)  porque su clase no **es Win32 \_ LogicalDisk**.


```sql
SELECT * FROM Win32_LogicalDisk   WHERE __CLASS = "Win32_LogicalDisk"
```



Use CLASS en los proveedores a los que se pide que proporcione instancias de una clase específica, independientemente \_ \_ de las subclases.

 

 
