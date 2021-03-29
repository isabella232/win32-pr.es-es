---
title: aggregatable (atributo)
description: El atributo \ aggregateable \ indica que la clase admite la agregación.
ms.assetid: 3b680692-fbf7-4aeb-b11a-c3a87ddaea67
keywords:
- atributo agregable MIDL
topic_type:
- apiref
api_name:
- aggregatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5091815cf38060c30b82aa33fd05ad6be9d6c390
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358876"
---
# <a name="aggregatable-attribute"></a>aggregatable (atributo)

El atributo **\[ agregable \]** indica que la clase admite la agregación.

``` syntax
[
   coclass-attribute-list,
   aggregatable
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

Utilice el atributo **\[ agregable \]** en una instrucción de [**coclase**](coclass.md) para permitir que los usuarios sepan que la clase admite agregaciones. Es decir, la clase permite que una clase contenedora exponga sus interfaces como si fueran las interfaces propias del contenedor.

La representación typeflag para este atributo es TYPEFLAG \_ FAGGREGATABLE.

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    aggregatable
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**coclase**](coclass.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 