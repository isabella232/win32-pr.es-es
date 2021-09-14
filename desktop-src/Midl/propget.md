---
title: propget (atributo)
description: El atributo \ propget\ especifica una función de accessor de propiedad. La propiedad debe tener el mismo nombre que la función .
ms.assetid: 0b76ece3-e19b-4c80-883c-ff414bc2e435
keywords:
- atributo propget MIDL
topic_type:
- apiref
api_name:
- propget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6337409e021670c282400d38b97543687fa81c2a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159414"
---
# <a name="propget-attribute"></a>propget (atributo)

El **\[ atributo \] propget** especifica una función de accessor de propiedad. La propiedad debe tener el mismo nombre que la función .

``` syntax
[propget [,optional-property-attributes]] return-type function-name( parameters);
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

*function-name* 
</dt> <dd>

Nombre del procedimiento remoto.

</dd> <dt>

*parameters* 
</dt> <dd>

Cero o más parámetros para el procedimiento remoto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una función que tenga el atributo propget también debe tener, como último parámetro, un tipo de puntero con los atributos **\[** [**out**](out-idl.md) **\]** y **\[** [**retval.**](retval.md) **\]** Si el último parámetro no tiene los atributos out, retval, el valor devuelto de la función se trata como \[ \] un parámetro \[ out, retval. \] Por ejemplo, una función con el prototipo

``` syntax
[propget] short MyFunction([in] long aLongValue);
```

se trata como

``` syntax
[propget] HRESULT MyFunction([in] long aLongValue, [out,retval] short *outValue);
```

Como máximo, se puede especificar **\[ uno de \] propget,** **\[** [**propput**](propput.md)y **\]** **\[** [**propputref**](propputref.md) para una **\]** función.

Si el atributo lcid se usa en la lista de parámetros de una función que contiene un parámetro con el atributo **\[** [](lcid.md) **\]** **\[** [**propput,**](propput.md) el parámetro **\]** **\[ lcid \]** debe ser de segundo a último.

### <a name="flags"></a>Marcas

INVOKE \_ PROPERTYGET

## <a name="examples"></a>Ejemplos

``` syntax
interface MyInterface : IDispatch                         
{                
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
        
    [propget, 
     helpstring("A meaningful comment."), id(1)] HRESULT Method2(
         [out, retval] YourInterface** ReturnVal); 

    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}                 
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Retval**](retval.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 