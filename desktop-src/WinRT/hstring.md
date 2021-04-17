---
description: Identificador de una cadena de Windows Runtime.
ms.assetid: 763ACE57-EFDD-482E-851E-668D7756C5DF
title: HSTRING (hstring. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9e73d7627a4bab8f02a95056e5b208569d922
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686780"
---
# <a name="hstring"></a>HSTRING

Identificador de una cadena de Windows Runtime.


```C++
typedef HSTRING__* HSTRING;
```



## <a name="remarks"></a>Observaciones

Use **HSTRING** para representar cadenas inmutables en el Windows Runtime.

JavaScript y otros lenguajes, como C \# y Microsoft Visual Basic, pueden usar cadenas que se representan mediante **HSTRING**. En la tabla siguiente se muestra cómo se representa un **HSTRING** en otros lenguajes.



| Lenguaje de programación                                                                    | Representación de cadena                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt)              | [winrt:: hstring](/uwp/cpp-ref-for-winrt/hstring) (clase)     |
| Extensiones de componentes Visual C++ ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx)) | [Platform:: String](/cpp/cppcx/platform-string-class) (clase) |
| JavaScript                                                                              | objeto de cadena                                              |
| .NET Framework                                                                          | clase System.String                                        |



 

El identificador de **HSTRING** es un tipo de identificador estándar. Semánticamente, un **HSTRING** que contiene el valor **null** representa la cadena vacía, que consta de cero caracteres de contenido y un carácter **nulo** de terminación. Al crear una cadena a través de [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) con cero caracteres, se generará el valor **null** del identificador. Al llamar a [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) con el valor **null**, se devolverá un puntero a una cadena vacía seguida solo por el carácter de terminación **NUL** . No existe ningún valor distinto para representar un **HSTRING** que no está inicializado.

Llame a la función [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) para crear un nuevo **HSTRING** y llame a la función [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) para liberar la referencia a la memoria de la cadena de respaldo. Llame a la función [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) para crear una referencia de cadena, que también se denomina *cadena de paso rápido*.

Copie un **HSTRING** mediante una llamada a la función [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) .

Concatene dos cadenas mediante una llamada a la función [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) .

Obtenga acceso a la memoria de la cadena de respaldo llamando a la función [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) .

**HSTRING** puede almacenar y usar caracteres **null** incrustados. Utilice la función [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) para comprobar los caracteres **null** incrustados antes de usar las funciones que pueden producir resultados inesperados. Por ejemplo, la mayoría de las funciones de Windows usan **LPCWSTR** como parámetro de entrada y calculan la longitud de la cadena solo hasta que se encuentra el primer **NUL** .

La cadena de respaldo debe permanecer inmutable y terminada en NULL. Cuando el código de llamada crea una referencia de cadena mediante la función [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) , el autor de la llamada es el propietario de la memoria que contiene la representación de la cadena de respaldo. El Windows Runtime se basa en el contenido de la cadena original para permanecer sin cambios. Al pasar una referencia de cadena en el Windows Runtime, es responsabilidad del autor de la llamada asegurarse de que el contenido de la cadena no cambia y **NUL** se termina mientras dure la llamada. El Windows Runtime libera todas las referencias a la referencia de cadena cuando se devuelve la llamada.

Cuando reciba un **HSTRING** como parámetro de salida, se recomienda establecer el identificador en **null** cuando termine de usarlo.

Llame a la función [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) para asignar un búfer de cadena mutable que puede usar para crear un **HSTRING** inmutable. Cuando haya terminado de rellenar el búfer, llame a la función [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) para crear el **HSTRING**. Este patrón de construcción en dos fases habilita una funcionalidad similar a un "generador de cadenas".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Hstring. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>


</dt> <dt>

[**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring)
</dt> <dt>

[**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring)
</dt> <dt>

[**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)
</dt> <dt>

[**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> </dl>

 

 
