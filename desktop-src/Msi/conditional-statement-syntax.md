---
description: En esta sección se describe la sintaxis de las instrucciones condicionales utilizadas por la función MsiEvaluateCondition y las tablas de secuencia de acciones. Para obtener más información, vea Ejemplos de sintaxis de instrucciones condicionales.
ms.assetid: 6f1657f9-063b-4d57-ad76-95e3dbe25786
title: Sintaxis de instrucciones condicionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f131cf9513d4bf19bb84c5777d1fed1411a682ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158815"
---
# <a name="conditional-statement-syntax"></a>Sintaxis de instrucciones condicionales

En esta sección se describe la sintaxis de las instrucciones condicionales utilizadas por la [**función MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) y las tablas de [secuencia de acciones](using-a-sequence-table.md). Para obtener más información, vea Ejemplos [de sintaxis de instrucciones condicionales.](examples-of-conditional-statement-syntax.md)

## <a name="summary-of-conditional-statement-syntax"></a>Resumen de la sintaxis de instrucciones condicionales

En esta tabla y en la lista siguiente se resume la sintaxis que se va a usar en expresiones condicionales.



| Elemento                | Sintaxis                                                                                                          |
|---------------------|-----------------------------------------------------------------------------------------------------------------|
| value               | entero \| literal \| de símbolo                                                                                    |
| comparison-operator | < \| > \| <= \| >= \| = \| <>                                                                 |
| término                | value \| value comparison-operator value \| ( expression )\|                                                    |
| Factor booleano      | term \| **NOT** term                                                                                            |
| Término booleano        | Boolean-factor \| Boolean-factor **AND** term                                                                   |
| expresión          | Boolean-term \| boolean-term **OR** expression                                                                  |
| símbolo              | propiedad \| %environment-variable \| $component-action \| ?component-state \| &feature-action \| !feature-state |



 

-   Los nombres de símbolos y los valores distinguen mayúsculas de minúsculas.
-   Los nombres de variables de entorno no distinguen mayúsculas de minúsculas.
-   El texto literal debe ir entre comillas ("texto").
    > [!Note]  
    > El texto literal que contiene comillas no se puede usar en instrucciones condicionales porque no hay ningún carácter de escape para las comillas dentro del texto literal. Para realizar una comparación con el texto literal que contiene comillas, el texto literal debe colocarse en una propiedad . Por ejemplo, para comprobar que la propiedad SERVERNAME no contiene comillas, defina una propiedad denominada QUOTES en la tabla [Property](property-table.md) con un valor de " y cambie la condición a NOT SERVERNAME><QUOTES.

     

-   Los valores de propiedad inexistentes se tratan como cadenas vacías.
-   No se admiten valores numéricos de punto flotante.
-   Los operadores y la precedencia son los mismos que en los lenguajes BASIC y SQL.
-   No se admiten operadores aritméticos.
-   Los paréntesis se pueden usar para invalidar la precedencia del operador.
-   Los operadores no distinguen mayúsculas de minúsculas.
-   Para las comparaciones de cadenas, una tilde "~" con el prefijo del operador realiza una comparación que no distingue mayúsculas de minúsculas.
-   La comparación de un entero con un valor de cadena o propiedad que no se puede convertir en un entero siempre es **msiEvaluateConditionFalse**, excepto para el operador de comparación "<>", que devuelve **msiEvaluateConditionTrue**.

## <a name="access-prefixes"></a>Prefijos de acceso

En la tabla siguiente se muestran los prefijos que se usarán para tener acceso a la información del sistema y del instalador para su uso en expresiones condicionales.



| Tipo de símbolo          | Prefijo | Value                                                     |
|----------------------|--------|-----------------------------------------------------------|
| Propiedad installer   | (ninguno) | Valor de la tabla property ([Property](property-table.md)). |
| Variable de entorno | %      | Valor de la variable de entorno.                            |
| Clave de tabla de componentes  | $      | Estado de acción del componente.                            |
| Clave de tabla de componentes  | ?      | Estado instalado del componente.                         |
| Clave de tabla de características    | &      | Estado de acción de la característica.                              |
| Clave de tabla de características    | !      | Estado instalado de la característica.                           |



 

## <a name="logical-operators"></a>Operadores lógicos

En la tabla siguiente se muestran los operadores lógicos en expresiones condicionales, en orden de prioridad de alta a baja.



| Operator | Significado                                                 |
|----------|---------------------------------------------------------|
| Not      | Operador unario de prefijo; invierte el estado del término siguiente. |
| And      | TRUE si ambos términos son TRUE.                            |
| Or       | TRUE si uno o ambos términos son TRUE.                  |
| Xor      | TRUE si ambos términos son TRUE.             |
| Eqv      | TRUE si ambos términos son TRUE o ambos términos son FALSE.    |
| Imp      | TRUE si el término izquierdo es FALSE o el término derecho es TRUE.       |



 

## <a name="comparative-operators"></a>Operadores comparativos

En la tabla siguiente se muestran los operadores de comparación usados en expresiones condicionales. Estos operadores de comparación solo pueden producirse entre dos valores.



| Operator | Significado                                                     |
|----------|-------------------------------------------------------------|
| =        | TRUE si el valor izquierdo es igual al valor derecho.                 |
| <> | TRUE si el valor izquierdo no es igual al valor derecho.             |
| >     | TRUE si el valor izquierdo es mayor que el valor derecho.             |
| >=    | TRUE si el valor izquierdo es mayor o igual que el valor derecho. |
| <     | TRUE si el valor izquierdo es menor que el valor derecho.                |
| <=    | TRUE si el valor izquierdo es menor o igual que el valor derecho.    |



 

## <a name="substring-operators"></a>Operadores de subcadena

En la tabla siguiente se muestran los operadores de subcadena utilizados en expresiones condicionales. Los operadores de subcadena pueden producirse entre dos valores de cadena.



| Operator | Significado                                           |
|----------|---------------------------------------------------|
| >< | TRUE si la cadena izquierda contiene la cadena derecha.    |
| << | TRUE si la cadena izquierda comienza por la cadena derecha. |
| >> | TRUE si la cadena izquierda termina con la cadena derecha.   |



 

## <a name="bitwise-numeric-operators"></a>Operadores numéricos bit a bit

En la tabla siguiente se muestran los operadores numéricos bit a bit en expresiones condicionales. Estos operadores pueden producirse entre dos valores enteros.



| Operator | Significado                                                                      |
|----------|------------------------------------------------------------------------------|
| >< | AND bit a bit, TRUE si los enteros izquierdo y derecho tienen bits en común.    |
| << | True si los 16 bits superiores del entero izquierdo son iguales al entero derecho. |
| >> | True si los 16 bits inferiores del entero izquierdo son iguales al entero derecho.  |



 

## <a name="feature-and-component-state-values"></a>Valores de estado de características y componentes

En la tabla siguiente se muestra dónde es válido usar los símbolos de operador de características y componentes.



| Estado del &lt; operador&gt; | Donde esta sintaxis es válida                                                                                                                                         |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| $component acción      | En la [tabla Condición](condition-table.md) y en las tablas [de](using-a-sequence-table.md) secuencia, después de la [acción CostFinalize.](costfinalize-action.md) |
| &característica-acción        | En la [tabla Condición](condition-table.md) y en las tablas [de](using-a-sequence-table.md) secuencia, después de la [acción CostFinalize.](costfinalize-action.md) |
| !feature-state         | En la [tabla Condición](condition-table.md) y en las tablas [de](using-a-sequence-table.md) secuencia, después de la [acción CostFinalize.](costfinalize-action.md) |
| ?component-state       | En la [tabla Condición](condition-table.md) y en las tablas [de](using-a-sequence-table.md) secuencia, después de la [acción CostFinalize.](costfinalize-action.md) |



 

En la tabla siguiente se muestran los valores de estado de característica y componente utilizados en expresiones condicionales. Estos estados no se establecen hasta que se llama a [**MsiSetInstallLevel,**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) ya sea directamente o mediante la [acción CostFinalize.](costfinalize-action.md)



| Estado                    | Value | Significado                                                         |
|--------------------------|-------|-----------------------------------------------------------------|
| INSTALLSTATE \_ UNKNOWN    | -1    | No se debe realizar ninguna acción en la característica o el componente.              |
| INSTALLSTATE \_ ANUNCIADO | 1     | Característica anunciada. Este estado no está disponible para los componentes. |
| INSTALLSTATE \_ ABSENT     | 2     | La característica o componente no está presente.                            |
| INSTALLSTATE \_ LOCAL      | 3     | Característica o componente en el equipo local.                     |
| INSTALLSTATE \_ SOURCE     | 4     | La característica o el componente se ejecutan desde el origen.                       |



 

Por ejemplo, la expresión condicional "&MyFeature=3" se evalúa como True solo si MyFeature cambia de su estado actual al estado de instalación en el equipo local, INSTALLSTATE \_ LOCAL.

Tenga en cuenta que no debe depender de la condición $Component 1=3 para comprobar si Component1 está instalado localmente en el equipo. Esto puede producir un error si Component1 está instalado por más de un producto. Después de que Product1 haya instalado Component1 localmente, el instalador evalúa la condición $Component 1=3 como False durante la instalación de Product2. Esto se debe a que el instalador determina la versión del componente mediante la ruta de acceso de clave del componente y marca el componente para la instalación si su versión es mayor o igual que el componente instalado.

Tenga en cuenta que el instalador no realizará comparaciones directas del tipo de datos [Version](version.md) en instrucciones condicionales. Por ejemplo, no puede usar operadores comparativos para comparar versiones como "01.10" y "1.010" en una instrucción condicional. En su lugar, use un método válido para buscar una versión, como se describe en Búsqueda de aplicaciones [existentes, archivos,](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)entradas del Registro o entradas de archivo .ini y, a continuación, establezca una propiedad .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar propiedades en instrucciones condicionales](using-properties-in-conditional-statements.md)
</dt> </dl>

 

 



