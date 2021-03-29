---
title: modificador/Char
description: El modificador/char ayuda a asegurarse de que el compilador de MIDL y el compilador de C funcionan juntos correctamente para todos los tipos Char y Small.
ms.assetid: 83f204cf-9cd0-42f3-bce7-b8f582e50e67
keywords:
- /char modificador MIDL
topic_type:
- apiref
api_name:
- /char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2254db9d0f4efcd003362e4126c5c295ca532b2f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784240"
---
# <a name="char-switch"></a>modificador/Char

El modificador **/Char** ayuda a asegurarse de que el compilador de MIDL y el compilador de C funcionan juntos correctamente para todos los tipos [**Char**](char-idl.md) y [**Small**](small.md) .

``` syntax
midl /char { signed | unsigned | ascii7 }
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="signed"></span><span id="SIGNED"></span>

<span id="signed"></span><span id="SIGNED"></span>con signo * * * *


</dt> <dd>

Especifica que el tipo de compilador de C predeterminado para [**Char**](char-idl.md) es signed. Todas las apariciones de **Char** que no vayan acompañadas de una especificación de signo se generan como carácter sin signo.

</dd> <dt>

<span id="unsigned"></span><span id="UNSIGNED"></span>

<span id="unsigned"></span><span id="UNSIGNED"></span>sin signo * * * *


</dt> <dd>

Especifica que el tipo de compilador de C predeterminado para [**Char**](char-idl.md) es sin signo. Todos los usos de [**pequeño**](small.md) no acompañado por una especificación de signo se generan como pequeños firmados.

</dd> <dt>

<span id="ascii7"></span><span id="ASCII7"></span>

<span id="ascii7"></span><span id="ASCII7"></span>ascii7 * * * *


</dt> <dd>

Especifica que todos los valores [**Char**](char-idl.md) se van a pasar a los archivos generados sin una palabra clave de signo específica. Todos los usos de [**pequeño**](small.md) no acompañado por una especificación de signo se generan como **pequeños**.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Por definición, el [**carácter**](char-idl.md) de MIDL es sin signo. "Small" se define en términos de **Char** ( \# definir caracteres pequeños) y MIDL [**Small**](small.md) está firmado.

El modificador **/Char** indica al compilador de MIDL que especifique declaraciones con [**signo**](signed.md) o [**sin signo**](unsigned.md) explícitas en los archivos generados cuando la declaración de firma del compilador de C entra en conflicto con el valor predeterminado de MIDL para ese tipo.

Recuerde que el compilador MIDL genera el código auxiliar como código fuente de C, que debe compilar como parte de los programas de cliente y servidor. Algunos compiladores usan los datos de [**caracteres**](char-idl.md) **Char Everywhere con signo** que se especifican en el código fuente. El código fuente de código auxiliar que genera el compilador MIDL trata todos los datos **Char** como **Char sin signo**. Si el compilador MIDL simplemente generó todos los datos **Char** en el archivo IDL como datos **Char** en el código auxiliar, los compiladores que usan un **carácter signed char** para los datos **Char** causarían un conflicto en el código fuente de código auxiliar.

El propósito del modificador de la línea de comandos **/Char** es resolver estos posibles conflictos. Conserva todos los datos especificados como [**Char**](char-idl.md) en el archivo IDL como **unsigned char** en el código fuente del código auxiliar. También mantiene los datos [**pequeños**](small.md) como firmados.

En la tabla siguiente se resumen los tipos generados.



| MIDL/Char, opción       | Tipo char generado | Tipo pequeño generado |
|-------------------------|---------------------|----------------------|
| **/char de MIDL con signo**   | **unsigned char**   | **small**            |
| **/char de MIDL sin signo** | **char**            | **con signo pequeño**     |
| **ascii7/char MIDL**   | **char**            | **small**            |



 

La opción **/Char** signed indica que los tipos Char y Small del compilador de C están firmados. Para que coincida con el valor predeterminado de MIDL para **Char**, el compilador MIDL debe convertir todos los usos de **Char** no acompañados de una especificación de signo a **Char sin signo**. No se modifica el tipo [**pequeño**](small.md) porque este valor predeterminado del compilador de C coincide con el valor predeterminado de MIDL para un **pequeño**.

La opción unsigned de **/Char** indica que el tipo [**Char**](char-idl.md) del compilador de C no tiene signo. El compilador MIDL convierte todos los usos de [**pequeños**](small.md) no acompañados de una especificación de signo a una **pequeña** **firmada** .

La opción ascii7 indica que no se ha agregado ninguna especificación de signo explícita a los tipos [**Char**](char-idl.md) . El tipo [**Small**](small.md) se genera como **pequeño**.

Para evitar confusiones, debe utilizar especificaciones de signo explícitas para los tipos [**Char**](char-idl.md) y Small siempre que sea posible en el archivo IDL. Tenga en cuenta que el uso de tipos **Char** con firma explícita en el archivo IDL no es compatible con DCE IDL. Por lo tanto, esta característica no está disponible al compilar con el modificador [**/OSF**](-osf.md) de MIDL.

Para obtener más información relacionada con **/Char**, vea [**Small**](small.md).

## <a name="examples"></a>Ejemplos

**MIDL/char signed nombreDeArchivo. idl**

**/char de MIDL sin signo nombreDeArchivo. idl**

**MIDL/char ascii7 nombreDeArchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**char**](char-idl.md)
</dt> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**pequeño**](small.md)
</dt> </dl>

 

 




