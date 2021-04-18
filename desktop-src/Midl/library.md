---
title: atributo de biblioteca
description: La instrucción Library contiene toda la información que el compilador MIDL utiliza para generar una biblioteca de tipos.
ms.assetid: d73acb17-abe4-4c31-a264-a131d1f9fa51
keywords:
- MIDL (atributo de biblioteca)
topic_type:
- apiref
api_name:
- library
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100c901c6b5d86ed3420d51e459627bdb5b461b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665821"
---
# <a name="library-attribute"></a>atributo de biblioteca

La instrucción **Library** contiene toda la información que el compilador MIDL utiliza para generar una biblioteca de tipos.

``` syntax
[
    uuid(uuid-number), 
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*UUID-número* 
</dt> <dd>

Especifica un número de identificación único universal para la biblioteca.

</dd> <dt>

*opcional-Attribute-List* 
</dt> <dd>

Especifica atributos adicionales que se aplican a toda la instrucción **Library** . Entre los atributos permitidos se incluyen **\[** [**control**](control.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**HelpFile**](helpfile.md) **\]** , **\[** [**HelpString**](helpstring.md) **\]** , **\[** [**Hidden**](hidden.md), **\]** **\[** [**LCID**](lcid.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** y **\[** [**version**](version.md) **\]** .

</dd> <dt>

*nombre de biblioteca* 
</dt> <dd>

Nombre por el que los componentes de software hacen referencia a la **biblioteca**.

</dd> <dt>

*Library-Definition-instrucciones* 
</dt> <dd>

Una o más instrucciones MIDL que definen el contenido de la **biblioteca**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las instrucciones dentro del bloque de biblioteca pueden utilizar elementos que se declaran dentro o fuera del bloque de biblioteca. Las instrucciones de biblioteca pueden utilizar esos elementos como tipos base, heredar de esos elementos o simplemente hacer referencia a ellos en una línea, como se indica a continuación:

``` syntax
interface MyFace 
{
    // Interface definition statements
};

[
    // library attributes
] 
library
{
    interface MyFace;

    // Other library definition statements.
};
```

El compilador MIDL creará una biblioteca de tipos que incluye las definiciones de todos los elementos dentro del bloque de biblioteca, así como las definiciones de los elementos definidos fuera y a los que se haga referencia desde dentro del bloque de biblioteca.

Para obtener información sobre la generación de una biblioteca de tipos y de código auxiliar y encabezados de proxy a partir de un único archivo IDL, vea [generar un archivo dll de proxy y una biblioteca de tipos desde un solo archivo IDL](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello 2.0 Type Library"), 
    lcid(0x0409), 
    version(2.0)
] 
library Hello 
{
    /* Library definition statements */
};
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Contenido de una biblioteca de tipos](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**control**](control.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpfile**](helpfile.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**plusvalía**](hidden.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Restrict**](restricted.md)
</dt> <dt>

[**Versión**](version.md)
</dt> </dl>

 

 