---
title: nonbrowsable (atributo)
description: Use el atributo \ nonbrowsable\ para etiquetar una interfaz o un miembro dispinterface que no debe mostrarse en un explorador de propiedades.
ms.assetid: 94e868cc-8d9c-4b8a-ac18-1ea513a103da
keywords:
- MIDL de atributo que no se puede ver
topic_type:
- apiref
api_name:
- nonbrowsable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e24c39511df9637c352245b98b237fe8fd451eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159448"
---
# <a name="nonbrowsable-attribute"></a>nonbrowsable (atributo)

Use el **\[ atributo no \] utilizable para** etiquetar una interfaz o un miembro dispinterface que no debe mostrarse en un explorador de propiedades.

``` syntax
[property-attribute-list, nonbrowsable]return-type property-name(prop-param-list)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*property-attribute-list* 
</dt> <dd>

Otros atributos que se aplican a la propiedad .

</dd> <dt>

*return-type* 
</dt> <dd>

Tipo de los datos devueltos por el método .

</dd> <dt>

*property-name* 
</dt> <dd>

Nombre de la propiedad o el método.

</dd> <dt>

*prop-param-list* 
</dt> <dd>

Cero o más parámetros que se pasarán al método .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Algunas propiedades no deben mostrarse en un explorador de propiedades. Esto puede deberse a que recuperar el valor tardaría mucho tiempo. El ejemplo evita que el usuario intente recuperar la *propiedad Count,* que devuelve el número de filas del conjunto dinámico. Este número puede representar los resultados de una consulta muy grande.

Otras propiedades pueden tener efectos inesperados en el explorador. Por ejemplo, considere un control con la propiedad "IsSelected" para saber si el control está seleccionado. Si "IsSelected" se establece en false, un explorador de propiedades basado en selección examinará un objeto diferente.

Tenga en cuenta que una propiedad etiquetada como **\[ no \]** utilizable seguirá apareciendo en un explorador de objetos, que no muestra los valores de propiedad.

### <a name="typeflag-representation"></a>Representación de tipoflag

Presencia de FUNCFLAG \_ FNONBROWSABLE o VARFLAG \_ FNONBROWSABLE.

## <a name="examples"></a>Ejemplos

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IDynaset:IDispatch
{
    [propget, nonbrowsable]HRESULT Count([out, retval] long *Value);
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 