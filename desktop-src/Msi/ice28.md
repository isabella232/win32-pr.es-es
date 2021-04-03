---
description: ICE28 se usa normalmente para validar que la acción ForceReboot se coloca antes o después y nunca dentro de un grupo específico de acciones en las tablas de secuencia de acciones. Consulte el tema de la acción ForceReboot para determinar las acciones que componen este grupo.
ms.assetid: 746d907a-33e1-479a-bcb0-93e7fd5dd975
title: ICE28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65878bdc3db4f9b79ba95b4a170b694a4728ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808749"
---
# <a name="ice28"></a>ICE28

ICE28 se usa normalmente para validar que la acción ForceReboot se coloca antes o después y nunca dentro de un grupo específico de acciones en las tablas de secuencia de acciones. Consulte el tema de la [acción ForceReboot](forcereboot-action.md) para determinar las acciones que componen este grupo.

ICE28 valida las acciones en las siguientes tablas de secuencia:

[Tabla AdminUISequence](adminuisequence-table.md)

[Tabla AdminExecuteSequence](adminexecutesequence-table.md)

[Tabla InstallUISequence](installuisequence-table.md)

[Tabla InstallExecuteSequence](installexecutesequence-table.md)

## <a name="result"></a>Resultado

ICE28 envía un mensaje de error si ForceReboot se secuencia en el grupo de acciones especificado.

## <a name="example"></a>Ejemplo

En el ejemplo mostrado, ICE28 envía el mensaje de error siguiente:

``` syntax
Action: 'ForceReboot' of table InstallExecuteSequence is not permitted in the range 5 to 15 because it cannot separate a set of actions contained in this range.
```

[Tabla InstallExecuteSequence](installexecutesequence-table.md)



| Acción             | Secuencia |
|--------------------|----------|
| ForceReboot        | 10       |
| RegisterMIMEInfo   |   5      |
| RegisterProgIdInfo | 15       |



 

El número de secuencia de 10 que se proporciona a las interrupciones de ForceReboot genera el error, porque se encuentra entre los números de secuencia de RegisterMIMEInfo y RegisterProgIdInfo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



