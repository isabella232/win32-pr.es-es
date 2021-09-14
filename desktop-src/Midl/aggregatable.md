---
title: aggregatable (atributo)
description: El atributo \ aggregationable\ indica que la clase admite la agregación.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159692"
---
# <a name="aggregatable-attribute"></a>aggregatable (atributo)

El **\[ atributo \] agregable** indica que la clase admite la agregación.

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

*coclass-attribute-list* 
</dt> <dd>

Otros atributos que se aplican a la clase .

</dd> <dt>

*coclass-name* 
</dt> <dd>

Nombre de la clase.

</dd> <dt>

*coclass-interface-list* 
</dt> <dd>

Lista de interfaces para la clase .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use el **\[ atributo agregable \]** en una instrucción [**coclass**](coclass.md) para que los usuarios sepan que la clase admite agregaciones. Es decir, la clase permite que una clase contenedora exponga sus interfaces como si fueran interfaces propias del contenedor.

La representación de la marca de tipo para este atributo es TYPEFLAG \_ CONFIGURABLEGREGATABLE.

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

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 