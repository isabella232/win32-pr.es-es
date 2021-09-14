---
title: helpfile (atributo)
description: El atributo \ helpfile\ establece el nombre del archivo de Ayuda para una biblioteca de tipos. Todos los tipos de una biblioteca comparten el mismo archivo de Ayuda.
ms.assetid: caa248b1-a1a7-4c36-886a-079a66a01907
keywords:
- atributo helpfile MIDL
topic_type:
- apiref
api_name:
- helpfile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b4283b0285631a710af774d364a01b82c9d44b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159566"
---
# <a name="helpfile-attribute"></a>helpfile (atributo)

El **\[ atributo \] helpfile** establece el nombre del archivo de Ayuda para una biblioteca de tipos. Todos los tipos de una biblioteca comparten el mismo archivo de Ayuda.

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

*uuid-number* 
</dt> <dd>

Especifica un número de identificación único universal para la [**biblioteca**](library.md).

</dd> <dt>

*filename* 
</dt> <dd>

Especifica el nombre del archivo que contiene el texto de ayuda.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Especifica cero o más atributos que el compilador MIDL aplicará a la [**biblioteca**](library.md).

</dd> <dt>

*instrucciones library* 
</dt> <dd>

Especifica una o varias instrucciones MIDL que definen la interfaz de biblioteca.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use las **funciones GetDocumentation** en las interfaces **ITypeLib** **e ITypeInfo** para recuperar el nombre de archivo.

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

[**Biblioteca**](library.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 