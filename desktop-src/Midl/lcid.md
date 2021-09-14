---
title: Atributo lcid
description: El atributo \ lcid\ especifica un identificador de configuración regional y habilita la compatibilidad del compilador MIDL específica de la configuración regional.
ms.assetid: 40457a1a-251c-41cd-bfa6-9d506601ff5e
keywords:
- atributo lcid MIDL
topic_type:
- apiref
api_name:
- lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa22b231c63583c6d16e6a50f3e9987c5b61128
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159517"
---
# <a name="lcid-attribute"></a>Atributo lcid

El **\[ atributo \] lcid** especifica un identificador de configuración regional y habilita la compatibilidad del compilador MIDL específica de la configuración regional.

``` syntax
[
    uuid(uuid-number), 
    lcid(localeID)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}

function-name([parameter-attribute-list, lcid] long  parameter-name,. . .);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*uuid-number* 
</dt> <dd>

Especifica un número de identificación único universal para la [**biblioteca**](library.md).

</dd> <dt>

*localeID* 
</dt> <dd>

Especifica el identificador de configuración regional de 32 bits que se usa Windows compatibilidad con idiomas nacionales. Normalmente, el identificador de configuración regional se indica en hexadecimal.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Cero o más atributos que se aplicarán a la [**biblioteca**](library.md).

</dd> <dt>

*library-name* 
</dt> <dd>

Nombre por el que los componentes de software hacen referencia a la [**biblioteca**](library.md).

</dd> <dt>

*library-definition-statements* 
</dt> <dd>

Una o varias instrucciones MIDL que definen el contenido de la [**biblioteca**](library.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre de la función en el archivo IDL.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Cero o más atributos MIDL que se aplicarán al parámetro de función.

</dd> <dt>

*parameter-name* 
</dt> <dd>

Especifica el nombre del parámetro en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **\[ sintaxis lcid \]** tiene dos formas diferentes; el efecto del [](library.md) atributo depende de la sintaxis que use: la sintaxis de la instrucción de biblioteca o la sintaxis de parámetros.

Cuando se aplica a la instrucción [**library,**](library.md) junto con un argumento localeID, como se muestra en el primer ejemplo, el atributo **\[ lcid \]** identifica la configuración regional de una biblioteca de tipos o de un argumento de función y permite usar caracteres internacionales dentro del bloque de biblioteca.

A partir de la versión 3.01.75 del compilador MIDL, el identificador de configuración regional proporcionado por este atributo no solo decora la biblioteca de tipos resultante, sino que cambia realmente el comportamiento del compilador. Dentro de [**una instrucción**](library.md) de biblioteca, desde el punto donde se usa el atributo **\[ lcid, \]** MIDL aceptará la entrada localizada según la configuración regional especificada. En concreto, hay disponible compatibilidad completa con idiomas asiáticos como japonés, chino y coreano (compatibilidad completa con DBCS). Las características admitidas por la localización son: comentarios, cadenas, cadenas de ayuda e identificadores.

Use el [**modificador del compilador /lcid**](-lcid.md) para que esta compatibilidad de localización esté disponible para todo el archivo de entrada, incluidos el nombre de archivo y la ruta de acceso del directorio, en lugar de solo dentro del bloque de biblioteca.

Cuando se aplica a un parámetro, el **\[ atributo lcid \]** permite pasar un identificador de configuración regional a una función, como se muestra en el segundo ejemplo. Las restricciones siguientes se aplican a **\[ los parámetros lcid: \]**

-   Una función puede tener como máximo un **\[ parámetro lcid. \]**
-   El tipo de datos del parámetro debe ser [**long.**](long.md)
-   La dirección del parámetro solo debe **\[** [**estar en**](in.md) **\]** .
-   El **\[ parámetro \] lcid** debe seguir cualquier otro parámetro, excepto un **\[** [**parámetro retval.**](retval.md) **\]**
-   No se puede aplicar **\[ el atributo lcid \]** a un parámetro [**dispinterface**](dispinterface.md) [**o coclass.**](coclass.md)

## <a name="examples"></a>Ejemplos

``` syntax
[  
    uuid(12345678-1234-1234-1234-123456789ABC),
    lcid(0x09),
    version(1.0)
] 
library MyLibrary
{
    /* Library definition statements */
};

interface IMyFace : IDispatch
{
    [propget] HRESULT MyFunc([in, lcid] long LocaleID,
                          [out, retval] BSTR * ReturnVal);
    // Other interface definition statements
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**coclase**](coclass.md)
</dt> <dt>

[**Dispinterface**](dispinterface.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**/lcid**](-lcid.md)
</dt> <dt>

[**Biblioteca**](library.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**Retval**](retval.md)
</dt> </dl>

 

 