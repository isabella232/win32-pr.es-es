---
title: defaultvtable (atributo)
description: El atributo \ defaultvtable\ define una interfaz como la interfaz de Vtable predeterminada.
ms.assetid: 05e50935-c630-4f9e-a7ec-3bb70a9834f1
keywords:
- atributo defaultvtable MIDL
topic_type:
- apiref
api_name:
- defaultvtable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffebc5907072f7fdfc539bbc2b06bf1e4ad9fb667826c6c3c5a96121b106326e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067345"
---
# <a name="defaultvtable-attribute"></a>defaultvtable (atributo)

El **\[ atributo \] defaultvtable** define una interfaz como la interfaz Vtable predeterminada.

``` syntax
[
    coclass-attribute-list, 
    defaultvtable
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

Otros atributos que se aplican a la clase . Los **\[** [**atributos source**](source.md) **\]** y **\[** [**uuid**](uuid.md) son **\]** obligatorios.

</dd> <dt>

*coclass-name* 
</dt> <dd>

Nombre de la clase.

</dd> <dt>

*coclass-interface-list* 
</dt> <dd>

Lista de interfaces para la clase .

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una interfaz de Vtable predeterminada no puede ser una interfaz dispinterface, debe ser una interfaz o una interfaz dual o de Vtable. Si la interfaz es una interfaz dual, los receptores pueden suponer que recibirán eventos a través de Vtable.

Una clase puede ser una interfaz de origen predeterminada y una interfaz de origen de Vtable predeterminada, como se muestra en el ejemplo. En este caso, un receptor de notificaciones debe usar IID IDISPATCH para recibir eventos de distribución y usar el identificador de interfaz \_ para recibir eventos de Vtable.

### <a name="typeflag-representation"></a>Representación typeflag

Presencia de IMPLTYPEFLAG \_ FDEFAULTVTABLE.

## <a name="examples"></a>Ejemplos

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget] HRESULT Backcolor([out, retval] long *Value);
    [propput] HRESULT Backcolor([in] long Value);
    [propget] HRESULT Name([out, retval] BSTR *Value);
    [propput] HRESULT Name([in] BSTR Value);}

[
    dual,
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    restricted
]
interface IFormEvents: IDispatch
{
    HRESULT Click();
    HRESULT Resize();}

    [
        uuid(1e123456-1f3c-1069-996b-123456789ABC)
    ]
    coclass Form
    {
        [default] interface IForm;
        [default, defaultvtable, source] interface IFormEvents;
    }
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**coclase**](coclass.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Fuente**](source.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> </dl>

 

 