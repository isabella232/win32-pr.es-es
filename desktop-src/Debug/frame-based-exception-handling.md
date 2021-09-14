---
description: Un controlador de excepciones basado en fotogramas permite tratar la posibilidad de que se produzca una excepción en una secuencia de código determinada. Un controlador de excepciones basado en marco consta de los siguientes elementos.
ms.assetid: 07aac772-f917-48b7-91a9-3b5d4cb43600
title: Control de excepciones basado en fotogramas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12b268b5d02de83bca22a1d3311905b05be1f748
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164649"
---
# <a name="frame-based-exception-handling"></a>Control de excepciones basado en fotogramas

Un *controlador de excepciones basado en fotogramas* permite tratar la posibilidad de que se produzca una excepción en una secuencia de código determinada. Un controlador de excepciones basado en marco consta de los siguientes elementos.

-   Un cuerpo de código guardado
-   Una expresión de filtro
-   Un bloque de controlador de excepciones

Los controladores de excepciones basados en fotogramas se declaran en sintaxis específica del lenguaje. Por ejemplo, en el compilador de optimización de Microsoft C/C++, se implementan **\_ \_ mediante try** y , **\_ \_ excepto**. Para obtener más información, vea [Sintaxis del controlador](handler-syntax.md).

El *cuerpo de código guardado es* un conjunto de una o varias instrucciones para las que la expresión de filtro y el bloque de controlador de excepciones proporcionan protección para el control de excepciones. El cuerpo guardado puede ser un bloque de código, un conjunto de bloques anidados o un procedimiento o función completos. Con el compilador de optimización de Microsoft C/C++, un cuerpo guardado se incluye entre llaves ( ) después {} de la palabra clave **\_ \_ try.**

La *expresión de filtro* de un controlador de excepciones basado en fotogramas es una expresión que evalúa el sistema cuando se produce una excepción dentro del cuerpo de protección. Esta evaluación da como resultado una de las siguientes acciones por parte del sistema.

-   El sistema detiene la búsqueda de un controlador de excepciones, restaura el estado de la máquina y continúa la ejecución del subproceso en el punto en el que se produjo la excepción.
-   El sistema continúa la búsqueda de un controlador de excepciones.
-   El sistema transfiere el control al controlador de excepciones y la ejecución del subproceso continúa secuencialmente en el marco de pila en el que se encuentra el controlador de excepciones. Si el controlador no está en el marco de pila en el que se produjo la excepción, el sistema desenreda la pila, dejando el marco de pila actual y cualquier otro marco de pila hasta que vuelva al marco de pila del controlador de excepciones. Antes de que se ejecute un controlador de excepciones, se ejecutan controladores de terminación para cualquier cuerpo de código guardado que finalice como resultado de la transferencia del control al controlador de excepciones. Para obtener más información sobre los controladores de terminación, consulte [Control de terminación.](termination-handling.md)

La expresión de filtro puede ser una expresión simple o puede invocar una *función de filtro* que intenta controlar la excepción. Puede llamar a las [**funciones GetExceptionCode**](getexceptioncode.md) y [**GetExceptionInformation**](getexceptioninformation.md) desde una expresión de filtro para obtener información sobre la excepción que se filtra. **GetExceptionCode devuelve** un código que identifica el tipo de excepción y **GetExceptionInformation** devuelve un puntero a una estructura [**EXCEPTION \_ POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) que contiene punteros a las estructuras [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) y [**EXCEPTION \_ RECORD.**](/windows/desktop/api/WinNT/ns-winnt-exception_record)

No se puede llamar a estas funciones desde dentro de una función de filtro, pero sus valores devueltos se pueden pasar como parámetros a una función de filtro. [**GetExceptionCode se**](getexceptioncode.md) puede usar dentro del bloque de controlador de excepciones, pero [**GetExceptionInformation**](getexceptioninformation.md) no puede porque la información a la que apunta suele estar en la pila y se destruye cuando el control se transfiere a un controlador de excepciones. Sin embargo, una aplicación puede copiar la información en un almacenamiento seguro para que esté disponible para el controlador de excepciones.

La ventaja de una función de filtro es que puede controlar una excepción y devolver un valor que hace que el sistema continúe con la ejecución desde el punto en el que se produjo la excepción. En cambio, con un bloque de controlador de excepciones, la ejecución continúa secuencialmente desde el controlador de excepciones en lugar de desde el punto de la excepción.

Controlar una excepción puede ser tan sencillo como advertir un error y establecer una marca que se examinará más adelante, imprimir un mensaje de error o una advertencia, o realizar alguna otra acción limitada. Si la ejecución puede continuar, también puede ser necesario cambiar el estado de la máquina modificando el registro de contexto. Para obtener un ejemplo de una función de filtro que controla una excepción de error de página, vea [Usar las funciones de memoria virtual](../memory/using-the-memory-management-functions.md).

La [**función UnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) se puede usar como función de filtro en una expresión de filtro. Devuelve EXCEPTION EXECUTE HANDLER a menos que el proceso \_ se esté depurando, en cuyo caso devuelve EXCEPTION CONTINUE \_ \_ \_ SEARCH.

 

 
