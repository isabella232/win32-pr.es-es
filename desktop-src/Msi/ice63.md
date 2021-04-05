---
description: ICE63 comprueba la secuenciación correcta de la acción RemoveExistingProducts.
ms.assetid: 4dd67bb0-c08a-4a44-b687-0394a3afc2c4
title: ICE63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5faa6f2ddbcb95cdf12966c2887fe9438a5d610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911337"
---
# <a name="ice63"></a>ICE63

ICE63 comprueba la secuenciación correcta de la [acción RemoveExistingProducts](removeexistingproducts-action.md). La acción RemoveExistingProducts se puede colocar:

1.  Entre InstallValidate y InstallInitialize
2.  Inmediatamente después de InstallInitialize o después de InstallInitialize si las acciones entre InstallInitialize y RemoveExistingProducts no generan ninguna acción de script.
3.  Inmediatamente después de InstallExecute o InstallExecuteAgain y antes de InstallFinalize (se aplica la misma restricción que antes).
4.  Después de InstallFinalize.

Si no se corrige una advertencia o un error informados por ICE63, se producirá un error en la actualización.

## <a name="result"></a>Resultado

ICE63 expone una advertencia o un error si la secuenciación de la acción RemoveExistingProducts no es correcta.

## <a name="example"></a>Ejemplo

ICE63 notifica el siguiente error para el ejemplo que se muestra.

``` syntax
WARNING: Some action falls between InstallInitialize and RemoveExistingProducts.
```

La acción "MyCustomAction" se produce entre InstallInitialize y RemoveExistingProducts. Si MyCustomAction genera acciones en el script, esto provoca problemas en la instalación.

Para corregir este error, compruebe que MyCustomAction no genera ninguna acción de script ni resecuenciar las acciones.

[Tabla InstallExecuteSequence](installexecutesequence-table.md)



| Acción                 | Condición | Secuencia |
|------------------------|-----------|----------|
| InstallInitialize      |           | 1000     |
| MyCustomAction         |           | 1010     |
| RemoveExistingProducts |           | 1020     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



