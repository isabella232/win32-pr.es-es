---
title: Atributo const
description: La palabra clave const modifica el tipo de una declaración de tipo o el tipo de un parámetro de función, lo que impide que el valor varíe.
ms.assetid: 398fab76-93f3-4d5a-9223-1c57c612b2d7
keywords:
- atributo const MIDL
topic_type:
- apiref
api_name:
- const
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7095e29daf18dc111caf37038b06b0beff5245a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159647"
---
# <a name="const-attribute"></a>Atributo const

La **palabra clave const** modifica el tipo de una declaración de tipo o el tipo de un parámetro de función, lo que impide que el valor varíe.

``` syntax
const const-type identifier = const-expression ;

[ typedef [ , type-attribute-list ] ] const const-type declarator-list;

[ typedef [ , type-attribute-list ] ] pointer-type const declarator-list;

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [ [ parameter-attribute-list ] ] ) const; 

const-type [declarator], [ [ parameter-attribute-list ] ] pointer-type const [declarator], ...);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*const-type* 
</dt> <dd>

Especifica un entero MIDL válido, un carácter, una cadena o un tipo booleano. Los tipos MIDL válidos incluyen small [**,**](small.md) [**short**](short.md), [**long**](long.md), [**char**](char-idl.md), **\* charÂ*, __ [*wchar \_ t* *](wchar-t.md), **wchar \_ \* tÂ*_, _ [*byte* *](byte.md), **byteÂ \** _, y [_*voidÂ \**_](void.md). Los tipos enteros y de caracteres pueden [ser _ *signed* *](signed.md) [**o unsigned**](unsigned.md).

</dd> <dt>

*identifier* 
</dt> <dd>

Especifica un identificador MIDL válido. Los identificadores MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado y deben comenzar con un carácter alfabético o de subrayado.

</dd> <dt>

*const-expression* 
</dt> <dd>

Especifica una expresión, un identificador o una constante numérica o de caracteres adecuada para el tipo especificado: literales enteros constantes o expresiones de entero constante para constantes enteras; Expresiones booleanas que se pueden calcular durante la compilación para tipos [**booleanos;**](boolean.md) constantes de un solo carácter para [**tipos char;**](char-idl.md) y constantes de cadena para tipos **\[** [**de**](string.md) **\]** cadena. El [ * *tipo \* voidÂ* _](void.md) solo se puede inicializar en _*NULL**.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Especifica uno o varios atributos que se aplican al tipo.

</dd> <dt>

*pointer-type* 
</dt> <dd>

Especifica un tipo de puntero MIDL válido.

</dd> <dt>

*declarator y declarator-list* 
</dt> <dd>

Especifica declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers). La *lista de declaradores* consta de uno o varios declaradores, separados por comas. El identificador de nombre de parámetro en el declarador de función es opcional.

</dd> <dt>

*function-attr-list* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son la devolución de llamada , local; el atributo de puntero **\[** [](callback.md) **\]** **\[** [](local.md) **\]** **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md); **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** y la cadena de atributos de uso , ignore y el identificador de contexto .

</dd> <dt>

*type-specifier* 
</dt> <dd>

Especifica un tipo base , [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type o type identifier. [ \_](midl-base-types.md) Una especificación de almacenamiento opcional puede *preceder al especificador de tipo*.

</dd> <dt>

*ptr-decl* 
</dt> <dd>

Especifica cero o más declaradores de puntero. Un declarador de puntero es el mismo que el declarador de puntero usado en C. Se construye a partir del **\* *designador _ , modificadores como _* far** y el calificador **const**.

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Especifica cero o más atributos direccionales, atributos de campo, atributos de uso y atributos de puntero adecuados para el tipo de parámetro especificado. Separe varios atributos con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

MIDL permite declarar tipos enteros, caracteres, cadenas y booleanos constantes en el cuerpo de la interfaz del archivo IDL. **Las declaraciones** de tipo Const se reproducen en el archivo de encabezado generado como **\# directivas define.**

Los compiladores IDL de DCE no admiten expresiones constantes. Por lo tanto, esta característica no está disponible cuando se usa el modificador [**/osf**](-osf.md) del compilador midL.

Una constante definida previamente se puede usar como el valor asignado de una constante subsiguiente. El valor de una expresión entera constante se convierte automáticamente al tipo entero correspondiente de acuerdo con las reglas de conversión de C.

El valor de una constante de caracteres debe ser un carácter ASCII entre comillas simples. Cuando la constante de caracteres es el propio carácter de comilla simple ('), el carácter de barra diagonal inversa ( ) debe preceder al carácter de comilla \\ simple, como en \\ '.

El valor de una constante de cadena de caracteres debe ser una cadena entre comillas dobles. Dentro de una cadena, el carácter de barra diagonal inversa ( ) debe preceder a un carácter literal de comilla **\\** doble ( **"** ), como en **\\ "**. Dentro de una cadena, el carácter de barra diagonal inversa ( **\\** ) representa un carácter de escape. Las constantes de cadena pueden constar de hasta 255 caracteres.

El valor **NULL** es el único valor válido para las constantes de tipo [ * *voidÂ \** _](void.md). Se omiten todos los atributos asociados a la declaración _ *const**.

El compilador MIDL no comprueba si hay errores de intervalo en **la inicialización const.** Por ejemplo, cuando se especifica "const short x = 0xFFFFFFFF;", el compilador MIDL no informa de un error y el inicializador se reproduce en el archivo de encabezado generado.

## <a name="examples"></a>Ejemplos

``` syntax
const void *  p1        = NULL; 
const char    my_char1  = 'a'; 
const char    my_char2  = my_char1; 
const wchar_t my_wchar3 = L'a'; 
const wchar_t * pszNote = L"Note"; 
const unsigned short int x = 123; 
 
typedef [string] const char *LPCSTR; 
 
HRESULT GetName([out] wchar_t * const pszName );
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Matrices**](arrays-1.md)
</dt> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**Boolean**](boolean.md)
</dt> <dt>

[**Byte**](byte.md)
</dt> <dt>

[**devolución de llamada**](callback.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[**identificador de \_ contexto**](context-handle.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Ignorar**](ignore.md)
</dt> <dt>

[**Local**](local.md)
</dt> <dt>

[**Largo**](long.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Corto**](short.md)
</dt> <dt>

[**Firmado**](signed.md)
</dt> <dt>

[**Pequeño**](small.md)
</dt> <dt>

[**Cadena**](string.md)
</dt> <dt>

[**Estructura**](struct.md)
</dt> <dt>

[**union**](union.md)
</dt> <dt>

[**Único**](unique.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> <dt>

[**void**](void.md)
</dt> <dt>

[**wchar \_ t**](wchar-t.md)
</dt> </dl>

 

 