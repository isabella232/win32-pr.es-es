---
title: propputref (atributo)
description: El atributo \ PROPPUTREF \ especifica una función de configuración de propiedades que usa una referencia en lugar de un valor.
ms.assetid: 84f1cd08-3c42-4a6d-bb1d-0bfd3f4c33f2
keywords:
- atributo PROPPUTREF MIDL
topic_type:
- apiref
api_name:
- propputref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead5ccf7f9dc6a59580b7c3e3576f3c7503ccafc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995131"
---
# <a name="propputref-attribute"></a>propputref (atributo)

El atributo **\[ PROPPUTREF \]** especifica una función de configuración de propiedades que usa una referencia en lugar de un valor.

``` syntax
[propputref [,optional-property-attributes]] return-type function-name( parameters);
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

Una función que tenga el atributo **\[ PROPPUTREF \]** también debe tener, como el último parámetro, un puntero con el atributo **\[** [**in**](in.md) **\]** .

La propiedad debe tener el mismo nombre que la función. Como máximo, **\[** [](propget.md) **\]** **\[** [](propput.md) **\]** se puede especificar uno de los atributos propget, PROPPUT y **\[ PROPPUTREF \]** para una función.

### <a name="flags"></a>Marcas

INVOCAr \_ PROPERTYPUTREF

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

[**de**](in.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**PROPPUT**](propput.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 