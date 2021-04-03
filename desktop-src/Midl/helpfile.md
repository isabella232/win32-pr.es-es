---
title: helpfile (atributo)
description: El atributo \ HelpFile \ establece el nombre del archivo de ayuda de una biblioteca de tipos. Todos los tipos de una biblioteca comparten el mismo archivo de ayuda.
ms.assetid: caa248b1-a1a7-4c36-886a-079a66a01907
keywords:
- atributo HelpFile (MIDL)
topic_type:
- apiref
api_name:
- helpfile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b4283b0285631a710af774d364a01b82c9d44b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790023"
---
# <a name="helpfile-attribute"></a>helpfile (atributo)

El atributo **\[ HelpFile \]** establece el nombre del archivo de ayuda de una biblioteca de tipos. Todos los tipos de una biblioteca comparten el mismo archivo de ayuda.

``` syntax
[
    uuid(uuid-number), 
    helpfile("filename") 
    [, optional-attribute-list]
] 
library 
{
    library statements
};
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*UUID-número* 
</dt> <dd>

Especifica un número de identificación único universal para la [**biblioteca**](library.md).

</dd> <dt>

*filename* 
</dt> <dd>

Especifica el nombre del archivo que contiene el texto de ayuda.

</dd> <dt>

*opcional-Attribute-List* 
</dt> <dd>

Especifica cero o más atributos que el compilador MIDL aplicará a la [**biblioteca**](library.md).

</dd> <dt>

*instrucciones de biblioteca* 
</dt> <dd>

Especifica una o más instrucciones MIDL que definen la interfaz de biblioteca.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use las funciones **GetDocumentation** en las interfaces **ITypeLib** y **ITypeInfo** para recuperar el nombre de archivo.

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpfile("filename.hlp"),
    lcid(0x0409), 
    version(2.0)
]
library Hello
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**biblioteca**](library.md)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 