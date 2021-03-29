---
title: const (atributo)
description: La palabra clave const modifica el tipo de una declaración de tipos o el tipo de un parámetro de función, lo que impide variar el valor.
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
ms.openlocfilehash: 8d2980f0f484c838e4f972bbf12fb72173edb3e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789874"
---
# <a name="const-attribute"></a>const (atributo)

La palabra clave **const** modifica el tipo de una declaración de tipos o el tipo de un parámetro de función, lo que impide variar el valor.

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

*const-Type* 
</dt> <dd>

Especifica un entero, un carácter, una cadena o un tipo booleano válidos de MIDL. Entre los tipos de MIDL válidos se incluyen [**Small**](small.md), [**Short**](short.md), [**Long**](long.md), [**Char**](char-idl.md), **charÂ \***, [**WCHAR \_ t**](wchar-t.md), **WCHAR \_ tÂ \***, [**byte**](byte.md), **byteÂ \*** y [**voidÂ \***](void.md). Los tipos enteros y de caracteres pueden estar [**firmados**](signed.md) o [**sin firmar**](unsigned.md).

</dd> <dt>

*identifier* 
</dt> <dd>

Especifica un identificador de MIDL válido. Los identificadores de MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado, y deben comenzar por un carácter alfabético o de subrayado.

</dd> <dt>

*const-Expression* 
</dt> <dd>

Especifica una expresión, un identificador o una constante numérica o de caracteres adecuada para el tipo especificado: literales constantes de tipo entero o expresiones de entero constante para constantes de tipo entero. Expresiones booleanas que se pueden calcular en la compilación para tipos [**booleanos**](boolean.md) ; constantes de un solo carácter para tipos [**Char**](char-idl.md) ; y las constantes de cadena para los tipos de **\[** [**cadena**](string.md) **\]** . El [**tipo \* voidÂ**](void.md) solo se puede inicializar en **null**.

</dd> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica uno o más atributos que se aplican al tipo.

</dd> <dt>

*tipo de puntero* 
</dt> <dd>

Especifica un tipo de puntero MIDL válido.

</dd> <dt>

*declarador y lista de declaradores* 
</dt> <dd>

Especifica los declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers). La *lista de declaradores* consta de uno o varios declaradores, separados por comas. El identificador de nombre de parámetro en el declarador de función es opcional.

</dd> <dt>

*function-ATTR-List* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y los atributos de uso **\[** [**cadena**](string.md) **\]** , **\[** [**omitir**](ignore.md) **\]** y **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .

</dd> <dt>

*Type-Specifier* 
</dt> <dd>

Especifica un [ \_ tipo base](midl-base-types.md), [**un struct**](struct.md), una [**Unión**](union.md), un tipo de [**enumeración**](enum.md) o un identificador de tipo. Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.

</dd> <dt>

*PTR-decl* 
</dt> <dd>

Especifica cero o más declaradores de puntero. Un declarador de puntero es el mismo que el declarador de puntero utilizado en C. Se construye a partir del **\*** designador, modificadores como **Far** y el calificador **const**.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Especifica cero o más atributos direccionales, atributos de campo, atributos de uso y atributos de puntero adecuados para el tipo de parámetro especificado. Separe varios atributos con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

MIDL permite declarar tipos enteros constantes, de caracteres, de cadena y booleanos en el cuerpo de la interfaz del archivo IDL. Las declaraciones de tipos **const** se reproducen en el archivo de encabezado generado como directivas de **\# definición** .

Los compiladores de DCE IDL no admiten expresiones constantes. Por lo tanto, esta característica no está disponible cuando se usa el modificador [**/OSF**](-osf.md) del compilador MIDL.

Se puede usar una constante definida previamente como el valor asignado de una constante subsiguiente. El valor de una expresión integral constante se convierte automáticamente al tipo de entero correspondiente de acuerdo con las reglas de conversión de C.

El valor de una constante de caracteres debe ser un carácter ASCII entre comillas simples. Cuando la constante de caracteres es el propio carácter de comilla simple ('), el carácter de barra diagonal inversa ( \) debe preceder al carácter de comilla simple, como en \\ '.

El valor de una constante de cadena de caracteres debe ser una cadena entre comillas dobles. Dentro de una cadena, el carácter de barra diagonal inversa ( **\\** ) debe preceder a un carácter de comilla doble literal ( **"** ), como en **\\ "**. Dentro de una cadena, el carácter de barra diagonal inversa ( **\\** ) representa un carácter de escape. Las constantes de cadena pueden constar de hasta 255 caracteres.

El valor **null** es el único valor válido para las constantes de tipo [**voidÂ \***](void.md). Se omiten los atributos asociados a la declaración **const** .

El compilador MIDL no comprueba los errores de intervalo en la inicialización **const** . Por ejemplo, si especifica "const Short x = 0xFFFFFFFF;", el compilador MIDL no notificará un error y el inicializador se reproducirá en el archivo de encabezado generado.

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

[**matrices**](arrays-1.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**Booleano**](boolean.md)
</dt> <dt>

[**bytes**](byte.md)
</dt> <dt>

[**devolución de llamada**](callback.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[**enumeración**](enum.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**omitir**](ignore.md)
</dt> <dt>

[**localizar**](local.md)
</dt> <dt>

[**tal**](long.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**conectado**](signed.md)
</dt> <dt>

[**pequeño**](small.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**Destructor**](struct.md)
</dt> <dt>

[**Unión**](union.md)
</dt> <dt>

[**espeficarse**](unique.md)
</dt> <dt>

[**sin signo**](unsigned.md)
</dt> <dt>

[**void**](void.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 