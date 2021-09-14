---
title: immediatebind (atributo)
description: El atributo \ immediatebind\ indica que se notificará inmediatamente a la base de datos todos los cambios realizados en una propiedad de un objeto enlazado a datos.
ms.assetid: 1c08ddca-e273-43b3-a8f6-ed7f552e4e0e
keywords:
- atributo immediatebind MIDL
topic_type:
- apiref
api_name:
- immediatebind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8a797514c15f8d4c46bb6161946d5d0b6bd10b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159547"
---
# <a name="immediatebind-attribute"></a>immediatebind (atributo)

El **\[ atributo \] immediatebind** indica que se notificará inmediatamente a la base de datos todos los cambios en una propiedad de un objeto enlazado a datos.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, immediatebind[, optional-attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Especifica una lista de uno o varios atributos que se aplican a la interfaz en su conjunto.

</dd> <dt>

*interface-name* 
</dt> <dd>

Especifica el nombre de la [**interfaz o**](interface.md) [**dispinterface**](dispinterface.md).

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Cero o más atributos de función.

</dd> <dt>

*returntype* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre de la función en el archivo IDL.

</dd> <dt>

*params* 
</dt> <dd>

Cero o más parámetros de función.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ atributo \] immediatebind** permite a los controles diferenciar entre las propiedades que necesitan notificar a la base de datos cada cambio y las que no. Por ejemplo, cada cambio en un control de casilla se debe enviar inmediatamente a la base de datos subyacente, incluso si el control no ha perdido el foco. Sin embargo, para un control de cuadro de lista, se produce un cambio cada vez que se resalta una selección diferente. Notificar a la base de datos un cambio antes de que el control pierda el foco sería ineficaz e innecesario. El **\[ atributo \] immediatebind** permite especificar, estableciendo el bit ImmediateBind, propiedades individuales en un formulario cuyos cambios se deben indicar inmediatamente.

Las propiedades que tienen **\[ el atributo immediatebind \]** también deben tener el atributo **\[** [**enlazable.**](bindable.md) **\]**

### <a name="flags"></a>Marcas

FUNCFLAG \_ FIMMEDIATEBIND, VARFLAG \_ FIMMEDIATEBIND

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, immediatebind] long Size(void);

        [id(1), propput, bindable, 
         immediatebind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Interfaz**](interface.md)
</dt> <dt>

[**Dispinterface**](dispinterface.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 