---
description: ICE28 se usa normalmente para validar que la acción ForceReboot se coloca antes o después, y nunca dentro, de un grupo específico de acciones en las tablas de secuencia de acciones. Consulte el tema acción ForceReboot para determinar las acciones que componen este grupo.
ms.assetid: 746d907a-33e1-479a-bcb0-93e7fd5dd975
title: ICE28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cda8676a072ebed21a16653dca9af67464f35699530eb3c08ae05d3cd9574b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528785"
---
# <a name="ice28"></a>ICE28

ICE28 se usa normalmente para validar que la acción ForceReboot se coloca antes o después, y nunca dentro, de un grupo específico de acciones en las tablas de secuencia de acciones. Consulte el [tema acción ForceReboot](forcereboot-action.md) para determinar las acciones que componen este grupo.

ICE28 valida las acciones en las siguientes tablas de secuencia:

[Tabla AdminUISequence](adminuisequence-table.md)

[Tabla AdminExecuteSequence](adminexecutesequence-table.md)

[Tabla InstallUISequence](installuisequence-table.md)

[Tabla InstallExecuteSequence](installexecutesequence-table.md)

## <a name="result"></a>Resultado

ICE28 envía un mensaje de error si ForceReboot se secuencia dentro del grupo de acciones especificado.

## <a name="example"></a>Ejemplo

En el ejemplo que se muestra, ICE28 publica el siguiente mensaje de error:

``` syntax
Action: 'ForceReboot' of table InstallExecuteSequence is not permitted in the range 5 to 15 because it cannot separate a set of actions contained in this range.
```

[InstallExecuteSequence Table](installexecutesequence-table.md)



| Acción             | Secuencia |
|--------------------|----------|
| Forcereboot        | 10       |
| RegisterMIMEInfo   |   5      |
| RegisterProgIdInfo | 15       |



 

El número de secuencia de 10 dado a los saltos ForceReboot genera el error, ya que se encuentra entre los números de secuencia de RegisterMIMEInfo y RegisterProgIdInfo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



