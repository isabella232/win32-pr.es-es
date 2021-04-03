---
title: defaultvtable (atributo)
description: El atributo \ defaultvtable \ define una interfaz como la interfaz vtable predeterminada.
ms.assetid: 05e50935-c630-4f9e-a7ec-3bb70a9834f1
keywords:
- defaultvtable (atributo) MIDL
topic_type:
- apiref
api_name:
- defaultvtable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8086d60d0936dcf56738afadea4244a5fff758b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904574"
---
# <a name="defaultvtable-attribute"></a>defaultvtable (atributo)

El atributo **\[ defaultvtable \]** define una interfaz como la interfaz vtable predeterminada.

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

*coclass-Attribute-List* 
</dt> <dd>

Otros atributos que se aplican a la clase. Los **\[** atributos [**source**](source.md) **\]** y **\[** [**UUID**](uuid.md) **\]** son obligatorios.

</dd> <dt>

*nombre de coclase* 
</dt> <dd>

Nombre de la clase.

</dd> <dt>

*coclass-interface-List* 
</dt> <dd>

Una lista de interfaces para la clase.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una interfaz vtable predeterminada no puede ser una dispinterface; debe ser una interfaz dual o vtable o una interfaz. Si la interfaz es una interfaz dual, los receptores pueden suponer que recibirán eventos a través de vtable.

Una clase puede ser tanto una interfaz de origen predeterminada como una interfaz de origen vtable predeterminada, como se muestra en el ejemplo. En este caso, un receptor de notificaciones debe utilizar IID \_ IDISPATCH para recibir los eventos de envío y usar el identificador de interfaz para recibir los eventos de vtable.

### <a name="typeflag-representation"></a>Representación Typeflag

La presencia de IMPLTYPEFLAG \_ FDEFAULTVTABLE.

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

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**fuentes**](source.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> </dl>

 

 