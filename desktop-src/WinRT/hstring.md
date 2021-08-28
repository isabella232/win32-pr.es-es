---
description: Identificador de una cadena Windows runtime.
ms.assetid: 763ACE57-EFDD-482E-851E-668D7756C5DF
title: HSTRING (Hstring.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4b43c92d439cec10c0d1683efb1e8ceafd8165a35c3c8aa9a1b35150e43a33a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121575"
---
# <a name="hstring"></a>HSTRING

Identificador de una cadena Windows runtime.


```C++
typedef HSTRING__* HSTRING;
```



## <a name="remarks"></a>Comentarios

Use **HSTRING para** representar cadenas inmutables en el entorno Windows runtime.

JavaScript y otros lenguajes, como C y Microsoft Visual Basic, pueden usar \# cadenas representadas mediante **HSTRING**. En la tabla siguiente se muestra **cómo se representa un HSTRING** en otros lenguajes.



| Lenguaje de programación                                                                    | Representación de cadena                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt)              | [winrt::hstring (clase)](/uwp/cpp-ref-for-winrt/hstring)     |
| Visual C++ de componentes ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx)) | [Platform::String (Clase)](/cpp/cppcx/platform-string-class) |
| JavaScript                                                                              | objeto de cadena                                              |
| .NET Framework                                                                          | clase System.String                                        |



 

El **identificador HSTRING** es un tipo de identificador estándar. Semánticamente, un **HSTRING** que contiene el valor **NULL** representa la cadena vacía, que consta de cero caracteres de contenido y un carácter **NULL final.** La creación de una cadena [**a través de WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) con cero caracteres producirá el valor de identificador **NULL.** Al llamar [**a WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) con el valor **NULL**, se devolverá un puntero a una cadena vacía seguida únicamente del carácter de terminación **NUL.** No existe ningún valor distinto para representar un **HSTRING** que no está inicializado.

Llame a [**la función WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) para crear una nueva **cadena HSTRING** y llame a la función [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) para liberar la referencia a la memoria de la cadena de respaldo. Llame a [**la función WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) para crear una referencia de cadena, que también se denomina cadena *de paso rápido.*

Copie un **HSTRING llamando** a la [**función WindowsDuplicateString.**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)

Concatene dos cadenas mediante una llamada a la [**función WindowsConcatString.**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring)

Acceda a la memoria de la cadena de respaldo mediante una llamada a la [**función WindowsGetStringRawBuffer.**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer)

**HSTRING puede** almacenar y usar caracteres **NUL incrustados.** Use la [**función WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) para comprobar si hay caracteres **NUL** incrustados antes de usar cualquier función que pueda producir resultados inesperados. Por ejemplo, la mayoría de las Windows usan **LPCWSTR** como parámetro de entrada y calculan la longitud de la cadena solo hasta que se encuentra el **primer NUL.**

La cadena de respaldo debe permanecer inmutable y terminada en NULL. Al llamar a código crea una referencia de cadena mediante la función [**WindowsCreateStringReference,**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) la memoria que contiene la representación de la cadena de respaldo es propiedad del autor de la llamada. El Windows runtime se basa en el contenido de la cadena original para permanecer sin cambios. Al pasar una referencia de cadena al runtime de Windows, es responsabilidad del autor de la llamada asegurarse de que el contenido de la cadena no cambia y que **nul** finaliza mientras dura la llamada. El Windows runtime libera todas las referencias a la referencia de cadena cuando se devuelve la llamada.

Cuando reciba un **HSTRING como** parámetro out, es una buena práctica establecer el identificador en **NULL** cuando haya terminado con él.

Llame a [**la función WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) para asignar un búfer de cadena mutable que puede usar para crear un **HSTRING** inmutable. Cuando haya terminado de rellenar el búfer, llame a la función [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) para crear **HSTRING.** Este patrón de construcción en dos fases permite una funcionalidad similar a un "generador de cadenas".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| Header<br/>                   | <dl> <dt>Hstring.h</dt> </dl> |



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

 

 
