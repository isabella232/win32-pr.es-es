---
title: uidefault (atributo)
description: El atributo \ uidefault \ indica que el miembro de información de tipo es el miembro predeterminado que se va a mostrar en la interfaz de usuario.
ms.assetid: e789be38-a509-437d-89c9-ebbc830e5ae2
keywords:
- uidefault (atributo) MIDL
topic_type:
- apiref
api_name:
- uidefault
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcef39f36abad7c7cb5562b2d892761bd1bb7b5b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420568"
---
# <a name="uidefault-attribute"></a>uidefault (atributo)

El atributo **\[ uidefault \]** indica que el miembro de información de tipo es el miembro predeterminado que se va a mostrar en la interfaz de usuario.

``` syntax
[method-attribute-list, uidefault]return-type method-name(method-parameter-list)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*lista de atributos de método* 
</dt> <dd>

Otros atributos que se aplican al método.

</dd> <dt>

*tipo de valor devuelto* 
</dt> <dd>

El tipo de los datos que el método devolverá cuando finalice la ejecución.

</dd> <dt>

*nombre del método* 
</dt> <dd>

Nombre del método.

</dd> <dt>

*lista de parámetros de método* 
</dt> <dd>

Cero o más parámetros para el método.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al aplicar el atributo **\[ uidefault \]** a un miembro de una interfaz o una interfaz dispinterface se indica Visual Basic, en tiempo de diseño, para mostrar automáticamente este evento o propiedad al usuario. Esto significa que cuando el usuario hace doble clic en un objeto, Visual Basic salta al evento en la interfaz de origen predeterminada que tiene el atributo **\[ uidefault \]** . Cuando el usuario selecciona un objeto, el explorador de propiedades de Visual Basic muestra la propiedad en la interfaz de origen predeterminada que tiene este atributo. Si ningún evento o propiedad tiene el atributo **\[ uidefault \]** , Visual Basic muestra el primer evento o propiedad enumerados en la interfaz predeterminada.

### <a name="typeflag-representation"></a>Representación Typeflag

La presencia de FUNCFLAG \_ FUIDEFAULT o VARFLAG \_ FUIDEFAULT

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

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 