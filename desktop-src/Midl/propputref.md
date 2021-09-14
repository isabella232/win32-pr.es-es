---
title: propputref (atributo)
description: El atributo \ propputref\ especifica una función de configuración de propiedades que usa una referencia en lugar de un valor.
ms.assetid: 84f1cd08-3c42-4a6d-bb1d-0bfd3f4c33f2
keywords:
- atributo propputref MIDL
topic_type:
- apiref
api_name:
- propputref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead5ccf7f9dc6a59580b7c3e3576f3c7503ccafc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159411"
---
# <a name="propputref-attribute"></a>propputref (atributo)

El **\[ atributo \] propputref** especifica una función de configuración de propiedades que usa una referencia en lugar de un valor.

``` syntax
[propputref [,optional-property-attributes]] return-type function-name( parameters);
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

Una función que tenga el **\[ atributo propputref \]** también debe tener, como último parámetro, un puntero que tenga el atributo **\[** [**in.**](in.md) **\]**

La propiedad debe tener el mismo nombre que la función . Como máximo, se puede especificar uno de los atributos **\[** [**propget**](propget.md), propput y **\]** **\[** [](propput.md) **\]** **\[ propputref \]** para una función.

### <a name="flags"></a>Marcas

INVOKE \_ PROPERTYPUTREF

## <a name="examples"></a>Ejemplos

``` syntax
interface InMyFace : IDispatch 
{
    [propget, 
     helpstring("A meaningful comment."), 
     id(1)] HRESULT Method2([out, retval] YourInterface** ReturnVal); 
    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**En**](in.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 