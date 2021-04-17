---
description: ICE65 comprueba que la tabla de entorno no tiene valores de prefijo o de anexión no válidos.
ms.assetid: 95d4e618-9a19-40db-910a-daab105559ae
title: ICE65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3d2b7bcd844c970ccc7fddf376b27c2ec54f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652997"
---
# <a name="ice65"></a>ICE65

ICE65 comprueba que la [tabla de entorno](environment-table.md) no tiene valores de prefijo o de anexión no válidos.

Si no se corrige una advertencia o un error informados por ICE65, generalmente se producen problemas en la instalación, desinstalación o reparación de la variable de entorno. Por ejemplo, solo se pueden quitar algunos valores de una variable determinada si uno o varios de los valores de esa variable tienen un separador final.

## <a name="result"></a>Resultado

ICE65 envía una advertencia o un error si la tabla de entorno tiene valores de prefijo o de anexión no válidos.

## <a name="example"></a>Ejemplo

ICE65 notifica el siguiente error y advertencia para el ejemplo que se muestra.

``` syntax
The environment variable 'Var3' has a separator beginning or ending its value.
```

El valor null final al final del valor ( \[ ~ \] ) marca este valor para que se antepone a cualquier valor existente. El carácter que precede a null (un punto y coma) se convierte en el separador de este valor. Este valor tiene un punto y coma al principio de la cadena.

Para corregir este error, simplemente elimine el punto y coma inicial.

``` syntax
WARNING: The environment variable 'Var2' has an alphanumeric separator
```

El valor null inicial en el valor ( \[ ~ \] ) marca este valor para anexarlo a cualquier valor existente. El carácter situado inmediatamente después de la NULL se convierte en el separador de este valor. En este caso, ese carácter es la letra "e", que también se produce en medio de la cadena que se va a anexar. Esta condición (con un separador que sea igual que un carácter dentro de la cadena que se va a anexar) puede producir resultados imprevisibles.

La letra "e", que es una letra común, es probable que se encuentre en el valor. Una opción mejor sería ";" u otros caracteres no alfanuméricos. (Sin embargo, si el valor es una ruta de acceso, ":" y " \\ " y "." son opciones de riesgo).

Para corregir esta advertencia, use un carácter separador diferente.

[Tabla de entorno](environment-table.md)



| Componente | Directorio | Atributos         | Rutas       |
|-----------|-----------|--------------------|---------------|
| Var1      | TestVar   | \[~\]; AppendThis   | TestComponent |
| Var2      | TestVar   | \[~\]eAppendThis   | TestComponent |
| Var3      | TestVar   | ; PrependThis;\[~\] | TestComponent |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



