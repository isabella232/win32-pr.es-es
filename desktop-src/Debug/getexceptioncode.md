---
description: Recupera un código que identifica el tipo de excepción que se produce. Solo se puede llamar a la función desde la expresión de filtro o el bloque de controlador de excepciones de un controlador de excepciones.
ms.assetid: f3c4a9f3-c9ae-4d20-85a7-787cb32278d1
title: Macro GetExceptionCode
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164641"
---
# <a name="getexceptioncode-macro"></a>Macro GetExceptionCode

Recupera un código que identifica el tipo de excepción que se produce. Solo se puede llamar a la función desde la expresión de filtro o el bloque de controlador de excepciones de un controlador de excepciones.

> [!Note]  
> El compilador de optimización de Microsoft C/C++ interpreta esta función como una palabra clave y su uso fuera de la sintaxis de control de excepciones adecuada genera un error del compilador.

 

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetExceptionCode(void);
```



## <a name="parameters"></a>Parámetros

Esta macro no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El valor devuelto identifica el tipo de excepción. En la tabla siguiente se identifican los códigos de excepción que pueden producirse debido a errores de programación comunes. Estos valores se definen en WinBase.h y WinNT.h.



| Código devuelto                                                                                                         | Descripción                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**INFRACCIÓN DE \_ ACCESO DE \_ EXCEPCIONES**</dt> </dl>         | El subproceso intenta leer o escribir en una dirección virtual para la que no tiene acceso.<br/> Este valor se define como INFRACCIÓN \_ DE ACCESO DE \_ ESTADO.<br/>                                                                                                                                                 |
| <dl> <dt>**LÍMITES \_ DE \_ MATRIZ DE \_ EXCEPCIONES SUPERADOS**</dt> </dl>   | El subproceso intenta acceder a un elemento de matriz que está fuera de los límites y el hardware subyacente admite la comprobación de límites.<br/> Este valor se define como STATUS \_ ARRAY \_ BOUNDS \_ EXCEEDED.<br/>                                                                                                                 |
| <dl> <dt>**PUNTO DE \_ INTERRUPCIÓN DE EXCEPCIÓN**</dt> </dl>                | Se encuentra un punto de interrupción.<br/> Este valor se define como STATUS \_ BREAKPOINT.<br/>                                                                                                                                                                                                                             |
| <dl> <dt>**ERROR \_ DE ALINEACIÓN DEL TIPO \_ DE DATOS DE EXCEPCIÓN**</dt> </dl>    | El subproceso intenta leer o escribir datos que están mal alineados en hardware que no proporciona alineación. Por ejemplo, los valores de 16 bits deben estar alineados en límites de 2 bytes, valores de 32 bits en límites de 4 bytes, y así sucesivamente.<br/> Este valor se define como STATUS \_ DATATYPE \_ MISALIGNMENT.<br/>                    |
| <dl> <dt>**OPERANDO \_ \_ DESNORMAL DE \_ EXCEPCIÓN FLT**</dt> </dl>    | Uno de los operandos de una operación de punto flotante es desnormal. Un valor desnormal es demasiado pequeño para representarlo como un valor de punto flotante estándar.<br/> Este valor se define como STATUS \_ FLOAT \_ DENORMAL \_ OPERAND.<br/>                                                                                  |
| <dl> <dt>**EXCEPCIÓN \_ FLT \_ DIVIDE ENTRE \_ \_ CERO**</dt> </dl>     | El subproceso intenta dividir un valor de punto flotante entre un divisor de punto flotante de 0 (cero).<br/> Este valor se define como STATUS \_ FLOAT \_ DIVIDE BY \_ \_ ZERO.<br/>                                                                                                                                               |
| <dl> <dt>**RESULTADO \_ \_ INEXACT DE EXCEPCIÓN FLT \_**</dt> </dl>      | El resultado de una operación de punto flotante no se puede representar exactamente como una fracción decimal.<br/> Este valor se define como STATUS \_ FLOAT \_ INEXACT \_ RESULT.<br/>                                                                                                                                                |
| <dl> <dt>**EXCEPTION \_ FLT \_ INVALID \_ OPERATION**</dt> </dl>   | Excepción de punto flotante que no se incluye en esta lista.<br/> Este valor se define como STATUS \_ FLOAT \_ INVALID \_ OPERATION.<br/>                                                                                                                                                                             |
| <dl> <dt>**EXCEPCIÓN \_ FLT \_ OVERFLOW**</dt> </dl>             | El exponente de una operación de punto flotante es mayor que la magnitud permitida por el tipo correspondiente.<br/> Este valor se define como STATUS \_ FLOAT \_ OVERFLOW.<br/>                                                                                                                                         |
| <dl> <dt>**EXCEPTION \_ FLT \_ STACK \_ CHECK**</dt> </dl>         | La pila se ha desbordado o se ha desbordado debido a una operación de punto flotante.<br/> Este valor se define como STATUS \_ FLOAT \_ STACK \_ CHECK.<br/>                                                                                                                                                                 |
| <dl> <dt>**\_SUBDESBORDO DE EXCEPCIÓN \_ FLT**</dt> </dl>            | El exponente de una operación de punto flotante es menor que la magnitud permitida por el tipo correspondiente.<br/> Este valor se define como STATUS \_ FLOAT \_ UNDERFLOW.<br/>                                                                                                                                           |
| <dl> <dt>**PÁGINA \_ PROTECCIÓN DE \_ EXCEPCIONES**</dt> </dl>               | El subproceso ha accedido a la memoria asignada con el modificador PAGE \_ GUARD.<br/> Este valor se define como INFRACCIÓN DE PÁGINA DE PROTECCIÓN \_ \_ DE \_ ESTADO.<br/>                                                                                                                                                                          |
| <dl> <dt>**INSTRUCCIÓN \_ NO ILEGAL DE \_ EXCEPCIÓN**</dt> </dl>      | El subproceso intenta ejecutar una instrucción no válida.<br/> Este valor se define como INSTRUCCIÓN \_ STATUS \_ ILLEGAL.<br/>                                                                                                                                                                                            |
| <dl> <dt>**EXCEPCIÓN \_ EN \_ ERROR DE \_ PÁGINA**</dt> </dl>           | El subproceso intenta acceder a una página que no está presente y el sistema no puede cargar la página. Por ejemplo, esta excepción puede producirse si se pierde una conexión de red mientras se ejecuta un programa a través de una red.<br/> Este valor se define como STATUS \_ IN \_ PAGE \_ ERROR.<br/>                                   |
| <dl> <dt>**EXCEPTION \_ INT \_ DIVIDE \_ BY \_ ZERO**</dt> </dl>     | El subproceso intenta dividir un valor entero entre un divisor entero de 0 (cero).<br/> Este valor se define como STATUS \_ INTEGER \_ DIVIDE BY \_ \_ ZERO.<br/>                                                                                                                                                         |
| <dl> <dt>**EXCEPTION \_ INT \_ OVERFLOW**</dt> </dl>             | El resultado de una operación de entero crea un valor demasiado grande para que lo tenga el registro de destino. En algunos casos, esto dará como resultado una realización del bit más significativo del resultado. Algunas operaciones no establecen la marca de transporte.<br/> Este valor se define como STATUS \_ INTEGER \_ OVERFLOW.<br/> |
| <dl> <dt>**DISPOSICIÓN \_ NO VÁLIDA DE \_ EXCEPCIÓN**</dt> </dl>      | Un controlador de excepciones devuelve una disposición no válida al distribuidor de excepciones. Los programadores que usan un lenguaje de alto nivel como C nunca deben encontrar esta excepción.<br/> Este valor se define como STATUS \_ INVALID \_ DISPOSITION.<br/>                                                                      |
| <dl> <dt>**IDENTIFICADOR \_ DE EXCEPCIÓN NO \_ VÁLIDO**</dt> </dl>           | El subproceso usó un identificador para un objeto kernel que no era válido (probablemente porque se había cerrado).<br/> Este valor se define como STATUS \_ INVALID \_ HANDLE.<br/>                                                                                                                                                 |
| <dl> <dt>**EXCEPCIÓN \_ EXCEPCIÓN \_ NOTINUABLE**</dt> </dl> | El subproceso intenta continuar la ejecución después de que se produzca una excepción no continuable.<br/> Este valor se define como STATUS \_ NONCONTINUABLE \_ EXCEPTION.<br/>                                                                                                                                                       |
| <dl> <dt>**INSTRUCCIÓN \_ PRIV \_ DE EXCEPCIÓN**</dt> </dl>         | El subproceso intenta ejecutar una instrucción con una operación que no está permitida en el modo de equipo actual.<br/> Este valor se define como INSTRUCCIÓN CON \_ \_ PRIVILEGIOS DE ESTADO.<br/>                                                                                                                           |
| <dl> <dt>**PASO \_ ÚNICO DE \_ EXCEPCIÓN**</dt> </dl>              | Una captura de seguimiento u otro mecanismo de instrucción único indica que se ejecuta una instrucción.<br/> Este valor se define como STATUS \_ SINGLE \_ STEP.<br/>                                                                                                                                                           |
| <dl> <dt>**DESBORDAMIENTO \_ DE PILA \_ DE EXCEPCIONES**</dt> </dl>           | El subproceso usa su pila.<br/> Este valor se define como STATUS \_ STACK \_ OVERFLOW.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>**CONSOLIDACIÓN \_ DE DESENREDO \_ DE ESTADO**</dt> </dl>          | Se ha ejecutado una consolidación de fotogramas.<br/>                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Observaciones

Solo se puede llamar a la función **GetExceptionCode** desde la expresión de filtro o el bloque de controlador de excepciones de un controlador de excepciones. La expresión de filtro se evalúa si se produce una excepción durante la **\_ \_** ejecución del bloque **\_ \_ try** y determina si se ejecuta o no el bloque except.

La expresión de filtro puede invocar una función de filtro. La función filter no puede llamar **a GetExceptionCode.** Sin embargo, el valor devuelto **de GetExceptionCode** se puede pasar como parámetro a una función de filtro. El valor devuelto de la [**función GetExceptionInformation**](getexceptioninformation.md) también se puede pasar como parámetro a una función de filtro. **GetExceptionInformation** devuelve un puntero a una estructura que incluye la información del código de excepción.

Cuando existen controladores anidados, cada expresión de filtro se evalúa hasta que se evalúa como EXCEPTION \_ EXECUTE HANDLER o EXCEPTION CONTINUE \_ \_ \_ EXECUTION. Cada expresión de filtro puede invocar **GetExceptionCode para** obtener el código de excepción.

El código de excepción devuelto es el código generado por una excepción de hardware o el código especificado en la función [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) para una excepción generada por software.

Al controlar la excepción de punto de interrupción, es importante incrementar el puntero de instrucción en el registro de contexto para continuar con esta excepción.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo, vea [Usar un controlador de excepciones.](using-an-exception-handler.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**GetExceptionInformation**](getexceptioninformation.md)
</dt> <dt>

[**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)
</dt> <dt>

[Funciones de control de excepciones estructurado](structured-exception-handling-functions.md)
</dt> <dt>

[Información general sobre el control de excepciones estructurado](structured-exception-handling.md)
</dt> </dl>

 

 
