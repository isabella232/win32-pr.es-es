---
title: " If, elif, else y directivas endif"
description: Directivas de preprocesador que controlan la compilación de partes de un archivo de código fuente.
ms.assetid: f29e5a9b-cc0c-4fca-aac7-809a226eda58
keywords:
- Directivas if, elif, else y endif HLSL
topic_type:
- apiref
api_name:
- if, elif, else, and endif Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb5f4716509905d4ce800abbe4cb11b85d116d7a5afd5a56301b1ecb5ce0724b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726455"
---
# <a name="if-elif-else-and-endif-directives"></a>\#If, \# elif, \# else y directivas \# endif

Directivas de preprocesador que controlan la compilación de partes de un archivo de código fuente.



| \#if *ifCondition* ...         |
|--------------------------------|
| \[\#elif *elifCondition* ...\] |
| \[\#Más...\]                 |
| \#endif                        |



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                                                                                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*<br/>                                                                                   | Condición principal que se debe evaluar. Si este parámetro se evalúa como un valor distinto de cero, todo el texto entre esta directiva if y la siguiente instancia de la directiva \# \# elif, else o endif se conserva en la unidad de traducción; de lo contrario, no se conserva el código fuente \# \# posterior. <br/> La condición puede usar el operador de preprocesador definido para determinar si se define una constante o macro de preprocesador específica; este uso es equivalente al uso de la [ \# directiva ifdef.](dx-graphics-hlsl-appendix-pre-ifdef.md) <br/> Consulte la sección Comentarios para ver las restricciones en el valor del *parámetro ifCondition.* <br/>                                                                                        |
| <span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[ Opcional\] <br/> | Otra condición que se evaluará. Si el parámetro *ifCondition* y todas las directivas elif anteriores se evalúan como cero y este parámetro se evalúa como un valor distinto de cero, todo el texto entre esta directiva elif y la siguiente instancia de la directiva \# elif, else o endif se conserva en la unidad de traducción; de lo contrario, no se conserva el código fuente \# \# \# \# posterior. <br/> La condición puede usar el operador de preprocesador definido para determinar si se define una constante o macro de preprocesador específica; este uso es equivalente al uso de la [ \# directiva ifdef.](dx-graphics-hlsl-appendix-pre-ifdef.md) <br/> Consulte la sección Comentarios para ver las restricciones en el valor del *parámetro elifCondition.* <br/> |



 

## <a name="remarks"></a>Comentarios

Cada \# directiva if de un archivo de código fuente debe coincidir con una directiva \# endif de cierre. Puede aparecer cualquier número de directivas elif entre las directivas if y endif, pero como máximo se permite \# \# otra \# \# directiva. La \# directiva else, si está presente, debe ser la última directiva antes \# de endif. Las directivas de compilación condicional contenidas en los archivos de incluyen deben cumplir las mismas condiciones.

Las directivas if, elif, else y endif pueden anidar en las partes de texto \# \# de \# \# \# otras directivas if. Cada directiva \# anidada else, \# elif o endif pertenece a la directiva if anterior más \# \# cercana.

Si ninguna condición se evalúa como un valor distinto de cero, el preprocesador selecciona el bloque de texto después de la \# directiva else. Si se omite la cláusula else y ninguna condición se evalúa como un valor distinto de \# cero, no se selecciona ningún bloque de texto.

Los *parámetros ifCondition* *y elifCondition* cumplen en gran parte los requisitos siguientes:

-   Las expresiones de [](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) compilación condicional se tratan como valores largos con firma y estas expresiones se evalúan con las mismas reglas que las expresiones de C++.
-   Las expresiones deben tener tipo entero y solo pueden incluir constantes de tipo entero, constantes de caracteres y el operador defined.
-   Las expresiones no pueden **usar sizeof** ni un operador de conversión de tipos.
-   Es posible que el entorno de destino no pueda representar todos los intervalos de enteros.
-   La traducción representa el tipo [**int**](/windows/desktop/WinProg/windows-data-types) igual que el tipo **long** y [**unsigned int**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) igual que **unsigned long**.
-   El traductor puede traducir constantes de caracteres a un conjunto de valores de código diferentes del conjunto para el entorno de destino. Para determinar las propiedades del entorno de destino, compruebe los valores de las macros de LIMITS.H en una aplicación compilada para el entorno de destino.
-   La expresión no debe realizar ninguna consulta de ambiente y debe permanecer aislada de los detalles de implementación del equipo de destino.

## <a name="examples"></a>Ejemplos

Esta sección contiene ejemplos que muestran cómo usar directivas de preprocesador de compilación condicional.

### <a name="use-of-the-defined-operator"></a>Uso del operador definido

En el ejemplo siguiente se muestra el uso del operador definido. Si se define el identificador CREDIT, se compila la llamada a la **función** de crédito. Si se define el identificador DEBIT, se compila la llamada a la función **de** débito. Si no se define ningún identificador, se compila la llamada a la función **printerror.** Tenga en cuenta que "CREDIT" y "credit" son identificadores distintos en C y C++ porque sus casos son diferentes.


```
#if defined(CREDIT)
    credit();
#elif defined(DEBIT)
    debit();
#else
    printerror();
#endif
```



### <a name="use-of-nested-if-directives"></a>Uso de directivas \# if anidadas

En el ejemplo siguiente se muestra cómo anidar \# directivas if. En este ejemplo se supone que se ha definido previamente una constante simbólica denominada DLEVEL. Las \# directivas elif y else se usan para tomar una de las cuatro \# opciones, en función del valor de DLEVEL. La constante STACK se establece en 0, 100 o 200, según la definición de DLEVEL. Si DLEVEL es mayor que 5, no se define STACK.


```
#if DLEVEL > 5
    #define SIGNAL  1
    #if STACKUSE == 1
        #define STACK   200
    #else
        #define STACK   100
    #endif
#else
    #define SIGNAL  0
    #if STACKUSE == 1
        #define STACK   100
    #else
        #define STACK   50
    #endif
#endif
#if DLEVEL == 0
    #define STACK 0
#elif DLEVEL == 1
    #define STACK 100
#elif DLEVEL > 5
    display( debugptr );
#else
    #define STACK 200
#endif
```



### <a name="use-for-including-header-files"></a>Uso para incluir archivos de encabezado

Un uso común para la compilación condicional es evitar inclusiones múltiples del mismo archivo de encabezado. En C++, donde las clases se definen a menudo en archivos de encabezado, se pueden usar construcciones de compilación condicionales para evitar varias definiciones. En el ejemplo siguiente se determina si se define la constante simbólica EXAMPLE \_ H. Si es así, el archivo ya se ha incluido y no es necesario volver a procesarlo; Si no es así, la constante EXAMPLE \_ H se define para indicar ese EJEMPLO. H ya se ha procesado.


```
#if !defined( EXAMPLE_H )
#define EXAMPLE_H

class Example
{
...
};

#endif // !defined( EXAMPLE_H )
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Directivas de preprocesador (HLSL de DirectX)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

