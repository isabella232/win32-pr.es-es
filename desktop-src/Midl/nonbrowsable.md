---
title: nonbrowsable (atributo)
description: Utilice el atributo \ nonbrowsableable \ para etiquetar un miembro de interfaz o dispinterface que no se debe mostrar en un explorador de propiedades.
ms.assetid: 94e868cc-8d9c-4b8a-ac18-1ea513a103da
keywords:
- MIDL de atributo no explorable
topic_type:
- apiref
api_name:
- nonbrowsable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e24c39511df9637c352245b98b237fe8fd451eb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995153"
---
# <a name="nonbrowsable-attribute"></a>nonbrowsable (atributo)

Use el atributo **\[ nonbrowsable \]** para etiquetar un miembro de interfaz o dispinterface que no se debe mostrar en un explorador de propiedades.

``` syntax
[property-attribute-list, nonbrowsable]return-type property-name(prop-param-list)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Property-Attribute-List* 
</dt> <dd>

Otros atributos que se aplican a la propiedad.

</dd> <dt>

*tipo de valor devuelto* 
</dt> <dd>

Tipo de los datos devueltos por el método.

</dd> <dt>

*nombre de propiedad* 
</dt> <dd>

Nombre de la propiedad o del método.

</dd> <dt>

*prop-param-List* 
</dt> <dd>

Cero o más parámetros que se van a pasar al método.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Algunas propiedades no deben mostrarse en un explorador de propiedades. Esto puede deberse a que la recuperación del valor tardaría mucho tiempo. En el ejemplo se impide que el usuario intente recuperar la propiedad *Count* , que devuelve el número de filas del conjunto de registros dinámico. Este número puede representar los resultados de una consulta muy grande.

Otras propiedades pueden tener efectos inesperados en el explorador. Por ejemplo, considere un control con la propiedad "IsSelected" para saber si el control está seleccionado. Si "IsSelected" está establecido en false, un explorador de propiedades basado en la selección examinará un objeto diferente.

Tenga en cuenta que una propiedad etiquetada como **\[ nonbrowsable \]** seguirá apareciendo en un examinador de objetos, que no muestra los valores de propiedad.

### <a name="typeflag-representation"></a>Representación Typeflag

La presencia de FUNCFLAG \_ FNONBROWSABLE o VARFLAG \_ FNONBROWSABLE.

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

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 