---
description: Recupera un código que identifica el tipo de excepción que se produce. Solo se puede llamar a la función desde dentro de la expresión de filtro o el bloque de controlador de excepciones de un controlador de excepciones.
ms.assetid: f3c4a9f3-c9ae-4d20-85a7-787cb32278d1
title: GetExceptionCode (macro)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetExceptionCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3b87b77ddb2d2e2af3a22e30d1204cf178ee6981
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659691"
---
# <a name="getexceptioncode-macro"></a>GetExceptionCode (macro)

Recupera un código que identifica el tipo de excepción que se produce. Solo se puede llamar a la función desde dentro de la expresión de filtro o el bloque de controlador de excepciones de un controlador de excepciones.

> [!Note]  
> El compilador de optimización de C/C++ de Microsoft interpreta esta función como una palabra clave y su uso fuera de la sintaxis de control de excepciones adecuada genera un error del compilador.

 

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetExceptionCode(void);
```



## <a name="parameters"></a>Parámetros

Esta macro no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El valor devuelto identifica el tipo de excepción. En la tabla siguiente se identifican los códigos de excepción que se pueden producir debido a errores de programación comunes. Estos valores se definen en WinBase. h y en Winnt. h.



| Código devuelto                                                                                                         | Descripción                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**infracción de acceso de excepción \_ \_**</dt> </dl>         | El subproceso intenta leer o escribir en una dirección virtual para la que no tiene acceso.<br/> Este valor se define como \_ infracción de acceso de estado \_ .<br/>                                                                                                                                                 |
| <dl> <dt>**se \_ han \_ superado los límites de la matriz de excepciones \_**</dt> </dl>   | El subproceso intenta tener acceso a un elemento de matriz que está fuera de los límites y el hardware subyacente admite la comprobación de límites.<br/> Este valor se define como límites de la matriz de estado \_ \_ \_ excedidos.<br/>                                                                                                                 |
| <dl> <dt>**punto de interrupción de excepción \_**</dt> </dl>                | Se encontró un punto de interrupción.<br/> Este valor se define como punto de interrupción de estado \_ .<br/>                                                                                                                                                                                                                             |
| <dl> <dt>**desalineación del tipo de carácter de excepción \_ \_**</dt> </dl>    | El subproceso intenta leer o escribir datos desalineados en hardware que no proporciona alineación. Por ejemplo, los valores de 16 bits se deben alinear en límites de 2 bytes, valores de 32 bits en límites de 4 bytes, etc.<br/> Este valor se define como mal alineación de tipo de carácter de estado \_ \_ .<br/>                    |
| <dl> <dt>**\_ \_ operando desnormalizado de excepción FLT \_**</dt> </dl>    | Uno de los operandos de una operación de punto flotante es desnormalizado. Un valor desnormalizado es el que es demasiado pequeño para representarlo como un valor de punto flotante estándar.<br/> Este valor se define como \_ \_ operando desnormalizado de estado Float \_ .<br/>                                                                                  |
| <dl> <dt>**EXCEPCIÓN \_ FLT \_ dividida \_ por \_ cero**</dt> </dl>     | El subproceso intenta dividir un valor de punto flotante en un divisor de punto flotante de 0 (cero).<br/> Este valor se define como estado \_ float \_ divide \_ por \_ cero.<br/>                                                                                                                                               |
| <dl> <dt>**\_ \_ resultado inexacto de la excepción FLT \_**</dt> </dl>      | El resultado de una operación de punto flotante no se puede representar exactamente como una fracción decimal.<br/> Este valor se define como el \_ resultado Float inexacto de status \_ \_ .<br/>                                                                                                                                                |
| <dl> <dt>**EXCEPCIÓN de la \_ operación de FLT \_ no válida \_**</dt> </dl>   | Una excepción de punto flotante que no se incluye en esta lista.<br/> Este valor se define como la \_ operación Float de estado \_ no válida \_ .<br/>                                                                                                                                                                             |
| <dl> <dt>**desbordamiento de la excepción \_ FLT \_**</dt> </dl>             | El exponente de una operación de punto flotante es mayor que la magnitud permitida por el tipo correspondiente.<br/> Este valor se define como estado \_ de \_ desbordamiento de float.<br/>                                                                                                                                         |
| <dl> <dt>**comprobación de la pila de la excepción \_ FLT \_ \_**</dt> </dl>         | La pila se ha desbordado o está subdesbordamiento, debido a una operación de punto flotante.<br/> Este valor se define como estado \_ float \_ stack \_ check.<br/>                                                                                                                                                                 |
| <dl> <dt>**subdesbordamiento de la excepción \_ FLT \_**</dt> </dl>            | El exponente de una operación de punto flotante es menor que la magnitud permitida por el tipo correspondiente.<br/> Este valor se define como un \_ subdesbordamiento de estado flotante \_ .<br/>                                                                                                                                           |
| <dl> <dt>**\_Página protección de excepciones \_**</dt> </dl>               | El subproceso ha tenido acceso a la memoria asignada con el \_ modificador de protección de páginas.<br/> Este valor se define como infracción de la página de estado de \_ protección \_ \_ .<br/>                                                                                                                                                                          |
| <dl> <dt>**\_instrucción no válida de excepción \_**</dt> </dl>      | El subproceso intenta ejecutar una instrucción no válida.<br/> Este valor se define como \_ instrucción no válida de estado \_ .<br/>                                                                                                                                                                                            |
| <dl> <dt>**EXCEPCIÓN \_ en \_ error de página \_**</dt> </dl>           | El subproceso intenta tener acceso a una página que no está presente y el sistema no puede cargar la página. Por ejemplo, esta excepción puede producirse si se pierde una conexión de red mientras se ejecuta un programa a través de una red.<br/> Este valor se define como estado \_ en \_ error de página \_ .<br/>                                   |
| <dl> <dt>**\_división int \_ \_ de excepción por \_ cero**</dt> </dl>     | El subproceso intenta dividir un valor entero por un divisor entero de 0 (cero).<br/> Este valor se define como el estado de \_ \_ división \_ de enteros por \_ cero.<br/>                                                                                                                                                         |
| <dl> <dt>**\_desbordamiento int de excepción \_**</dt> </dl>             | El resultado de una operación de entero crea un valor que es demasiado grande para que lo mantenga el registro de destino. En algunos casos, esto dará lugar a un transporte fuera del bit más significativo del resultado. Algunas operaciones no establecen la marca de transporte.<br/> Este valor se define como estado de \_ desbordamiento de enteros \_ .<br/> |
| <dl> <dt>**disposición de excepción \_ no válida \_**</dt> </dl>      | Un controlador de excepciones devuelve una disposición no válida al distribuidor de excepciones. Los programadores que usan un lenguaje de alto nivel, como C, nunca deben encontrar esta excepción.<br/> Este valor se define como la \_ disposición de estado no válida \_ .<br/>                                                                      |
| <dl> <dt>**identificador de excepción \_ no válido \_**</dt> </dl>           | El subproceso utilizó un identificador para un objeto de kernel que no era válido (probablemente porque se había cerrado).<br/> Este valor se define como un \_ identificador no válido de estado \_ .<br/>                                                                                                                                                 |
| <dl> <dt>**excepción no \_ continuada de excepción \_**</dt> </dl> | El subproceso intenta continuar la ejecución después de que se produzca una excepción no continuable.<br/> Este valor se define como excepción de estado no \_ continuable \_ .<br/>                                                                                                                                                       |
| <dl> <dt>**\_instrucción priv de excepción \_**</dt> </dl>         | El subproceso intenta ejecutar una instrucción con una operación que no está permitida en el modo de equipo actual.<br/> Este valor se define como instrucción con privilegios de estado \_ \_ .<br/>                                                                                                                           |
| <dl> <dt>**\_paso único de la excepción \_**</dt> </dl>              | Una captura de seguimiento u otro mecanismo de instrucción única indica que se ejecuta una instrucción.<br/> Este valor se define como estado de \_ un solo \_ paso.<br/>                                                                                                                                                           |
| <dl> <dt>**desbordamiento de la pila de excepciones \_ \_**</dt> </dl>           | El subproceso usa su pila.<br/> Este valor se define como desbordamiento de la pila de estado \_ \_ .<br/>                                                                                                                                                                                                                       |
| <dl> <dt>**desenredado de estado \_ \_ ConsoliDate**</dt> </dl>          | Se ha ejecutado una consolidación de fotogramas.<br/>                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Observaciones

Solo se puede llamar a la función **GetExceptionCode** desde dentro de la expresión de filtro o el bloque de controlador de excepciones de un controlador de excepciones. La expresión de filtro se evalúa si se produce una excepción durante la ejecución del bloque **\_ \_ try** y determina si se ejecuta el bloque **\_ \_ Except** .

La expresión de filtro puede invocar una función de filtro. La función Filter no puede llamar a **GetExceptionCode**. Sin embargo, el valor devuelto de **GetExceptionCode** se puede pasar como un parámetro a una función de filtro. El valor devuelto de la función [**GetExceptionInformation**](getexceptioninformation.md) también se puede pasar como un parámetro a una función de filtro. **GetExceptionInformation** devuelve un puntero a una estructura que incluye la información del código de la excepción.

Cuando existen controladores anidados, cada expresión de filtro se evalúa hasta que se evalúa una como controlador de ejecución de excepción o continuación de la ejecución de la \_ \_ excepción \_ \_ . Cada expresión de filtro puede invocar **GetExceptionCode** para obtener el código de excepción.

El código de excepción devuelto es el código generado por una excepción de hardware o el código especificado en la función [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) para una excepción generada por software.

Al controlar la excepción de punto de interrupción, es importante incrementar el puntero de instrucción en el registro de contexto para continuar a partir de esta excepción.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, vea [usar un controlador de excepciones](using-an-exception-handler.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetExceptionInformation**](getexceptioninformation.md)
</dt> <dt>

[**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)
</dt> <dt>

[Funciones de control de excepciones estructurado](structured-exception-handling-functions.md)
</dt> <dt>

[Información general sobre el control estructurado de excepciones](structured-exception-handling.md)
</dt> </dl>

 

 
