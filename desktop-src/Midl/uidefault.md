---
title: uidefault (atributo)
description: El atributo \ uidefault\ indica que el miembro de información de tipo es el miembro predeterminado para mostrar en la interfaz de usuario.
ms.assetid: e789be38-a509-437d-89c9-ebbc830e5ae2
keywords:
- atributo uidefault MIDL
topic_type:
- apiref
api_name:
- uidefault
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 891d37611eb931a8857157434419e5221e808710290f2e209f50c743bcb5b7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013483"
---
# <a name="uidefault-attribute"></a>uidefault (atributo)

El **\[ atributo \] uidefault** indica que el miembro de información de tipo es el miembro predeterminado para mostrar en la interfaz de usuario.

``` syntax
[method-attribute-list, uidefault]return-type method-name(method-parameter-list)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*method-attribute-list* 
</dt> <dd>

Otros atributos que se aplican al método .

</dd> <dt>

*return-type* 
</dt> <dd>

Tipo de los datos que devolverá el método cuando finalice la ejecución.

</dd> <dt>

*method-name* 
</dt> <dd>

Nombre del método.

</dd> <dt>

*method-parameter-list* 
</dt> <dd>

Cero o más parámetros para el método .

</dd> </dl>

## <a name="remarks"></a>Comentarios

La aplicación del atributo **\[ uidefault \]** a un miembro de una interfaz o una interfaz dispinterface indica a Visual Basic, en tiempo de diseño, que muestre automáticamente este evento o propiedad al usuario. Esto significa que cuando el usuario hace doble clic en un objeto, Visual Basic salta al evento en la interfaz de origen predeterminada que tiene el **\[ atributo uidefault. \]** Cuando el usuario selecciona un objeto, Visual Basic explorador Propiedades muestra la propiedad en la interfaz de origen predeterminada que tiene este atributo. Si ningún evento o propiedad tiene el atributo **\[ uidefault, \]** Visual Basic muestra el primer evento o propiedad enumerado en la interfaz predeterminada.

### <a name="typeflag-representation"></a>Representación typeflag

La presencia de FUNCFLAG \_ QUEDEFAULT o VARFLAG \_ QUEERDEFAULT

## <a name="examples"></a>Ejemplos

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget]HRESULT Backcolor([out, retval] long *Value);
    [propput]HRESULT Backcolor([in] long Value);
    [propget, uidefault]HRESULT Name([out, retval] BSTR *Value);
    [propput, uidefault]HRESULT Name([in] BSTR Value);
}
[
    odl,
    dual,
    uuid(87654321-1234-1234-1234-123456789ABC),
    restricted
] 
interface IFormEvents: IDispatch
{
    [uidefault]HRESULT Click();
    HRESULT Resize();
}

[
    uuid(12345678-1234-1234-1234-987654321ABC)
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 