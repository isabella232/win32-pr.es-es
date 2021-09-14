---
title: restricted (atributo)
description: El atributo \ restricted\ especifica que no se puede llamar arbitrariamente a una biblioteca o miembro de un módulo, interfaz o dispinterface.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159393"
---
# <a name="restricted-attribute"></a>restricted (atributo)

El **\[ atributo \] restringido** especifica que no se puede llamar arbitrariamente a una biblioteca o miembro de un módulo, interfaz o dispinterface.

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

*otros atributos* 
</dt> <dd>

Cero o más atributos MIDL.

</dd> <dt>

*statement-type* 
</dt> <dd>

Uno de los siguientes: [**library**](library.md), [**module**](module.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md).

</dd> <dt>

*statement-name* 
</dt> <dd>

Identificador por el que el software hace referencia a esta instrucción.

</dd> <dt>

*Definiciones* 
</dt> <dd>

Elementos de lenguaje MIDL que definen el contenido de esta instrucción.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este atributo permite controlar el acceso a elementos de interfaces, bibliotecas, módulos e interfaces dispinterface. Por ejemplo, puede impedir que un programador de macros utilice un elemento de datos. Puede aplicar este atributo a un miembro de una [**coclase**](coclass.md), independientemente de si el miembro es una interfaz o interfaz dispinterface e independientemente de si el miembro es un receptor (entrante) o de origen (saliente). Un miembro de una **coclase** no puede tener los atributos **\[ \] restringidos** **\[ y predeterminados. \]**

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

[**Biblioteca**](library.md)
</dt> <dt>

[**Interfaz**](interface.md)
</dt> <dt>

[**Dispinterface**](dispinterface.md)
</dt> <dt>

[**Módulo**](module.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 