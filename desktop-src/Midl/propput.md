---
title: propput (atributo)
description: El atributo \ propput\ especifica una función de configuración de propiedades. La propiedad debe tener el mismo nombre que la función.
ms.assetid: ffd8af15-42a4-4852-a29b-1fc66f673978
keywords:
- atributo propput MIDL
topic_type:
- apiref
api_name:
- propput
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f0e34d4826abfa2df6cd1262ccd4bcec04344f4500ddf5c146816d23f6261c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641938"
---
# <a name="propput-attribute"></a>propput (atributo)

El **\[ atributo \] propput** especifica una función de configuración de propiedades. La propiedad debe tener el mismo nombre que la función *.*

``` syntax
[propput [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*optional-property-attributes* 
</dt> <dd>

Cero o más atributos de propiedad.

</dd> <dt>

*return-type* 
</dt> <dd>

Tipo de los datos devueltos por el procedimiento remoto.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Nombre del procedimiento remoto.

</dd> <dt>

*parameters* 
</dt> <dd>

Cero o más parámetros para el procedimiento remoto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una función que tenga el **\[ atributo propput \]** también debe tener, como último parámetro, un parámetro que tenga el atributo **\[** [**in.**](in.md) **\]**

Como máximo, se puede especificar **\[** [**uno de propget**](propget.md), **\]** **\[ propput \]** y **\[** [**propputref**](propputref.md) para una **\]** función.

Si el atributo lcid se usa en la lista de parámetros de una función que contiene un parámetro con el atributo **\[** [](lcid.md) **\]** **\[ propput, \]** el **\[ parámetro lcid \]** debe ser el segundo al último.

### <a name="flags"></a>Marcas

INVOKE \_ PROPERTYPUT

## <a name="examples"></a>Ejemplos

``` syntax
interface InMyFace : IDispatch                         
{
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Diferencias entre MIDL y MKTYPLIB](differences-between-midl-and-mktyplib.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 