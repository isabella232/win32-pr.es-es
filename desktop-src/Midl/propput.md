---
title: propput (atributo)
description: El atributo \ PROPPUT \ especifica una función de configuración de propiedades. La propiedad debe tener el mismo nombre que la función.
ms.assetid: ffd8af15-42a4-4852-a29b-1fc66f673978
keywords:
- atributo de PROPPUT (MIDL)
topic_type:
- apiref
api_name:
- propput
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79bf5520a3f4f4872801145064f49a8108cf602a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149204"
---
# <a name="propput-attribute"></a>propput (atributo)

El atributo **\[ PROPPUT \]** especifica una función de configuración de propiedades. La propiedad debe tener el mismo nombre que la función *.*

``` syntax
[propput [,optional-property-attributes]] return-type function-name( parameters);
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

Una función que tiene el atributo **\[ PROPPUT \]** también debe tener, como su último parámetro, un parámetro que tiene el **\[** atributo [**in**](in.md) **\]** .

Como máximo, **\[** [](propget.md) **\]** se puede especificar una de propget, **\[ PROPPUT \]** y **\[** [**PROPPUTREF**](propputref.md) **\]** para una función.

Si el **\[** atributo [**LCID**](lcid.md) **\]** se utiliza en la lista de parámetros de una función que contiene un parámetro con el atributo **\[ PROPPUT \]** , el parámetro **\[ LCID \]** debe ser el segundo en el último.

### <a name="flags"></a>Marcas

INVOCAr \_ PROPERTYPUT

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

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**PROPPUTREF**](propputref.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 