---
title: " If, Elif, Else y endif (directivas)"
description: Directivas de preprocesador que controlan la compilación de partes de un archivo de código fuente.
ms.assetid: f29e5a9b-cc0c-4fca-aac7-809a226eda58
keywords:
- If, Elif, Else y endif (directivas HLSL)
topic_type:
- apiref
api_name:
- if, elif, else, and endif Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a32206232c726f19febf77c3f3270882894a6747
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149283"
---
# <a name="if-elif-else-and-endif-directives"></a>\#If, \# Elif, \# Else y \# endif (directivas)

Directivas de preprocesador que controlan la compilación de partes de un archivo de código fuente.



| \#Si *ifCondition* ...         |
|--------------------------------|
| \[\#Elif *elifCondition* ...\] |
| \[\#otra cosa...\]                 |
| \#endif                        |



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                                                                                                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*<br/>                                                                                   | Condición primaria que se va a evaluar. Si este parámetro se evalúa como un valor distinto de cero, todo el texto entre esta \# Directiva if y la siguiente instancia de la \# Directiva Elif, \# else o \# endif se conserva en la unidad de traducción; de lo contrario, el código fuente subsiguiente no se conserva. <br/> La condición puede utilizar el operador de preprocesador definido para determinar si se ha definido una constante o una macro de preprocesador específica; Este uso es equivalente al uso de la directiva [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) . <br/> Vea la sección Comentarios para conocer las restricciones sobre el valor del parámetro *ifCondition* . <br/>                                                                                        |
| <span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[ opta\] <br/> | Otra condición que se va a evaluar. Si el parámetro *ifCondition* y todas las \# directivas Elif anteriores se evalúan como cero, y este parámetro se evalúa como un valor distinto de cero, todo el texto entre esta \# Directiva Elif y la siguiente instancia de la \# Directiva Elif, \# else o \# endif se conserva en la unidad de traducción; de lo contrario, el código fuente subsiguiente no se conserva. <br/> La condición puede utilizar el operador de preprocesador definido para determinar si se ha definido una constante o una macro de preprocesador específica; Este uso es equivalente al uso de la directiva [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) . <br/> Vea la sección Comentarios para conocer las restricciones sobre el valor del parámetro *elifCondition* . <br/> |



 

## <a name="remarks"></a>Observaciones

Cada \# Directiva if en un archivo de código fuente debe coincidir con una \# Directiva de cierre endif. Puede aparecer cualquier número de \# directivas Elif entre las \# directivas if y \# endif, pero se permite como máximo una \# Directiva else. La \# Directiva else, si está presente, debe ser la última Directiva antes de \# endif. Las directivas de compilación condicional contenidas en archivos de inclusión deben cumplir las mismas condiciones.

Las \# directivas if, \# Elif, \# Else y \# endif pueden anidarse en las partes de texto de otras \# directivas if. Cada directiva anidada \# else, \# Elif o \# endif pertenece a la Directiva if anterior más cercana \# .

Si ninguna condición se evalúa como un valor distinto de cero, el preprocesador selecciona el bloque de texto después de la \# Directiva else. Si \# se omite la cláusula else y ninguna condición se evalúa como un valor distinto de cero, no se selecciona ningún bloque de texto.

Los parámetros *ifCondition* y *elifCondition* cumplen los requisitos siguientes:

-   Las expresiones de compilación condicional se tratan como valores [**largos con signo**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) y estas expresiones se evalúan con las mismas reglas que las expresiones en C++.
-   Las expresiones deben tener tipo entero y solo pueden incluir constantes de tipo entero, constantes de caracteres y el operador defined.
-   Las expresiones no pueden usar **sizeof** o un operador de conversión de tipos.
-   Es posible que el entorno de destino no pueda representar todos los intervalos de enteros.
-   La traducción representa el tipo [**int**](/windows/desktop/WinProg/windows-data-types) igual que el tipo **Long** y [**unsigned int**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) igual que **unsigned Long**.
-   El traductor puede traducir constantes de caracteres a un conjunto de valores de código diferentes del conjunto para el entorno de destino. Para determinar las propiedades del entorno de destino, compruebe los valores de las macros de LIMITS.H en una aplicación compilada para el entorno de destino.
-   La expresión no debe realizar ninguna consulta de ambiente y debe permanecer aislada de los detalles de implementación del equipo de destino.

## <a name="examples"></a>Ejemplos

Esta sección contiene ejemplos que muestran cómo usar las directivas de preprocesador de compilación condicional.

### <a name="use-of-the-defined-operator"></a>Uso del operador definido

En el siguiente ejemplo se muestra el uso del operador defined. Si se define el crédito del identificador, se compila la llamada a la función de **crédito** . Si se define el identificador de débito, se compila la llamada a la función de **débito** . Si no se define ningún identificador, se compila la llamada a la función **printerror** . Tenga en cuenta que "CREDIT" y "Credit" son identificadores distintos en C y C++ porque sus casos son diferentes.


```
#if defined(CREDIT)
    credit();
#elif defined(DEBIT)
    debit();
#else
    printerror();
#endif
```



### <a name="use-of-nested-if-directives"></a>Uso de \# directivas if anidadas

En el ejemplo siguiente se muestra cómo anidar \# directivas if. En este ejemplo se da por supuesto que se ha definido previamente una constante simbólica denominada DLEVEL. Las \# directivas Elif y \# else se usan para tomar una de las cuatro opciones, según el valor de DLEVEL. La pila de constantes se establece en 0, 100 o 200, en función de la definición de DLEVEL. Si DLEVEL es mayor que 5, la pila no está definida.


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



### <a name="use-for-including-header-files"></a>Usar para incluir archivos de encabezado

Un uso común para la compilación condicional es evitar inclusiones múltiples del mismo archivo de encabezado. En C++, donde las clases suelen definirse en archivos de encabezado, se pueden usar construcciones de compilación condicionales para evitar varias definiciones. En el ejemplo siguiente se determina si se define la constante simbólica EXAMPLE \_ H. Si es así, el archivo ya se ha incluido y no es necesario volver a procesarlo; Si no es así, se define el ejemplo de constante \_ H para indicar ese ejemplo. H ya se ha procesado.


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

[Directivas de preprocesador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

