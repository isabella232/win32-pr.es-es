---
title: LCID (atributo)
description: El atributo \ LCID \ especifica un identificador de configuración regional y habilita la compatibilidad con el compilador MIDL específico de la configuración regional.
ms.assetid: 40457a1a-251c-41cd-bfa6-9d506601ff5e
keywords:
- LCID (atributo) MIDL
topic_type:
- apiref
api_name:
- lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa22b231c63583c6d16e6a50f3e9987c5b61128
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789970"
---
# <a name="lcid-attribute"></a>LCID (atributo)

El atributo **\[ LCID \]** especifica un identificador de configuración regional y habilita la compatibilidad con el compilador de MIDL específico de la configuración regional.

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

*UUID-número* 
</dt> <dd>

Especifica un número de identificación único universal para la [**biblioteca**](library.md).

</dd> <dt>

*LCID* 
</dt> <dd>

Especifica el identificador de configuración regional de 32 bits usado en la compatibilidad con el idioma nacional de Windows. Normalmente, el identificador de configuración regional se proporciona en formato hexadecimal.

</dd> <dt>

*opcional-Attribute-List* 
</dt> <dd>

Cero o más atributos que se van a aplicar a la [**biblioteca**](library.md).

</dd> <dt>

*nombre de biblioteca* 
</dt> <dd>

Nombre por el que los componentes de software hacen referencia a la [**biblioteca**](library.md).

</dd> <dt>

*Library-Definition-instrucciones* 
</dt> <dd>

Una o más instrucciones MIDL que definen el contenido de la [**biblioteca**](library.md).

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre de la función en el archivo IDL.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Cero o más atributos de MIDL que se aplicarán al parámetro de función.

</dd> <dt>

*nombre de parámetro* 
</dt> <dd>

Especifica el nombre del parámetro en el archivo IDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La sintaxis de **\[ \] LCID** tiene dos formas diferentes; el efecto del atributo depende de la sintaxis que se utilice, ya sea de la sintaxis de la instrucción de la [**biblioteca**](library.md) o de la sintaxis del parámetro.

Cuando se aplica a la instrucción [**Library**](library.md) , junto con un argumento localeID, como se muestra en el primer ejemplo, el atributo **\[ LCID \]** identifica la configuración regional de una biblioteca de tipos o de un argumento de función y permite usar caracteres internacionales dentro del bloque de biblioteca.

A partir de la versión 3.01.75 del compilador de MIDL, el identificador de configuración regional proporcionado por este atributo no solo decora la biblioteca de tipos resultante, sino que realmente cambia el comportamiento del compilador. Dentro de una instrucción de [**biblioteca**](library.md) , desde el punto donde se usa el atributo **\[ LCID \]** , MIDL aceptará la entrada localizada según la configuración regional especificada. En concreto, hay disponible compatibilidad total con idiomas asiáticos como japonés, Chino y Coreano (compatibilidad completa con DBCS). Las características admitidas por la localización son: comentarios, cadenas, helpstrings e identificadores.

Utilice el modificador de compilador [**/LCID**](-lcid.md) para que esta compatibilidad de localización esté disponible en todo el archivo de entrada, incluidos el nombre de archivo y la ruta de acceso del directorio, en lugar de simplemente dentro del bloque de biblioteca.

Cuando se aplica a un parámetro, el atributo **\[ LCID \]** permite pasar un identificador de configuración regional a una función, tal y como se muestra en el segundo ejemplo. Las restricciones siguientes se aplican a los parámetros de **\[ LCID \]** :

-   Una función puede tener como máximo un parámetro **\[ LCID \]** .
-   El tipo de datos del parámetro debe ser [**largo**](long.md).
-   La dirección del parámetro debe ser solo **\[** [**en**](in.md) **\]** .
-   El parámetro **\[ LCID \]** debe seguir a cualquier otro parámetro, excepto un **\[** parámetro [**retval**](retval.md) **\]** .
-   No se puede aplicar el atributo **\[ LCID \]** a un parámetro [**dispinterface**](dispinterface.md) o [**CoClass**](coclass.md) .

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

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**/LCID**](-lcid.md)
</dt> <dt>

[**biblioteca**](library.md)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 