---
title: Modificador /char
description: El modificador /char ayuda a garantizar que el compilador MIDL y el compilador de C funcionan juntos correctamente para todos los tipos char y small.
ms.assetid: 83f204cf-9cd0-42f3-bce7-b8f582e50e67
keywords:
- /char switch MIDL
topic_type:
- apiref
api_name:
- /char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2254db9d0f4efcd003362e4126c5c295ca532b2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159772"
---
# <a name="char-switch"></a>Modificador /char

El **modificador /char** ayuda a garantizar que el compilador MIDL y el compilador de C funcionan juntos correctamente para todos los [**tipos char**](char-idl.md) y [**small.**](small.md)

``` syntax
midl /char { signed | unsigned | ascii7 }
```

## <a name="switch-options"></a>Opciones de cambio

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="signed"></span><span id="SIGNED"></span>

<span id="signed"></span><span id="SIGNED"></span>signed*"


</dt> <dd>

Especifica que el tipo predeterminado del compilador de C para [**char**](char-idl.md) está firmado. Todas las apariciones de **char** no acompañadas de una especificación de signo se generan como unsigned char.

</dd> <dt>

<span id="unsigned"></span><span id="UNSIGNED"></span>

<span id="unsigned"></span><span id="UNSIGNED"></span>unsigned***


</dt> <dd>

Especifica que el tipo predeterminado del compilador de C para [**char**](char-idl.md) es unsigned. Todos los usos [**de pequeño**](small.md) que no van acompañados de una especificación de signo se generan como pequeños firmados.

</dd> <dt>

<span id="ascii7"></span><span id="ASCII7"></span>

<span id="ascii7"></span><span id="ASCII7"></span>ascii7**


</dt> <dd>

Especifica que todos los [**valores char**](char-idl.md) se van a pasar a los archivos generados sin una palabra clave de signo específica. Todos los usos [**de pequeño**](small.md) que no van acompañados de una especificación de signo se generan como **pequeños.**

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Por definición, midL [**char**](char-idl.md) no tiene signo. "Small" se define en términos de **char** ( \# define small char) y MIDL [**small**](small.md) está firmado.

El **modificador /char** dirige al compilador [](signed.md) MIDL [](unsigned.md) para especificar declaraciones explícitas con signo o sin signo en los archivos generados cuando la declaración de signo del compilador de C entra en conflicto con el valor predeterminado de MIDL para ese tipo.

Recuerde que el compilador MIDL genera los códigos auxiliares como código fuente de C, que debe compilar como parte de los programas cliente y servidor. Algunos compiladores usan un **carácter con firma en** todas las partes en las que se especifican los datos char en el código fuente. [](char-idl.md) El código fuente de código auxiliar que genera el compilador MIDL trata todos los datos **char** **como unsigned char**. Si el compilador MIDL simplemente genera todos los datos **char** en el archivo IDL como datos **char** en los códigos auxiliares, los compiladores que usan un **carácter** con firma para los datos **char** provocarían un conflicto en el código fuente del código auxiliar.

El propósito del modificador de línea de comandos **/char** es resolver estos posibles conflictos. Conserva todos los datos especificados como [**char**](char-idl.md) en el archivo IDL **como unsigned char** en el código fuente del código auxiliar. También mantiene datos [**pequeños como**](small.md) firmados.

En la tabla siguiente se resumen los tipos generados.



| midl /char , opción       | Tipo char generado | Tipo pequeño generado |
|-------------------------|---------------------|----------------------|
| **midl /char signed**   | **unsigned char**   | **small**            |
| **midl /char unsigned** | **char**            | **signed small**     |
| **midl /char ascii7**   | **char**            | **small**            |



 

La **opción /char** signed indica que los tipos char y small del compilador de C están firmados. Para que coincida con el valor predeterminado de MIDL para **char**, el compilador de MIDL debe convertir todos los usos de **char** no acompañados de una especificación de signo en **unsigned char**. El [**tipo**](small.md) pequeño no se modifica porque este valor predeterminado del compilador de C coincide con el valor predeterminado de MIDL para **el pequeño**.

La **opción /char** unsigned indica que el tipo char del [**compilador**](char-idl.md) de C no tiene signo. El compilador MIDL convierte todos los usos de [**pequeño**](small.md) no acompañado de una especificación de signo en **signed** **small**.

La opción ascii7 indica que no se agrega ninguna especificación de signo explícita a los [**tipos char.**](char-idl.md) El tipo [**pequeño**](small.md) se genera como **pequeño.**

Para evitar confusiones, debe usar especificaciones de signo explícitas para los tipos [**char**](char-idl.md) y small siempre que sea posible en el archivo IDL. Tenga en cuenta que el uso de tipos **char** firmados explícitamente en el archivo IDL no es compatible con DCE IDL. Por lo tanto, esta característica no está disponible cuando se compila con el modificador MIDL [**/osf.**](-osf.md)

Para obtener más información relacionada **con /char**, vea [**small**](small.md).

## <a name="examples"></a>Ejemplos

**midl /char signed filename.idl**

**midl /char unsigned filename.idl**

**midl /char ascii7 filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Pequeño**](small.md)
</dt> </dl>

 

 




