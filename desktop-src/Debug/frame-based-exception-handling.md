---
description: Un controlador de excepciones basado en marcos permite solucionar la posibilidad de que se produzca una excepción en una secuencia determinada de código. Un controlador de excepciones basado en marco consta de los siguientes elementos.
ms.assetid: 07aac772-f917-48b7-91a9-3b5d4cb43600
title: Control de excepciones basado en marcos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12b268b5d02de83bca22a1d3311905b05be1f748
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496384"
---
# <a name="frame-based-exception-handling"></a>Control de excepciones basado en marcos

Un *controlador de excepciones basado en marcos* permite solucionar la posibilidad de que se produzca una excepción en una secuencia determinada de código. Un controlador de excepciones basado en marco consta de los siguientes elementos.

-   Un cuerpo protegido del código
-   Una expresión de filtro
-   Un bloque de controlador de excepciones

Los controladores de excepciones basados en marcos se declaran en la sintaxis específica del lenguaje. Por ejemplo, en el compilador de optimización de C/C++ de Microsoft, se implementan mediante **\_ \_ try** y **\_ \_ Except**. Para obtener más información, vea [Sintaxis de controlador](handler-syntax.md).

El *cuerpo protegido del código* es un conjunto de una o varias instrucciones para las que la expresión de filtro y el bloque de controlador de excepciones proporcionan protección de control de excepciones. El cuerpo protegido puede ser un bloque de código, un conjunto de bloques anidados o un procedimiento o una función completos. Mediante el compilador de optimización de C/C++ de Microsoft, un cuerpo protegido se incluye entre llaves ( {} ) después de la palabra clave **\_ \_ try** .

La *expresión de filtro* de un controlador de excepciones basado en marcos es una expresión evaluada por el sistema cuando se produce una excepción en el cuerpo protegido. Esta evaluación da como resultado una de las siguientes acciones del sistema.

-   El sistema detiene su búsqueda de un controlador de excepciones, restaura el estado del equipo y continúa la ejecución del subproceso en el punto en el que se produjo la excepción.
-   El sistema continúa buscando un controlador de excepciones.
-   El sistema transfiere el control al controlador de excepciones y la ejecución de subprocesos continúa secuencialmente en el marco de pila en el que se encuentra el controlador de excepciones. Si el controlador no está en el marco de pila en el que se produjo la excepción, el sistema desenreda la pila, saliendo del marco de pila actual y de cualquier otro marco de pila hasta que vuelva al marco de pila del controlador de excepciones. Antes de que se ejecute un controlador de excepciones, los controladores de terminación se ejecutan para los cuerpos protegidos del código que finalizaron como resultado de la transferencia de control al controlador de excepciones. Para obtener más información sobre los controladores de terminación, consulte [control de finalización](termination-handling.md).

La expresión de filtro puede ser una expresión simple o puede invocar una *función de filtro* que intenta controlar la excepción. Puede llamar a las funciones [**GetExceptionCode**](getexceptioncode.md) y [**GetExceptionInformation**](getexceptioninformation.md) desde una expresión de filtro para obtener información sobre la excepción que se está filtrando. **GetExceptionCode** devuelve un código que identifica el tipo de excepción y **GetExceptionInformation** devuelve un puntero a una estructura [**de \_ punteros de excepción**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) que contiene punteros a estructuras [**de \_ registro**](/windows/desktop/api/WinNT/ns-winnt-exception_record) de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) y de excepción.

No se puede llamar a estas funciones desde una función de filtro, pero sus valores devueltos se pueden pasar como parámetros a una función de filtro. [**GetExceptionCode**](getexceptioncode.md) se puede usar en el bloque de controlador de excepciones, pero [**GetExceptionInformation**](getexceptioninformation.md) no puede porque la información a la que apunta está normalmente en la pila y se destruye cuando el control se transfiere a un controlador de excepciones. Sin embargo, una aplicación puede copiar la información en un almacenamiento seguro para que esté disponible para el controlador de excepciones.

La ventaja de una función de filtro es que puede controlar una excepción y devolver un valor que hace que el sistema continúe la ejecución desde el punto en el que se produjo la excepción. En cambio, con un bloque de controlador de excepciones, la ejecución continúa secuencialmente desde el controlador de excepciones en lugar de desde el punto de la excepción.

Controlar una excepción puede ser tan sencillo como anotar un error y establecer una marca que se examinará más adelante, imprimiendo una advertencia o un mensaje de error o realizando alguna otra acción limitada. Si se puede continuar la ejecución, también puede ser necesario cambiar el estado de la máquina modificando el registro de contexto. Para obtener un ejemplo de una función de filtro que controla una excepción de error de página, vea [usar las funciones de memoria virtual](../memory/using-the-memory-management-functions.md).

La función [**UnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) se puede usar como una función de filtro en una expresión de filtro. Devuelve \_ \_ el controlador de ejecución de excepciones a menos que se esté depurando el proceso, en cuyo caso devuelve la búsqueda de la excepción \_ continue \_ .

 

 
