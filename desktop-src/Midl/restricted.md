---
title: restricted (atributo)
description: El atributo \ Restricted \ especifica que una biblioteca, o un miembro de un módulo, una interfaz o una dispinterface, no se puede llamar arbitrariamente.
ms.assetid: ad1ae84f-77f4-4028-bd71-ff01414e474e
keywords:
- MIDL de atributo restringido
topic_type:
- apiref
api_name:
- restricted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca610c0dcf29ebc3a767005b4c22e3231947e88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420647"
---
# <a name="restricted-attribute"></a>restricted (atributo)

El atributo **\[ Restricted \]** especifica que una biblioteca, o miembro de un módulo, una interfaz o una dispinterface, no se puede llamar arbitrariamente.

``` syntax
[
    restricted
    [, other-attributes]
] 
statement-type statement-name 
{
    definitions
};
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*otros: atributos* 
</dt> <dd>

Cero o más atributos de MIDL.

</dd> <dt>

*tipo de instrucción* 
</dt> <dd>

Uno de los siguientes: [**Library**](library.md), [**Module**](module.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md).

</dd> <dt>

*nombre de instrucción* 
</dt> <dd>

Identificador por el que el software hace referencia a esta instrucción.

</dd> <dt>

*Figura* 
</dt> <dd>

Elementos del lenguaje MIDL que definen el contenido de esta instrucción.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este atributo permite controlar el acceso a los elementos de interfaces, bibliotecas, módulos e interfaces dispinterface. Por ejemplo, puede impedir que un elemento de datos sea utilizado por un programador de macros. Puede aplicar este atributo a un miembro de una [**coclase**](coclass.md), independientemente de si el miembro es una interfaz dispinterface o una interfaz, e independientemente de si el miembro es un receptor (entrante) o de origen (saliente). Un miembro de una **coclase** no puede tener los atributos **\[ restringidos \]** y **\[ predeterminados \]** .

### <a name="flags"></a>Marcas

IMPLTYPEFLAG \_ FRESTRICTED, FUNCFLAG \_ FRESTRICTED

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version (1.0), 
    restricted
] 
library MyLibrary
{
    // Library definition statements.
};

[propget, restricted] HRESULT MyProc(void);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**biblioteca**](library.md)
</dt> <dt>

[**interfaz**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**destina**](module.md)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 