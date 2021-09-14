---
description: ICE65 comprueba que la tabla Environment no tiene valores de prefijo o anexados no válidos.
ms.assetid: 95d4e618-9a19-40db-910a-daab105559ae
title: ICE65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3d2b7bcd844c970ccc7fddf376b27c2ec54f56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074561"
---
# <a name="ice65"></a>ICE65

ICE65 comprueba que la [tabla Environment](environment-table.md) no tiene valores de prefijo o anexados no válidos.

Si no se corrige una advertencia o un error notificados por ICE65, por lo general se producirán problemas en la instalación, desinstalación o reparación de la variable de entorno. Por ejemplo, solo se pueden quitar algunos valores de una variable determinada si uno o varios de los valores de esa variable tienen un separador final.

## <a name="result"></a>Resultado

ICE65 envía una advertencia o un error si la tabla de entorno tiene valores de prefijo o anexados no válidos.

## <a name="example"></a>Ejemplo

ICE65 notifica el siguiente error y advertencia para el ejemplo mostrado.

``` syntax
The environment variable 'Var3' has a separator beginning or ending its value.
```

El valor NULL final al final del valor ( ) marca este valor para anteponerlo \[ ~ \] a cualquier valor existente. El carácter inmediatamente anterior al valor NULL (punto y coma) se convierte en el separador de este valor. Este valor también tiene un punto y coma al principio de la cadena.

Para corregir este error, basta con eliminar el punto y coma inicial.

``` syntax
WARNING: The environment variable 'Var2' has an alphanumeric separator
```

El valor NULL inicial del valor ( \[ ~ \] ) marca este valor para anexarse a cualquier valor existente. El carácter inmediatamente después del valor NULL se convierte en el separador de este valor. En este caso, ese carácter es la letra "e", que también se produce en el medio de la cadena que se va a anexar. Esta condición (tener un separador que sea el mismo que un carácter dentro de la cadena que se va a anexar) puede provocar resultados impredecibles.

Es probable que la letra "e", que es una letra común, se encuentra en el valor . Una mejor opción sería ";" o algún otro carácter no alfanumérico. (Sin embargo, si el valor es una ruta de acceso, ":" y \\ " " y "." son opciones de riesgo).

Para corregir esta advertencia, use un carácter separador diferente.

[Tabla de entorno](environment-table.md)



| Componente | Directorio | Atributos         | KeyPath       |
|-----------|-----------|--------------------|---------------|
| Var1      | TestVar   | \[~\]; AppendThis   | TestComponent |
| Var2      | TestVar   | \[~\]eAppendThis   | TestComponent |
| Var3      | TestVar   | ; PrependThis;\[~\] | TestComponent |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



