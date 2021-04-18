---
title: noncreatable (atributo)
description: El atributo \ noncreatable \ define un objeto del que no se pueden crear instancias de sí mismo.
ms.assetid: 75d7b978-0f82-4e8a-89c2-ffd5b9a691d6
keywords:
- MIDL de atributo no creatable
topic_type:
- apiref
api_name:
- noncreatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2aa54be3416087c06651a4bb58902a0469e8f0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358865"
---
# <a name="noncreatable-attribute"></a>noncreatable (atributo)

El atributo **\[ noncreatable \]** define un objeto del que no se pueden crear instancias de sí mismo.

``` syntax
[
  coclass-attribute-list, 
    noncreatable
]
coclass coclass-name
{
  coclass-interface-list
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*coclass-Attribute-List* 
</dt> <dd>

Otros atributos que se aplican a la clase.

</dd> <dt>

*nombre de coclase* 
</dt> <dd>

Nombre de la clase.

</dd> <dt>

*coclass-interface-List* 
</dt> <dd>

Una lista de interfaces para la clase.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use el atributo **\[ noncreatable \]** en una instrucción de [**coclase**](coclass.md) para indicar a los usuarios que no pueden crear un nuevo objeto de esta clase en el nivel superior, es decir, mediante una llamada a **CreateInstance** o **CoCreateInstance**. La creación de instancias de un objeto de esta clase requiere una llamada de método a otro objeto. Por ejemplo, en Microsoft Excel, el objeto "Cell" no se puede crear y se debe obtener de un objeto de hoja de cálculo de Microsoft Excel.

Los métodos que devuelven instancias de clases que no se pueden crear deben devolver el tipo exacto del objeto, en lugar de los tipos **Variant** o **IDispatch** \* .

### <a name="typeflag-representation"></a>Representación de Typeflag:

Ausencia de TYPEFLAG \_ FCANCREATE.

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is MyCOClass"),
    noncreatable
]
coclass MyCoClass
{
    [default] interface IMyClass;
    [default, source] dispinterface IMyClassEvents;
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**coclase**](coclass.md)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 