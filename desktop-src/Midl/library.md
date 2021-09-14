---
title: atributo library
description: La instrucción library contiene toda la información que el compilador MIDL usa para generar una biblioteca de tipos.
ms.assetid: d73acb17-abe4-4c31-a264-a131d1f9fa51
keywords:
- atributo de biblioteca MIDL
topic_type:
- apiref
api_name:
- library
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100c901c6b5d86ed3420d51e459627bdb5b461b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159512"
---
# <a name="library-attribute"></a>atributo library

La **instrucción** library contiene toda la información que el compilador MIDL usa para generar una biblioteca de tipos.

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

*uuid-number* 
</dt> <dd>

Especifica un número de identificación único universal para la biblioteca.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Especifica atributos adicionales que se aplican a toda la instrucción **de biblioteca.** Entre los atributos permitidos se **\[** [**incluyen control**](control.md) **\]** , **\[** [**helpcontext**](helpcontext.md), **\]** **\[** [**helpfile**](helpfile.md), **\]** **\[** [**helpstring**](helpstring.md), **\]** **\[** [**hidden**](hidden.md) **\]** , **\[** [**lcid,**](lcid.md) **\]** **\[** [**restricted**](restricted.md)y **\]** **\[** [**version**](version.md) **\]** .

</dd> <dt>

*library-name* 
</dt> <dd>

Nombre por el que los componentes de software hacen referencia a la **biblioteca**.

</dd> <dt>

*library-definition-statements* 
</dt> <dd>

Una o varias instrucciones MIDL que definen el contenido de la **biblioteca**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las instrucciones dentro del bloque de biblioteca pueden usar elementos que se declaran dentro o fuera del bloque de biblioteca. Las instrucciones library pueden usar esos elementos como tipos base, heredar de esos elementos o simplemente hacer referencia a ellos en una línea, como se muestra a continuación:

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

El compilador MIDL creará una biblioteca de tipos que incluye definiciones para cada elemento dentro del bloque de biblioteca, además de definiciones para los elementos definidos fuera y a los que se hace referencia desde dentro del bloque de biblioteca.

Para obtener información sobre cómo generar una biblioteca de tipos y códigos auxiliares de proxy y encabezados a partir de un único archivo IDL, vea Generar un archivo DLL de proxy y una biblioteca de tipos a partir de un [único archivo IDL.](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md)

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

[**Control**](control.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpfile**](helpfile.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**Oculto**](hidden.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Restringido**](restricted.md)
</dt> <dt>

[**version**](version.md)
</dt> </dl>

 

 