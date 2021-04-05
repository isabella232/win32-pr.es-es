---
description: En esta sección se describe la sintaxis de las instrucciones condicionales usadas por la función MsiEvaluateCondition y las tablas de secuencia de acciones. Para obtener más información, vea ejemplos de sintaxis de instrucciones condicionales.
ms.assetid: 6f1657f9-063b-4d57-ad76-95e3dbe25786
title: Sintaxis de la instrucción condicional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0548a71756faff654bfe2b49e14c0581a6248a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909026"
---
# <a name="conditional-statement-syntax"></a>Sintaxis de la instrucción condicional

En esta sección se describe la sintaxis de las instrucciones condicionales usadas por la función [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) y las [tablas de secuencia](using-a-sequence-table.md)de acciones. Para obtener más información, vea [ejemplos de sintaxis de instrucciones condicionales](examples-of-conditional-statement-syntax.md).

## <a name="summary-of-conditional-statement-syntax"></a>Resumen de la sintaxis de la instrucción condicional

En esta tabla y en la lista siguiente se resume la sintaxis que se va a usar en las expresiones condicionales.



| Elemento                | Sintaxis                                                                                                          |
|---------------------|-----------------------------------------------------------------------------------------------------------------|
| value               | \|entero de literal de símbolo \|                                                                                    |
| Comparison-Operator | < \| > \| <= \| >= \| = \| <>                                                                 |
| término                | \|comparación de valores de valor: valor del operador \| (expresión)\|                                                    |
| Factor booleano      | término \| **no** term                                                                                            |
| Término booleano        | Factor booleano \| **y** término de factor booleano                                                                   |
| expresión          | \|Expresión **o** término booleano de término booleano                                                                  |
| símbolo              | propiedad \| % Environment: variable \| $Component-Action \| ? componente-State \| &característica-acción \| ! Estado de la característica |



 

-   Los nombres y valores de símbolos distinguen mayúsculas de minúsculas.
-   Los nombres de las variables de entorno no distinguen mayúsculas de minúsculas.
-   El texto literal debe ir entre comillas ("texto").
    > [!Note]  
    > El texto literal que contiene comillas no se puede usar en instrucciones condicionales porque no hay ningún carácter de escape para las comillas dentro del texto literal. Para realizar una comparación con el texto literal que contiene comillas, el texto literal debe colocarse en una propiedad. Por ejemplo, para comprobar que la propiedad SERVERNAME no contiene comillas, defina una propiedad denominada QUOTEs en la [tabla de propiedades](property-table.md) con un valor de "y cambie la condición a not ServerName><Quotes.

     

-   Los valores de propiedad inexistentes se tratan como cadenas vacías.
-   No se admiten valores numéricos de punto flotante.
-   Los operadores y la prioridad son los mismos que en los lenguajes básico y SQL.
-   No se admiten los operadores aritméticos.
-   Los paréntesis se pueden usar para invalidar la precedencia de los operadores.
-   Los operadores no distinguen mayúsculas de minúsculas.
-   En las comparaciones de cadenas, una tilde "~" con el prefijo para el operador realiza una comparación que no distingue entre mayúsculas y minúsculas.
-   La comparación de un entero con un valor de cadena o propiedad que no se puede convertir en un entero es siempre **msiEvaluateConditionFalse**, excepto para el operador de comparación "<>", que devuelve **msiEvaluateConditionTrue**.

## <a name="access-prefixes"></a>Prefijos de acceso

En la tabla siguiente se muestran los prefijos que se van a usar para tener acceso a diversa información del sistema y del instalador para su uso en expresiones condicionales.



| Tipo de símbolo          | Prefijo | Value                                                     |
|----------------------|--------|-----------------------------------------------------------|
| Propiedad Installer   | (ninguno) | Valor de la tabla de propiedades ([propiedad](property-table.md)). |
| Variable de entorno | %      | Valor de la variable de entorno.                            |
| Clave de la tabla de componentes  | $      | Estado de acción del componente.                            |
| Clave de la tabla de componentes  | ?      | Estado instalado del componente.                         |
| Clave de la tabla de características    | &      | Estado de acción de la característica.                              |
| Clave de la tabla de características    | !      | Estado instalado de la característica.                           |



 

## <a name="logical-operators"></a>Operadores lógicos

En la tabla siguiente se muestran los operadores lógicos en expresiones condicionales, en orden de prioridad alta a baja.



| Operator | Significado                                                 |
|----------|---------------------------------------------------------|
| Not      | Prefix (operador unario); invierte el estado del término siguiente. |
| And      | TRUE si ambos términos son TRUE.                            |
| O bien       | TRUE si uno o ambos términos son TRUE.                  |
| Xor      | TRUE si, pero no ambos términos, son verdaderos.             |
| Eqv      | TRUE si ambos términos son TRUE o ambos términos son FALSE.    |
| Imp      | TRUE si el término izquierdo es falso o el término derecho es TRUE.       |



 

## <a name="comparative-operators"></a>Operadores de comparación

En la tabla siguiente se muestran los operadores de comparación que se usan en las expresiones condicionales. Estos operadores de comparación solo se pueden producir entre dos valores.



| Operator | Significado                                                     |
|----------|-------------------------------------------------------------|
| =        | TRUE si el valor de la izquierda es igual al valor derecho.                 |
| <> | TRUE si el valor de la izquierda no es igual al valor derecho.             |
| >     | TRUE si el valor izquierdo es mayor que el valor derecho.             |
| >=    | TRUE si el valor izquierdo es mayor o igual que el valor derecho. |
| <     | TRUE si el valor de la izquierda es menor que el valor derecho.                |
| <=    | TRUE si el valor de la izquierda es menor o igual que el valor derecho.    |



 

## <a name="substring-operators"></a>Operadores de subcadena

En la tabla siguiente se muestran los operadores de subcadena utilizados en las expresiones condicionales. Se pueden producir operadores de subcadena entre dos valores de cadena.



| Operator | Significado                                           |
|----------|---------------------------------------------------|
| >< | TRUE si la cadena izquierda contiene la cadena derecha.    |
| << | TRUE si la cadena izquierda comienza con la cadena derecha. |
| >> | TRUE si la cadena izquierda termina con la cadena derecha.   |



 

## <a name="bitwise-numeric-operators"></a>Operadores numéricos bit a bit

En la tabla siguiente se muestran los operadores numéricos bit a bit en expresiones condicionales. Estos operadores pueden producirse entre dos valores enteros.



| Operator | Significado                                                                      |
|----------|------------------------------------------------------------------------------|
| >< | And bit a bit, TRUE si los enteros izquierdo y derecho tienen algún bit en común.    |
| << | True si los 16 bits superiores del entero izquierdo son iguales que el entero derecho. |
| >> | True si los 16 bits inferiores del entero izquierdo son iguales que el entero derecho.  |



 

## <a name="feature-and-component-state-values"></a>Valores de estado de componentes y características

En la tabla siguiente se muestra dónde es válido usar los símbolos de operador de componentes y características.



| Operator <state> | Donde esta sintaxis es válida                                                                                                                                         |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| $component-acción      | En la tabla de [condiciones](condition-table.md) , y en las tablas de [secuencias](using-a-sequence-table.md) , después de la acción [CostFinalize](costfinalize-action.md) . |
| &característica-acción        | En la tabla de [condiciones](condition-table.md) , y en las tablas de [secuencias](using-a-sequence-table.md) , después de la acción [CostFinalize](costfinalize-action.md) . |
| ! Estado de la característica         | En la tabla de [condiciones](condition-table.md) , y en las tablas de [secuencias](using-a-sequence-table.md) , después de la acción [CostFinalize](costfinalize-action.md) . |
| ? componente-estado       | En la tabla de [condiciones](condition-table.md) , y en las tablas de [secuencias](using-a-sequence-table.md) , después de la acción [CostFinalize](costfinalize-action.md) . |



 

En la tabla siguiente se muestran los valores de estado de componentes y características que se usan en las expresiones condicionales. Estos Estados no se establecen hasta que se llama a [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) , ya sea directamente o mediante la acción [CostFinalize](costfinalize-action.md) .



| Estado                    | Value | Significado                                                         |
|--------------------------|-------|-----------------------------------------------------------------|
| INSTALLSTATE \_ desconocido    | -1    | No se realiza ninguna acción en la característica o componente.              |
| INSTALLSTATE \_ anunciado | 1     | Característica anunciada. Este estado no está disponible para los componentes de. |
| INSTALLSTATE \_ ausente     | 2     | La característica o componente no está presente.                            |
| INSTALLSTATE \_ local      | 3     | Característica o componente en el equipo local.                     |
| origen de INSTALLSTATE \_     | 4     | La característica o componente se ejecuta desde el origen.                       |



 

Por ejemplo, la expresión condicional "&función = 3" solo se evalúa como true si la función está cambiando de su estado actual al estado de instalación en el equipo local, INSTALLSTATE \_ local.

Tenga en cuenta que no debe depender de la condición $Component 1 = 3 para comprobar si Component1 está instalado localmente en el equipo. Esto puede producir un error si Component1 está instalado por más de un producto. Una vez instalado Component1 localmente por Product1, el instalador evalúa la condición $Component 1 = 3 como false durante la instalación de product2. Esto se debe a que el instalador determina la versión del componente mediante la ruta de acceso de la clave del componente y marca el componente para la instalación si su versión es mayor o igual que el componente instalado.

Tenga en cuenta que el instalador no realizará comparaciones directas del tipo de datos de la [versión](version.md) en las instrucciones condicionales. Por ejemplo, no puede utilizar operadores de comparación para comparar versiones como "01,10" y "1,010" en una instrucción condicional. En su lugar, use un método válido para buscar una versión, como se describe en [Buscar aplicaciones, archivos, entradas del registro o entradas del archivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)y, a continuación, establecer una propiedad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar propiedades en instrucciones condicionales](using-properties-in-conditional-statements.md)
</dt> </dl>

 

 



