---
title: propget (atributo)
description: El atributo \ propget \ especifica una función de descriptor de acceso de propiedad. La propiedad debe tener el mismo nombre que la función.
ms.assetid: 0b76ece3-e19b-4c80-883c-ff414bc2e435
keywords:
- propget (atributo) MIDL
topic_type:
- apiref
api_name:
- propget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6337409e021670c282400d38b97543687fa81c2a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077596"
---
# <a name="propget-attribute"></a>propget (atributo)

El atributo **\[ propget \]** especifica una función de descriptor de acceso de propiedad. La propiedad debe tener el mismo nombre que la función.

``` syntax
[propget [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Optional-Property-Attributes* 
</dt> <dd>

Cero o más atributos de propiedad.

</dd> <dt>

*tipo de valor devuelto* 
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

Una función que tiene el atributo propget también debe tener, como su último parámetro, un tipo de puntero con los **\[** atributos [**out**](out-idl.md) **\]** y **\[** [**retval**](retval.md) **\]** . Si el último parámetro no tiene los \[ atributos out, retval \] , el valor devuelto de la función se trata como un \[ parámetro out, retval \] . Por ejemplo, una función con el prototipo

``` syntax
[propget] short MyFunction([in] long aLongValue);
```

se trata como

``` syntax
[propget] HRESULT MyFunction([in] long aLongValue, [out,retval] short *outValue);
```

Como máximo, se puede especificar una de **\[ propget \]**, **\[** [**PROPPUT**](propput.md) **\]** y **\[** [**PROPPUTREF**](propputref.md) **\]** para una función.

Si el **\[** atributo [**LCID**](lcid.md) **\]** se utiliza en la lista de parámetros de una función que contiene un parámetro con el **\[** atributo [**PROPPUT**](propput.md) **\]** , el parámetro **\[ LCID \]** debe ser el segundo en el último.

### <a name="flags"></a>Marcas

INVOCAr \_ PropertyGet (

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

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**enuncia**](out-idl.md)
</dt> <dt>

[**retval**](retval.md)
</dt> <dt>

[**PROPPUT**](propput.md)
</dt> <dt>

[**PROPPUTREF**](propputref.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 