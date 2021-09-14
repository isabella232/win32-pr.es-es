---
title: defaultcollelem (atributo)
description: El atributo \ defaultcollelem\ marca una propiedad como una función de accessor para un elemento de la colección predeterminada.
ms.assetid: e409f845-3f26-4551-abda-86c4776160aa
keywords:
- atributo defaultcollelem MIDL
topic_type:
- apiref
api_name:
- defaultcollelem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45fdbd59ca954d955fc5598b2bc2dc7a39ee14b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159628"
---
# <a name="defaultcollelem-attribute"></a>defaultcollelem (atributo)

El **\[ atributo defaultcollelem \]** marca una propiedad como una función de accessor para un elemento de la colección predeterminada.

``` syntax
[property-attribute-list, defaultcollelem] return-type property-name(prop-param-list)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*property-attribute-list* 
</dt> <dd>

Otros atributos que se aplican a la propiedad .

</dd> <dt>

*return-type* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*property-name* 
</dt> <dd>

El nombre de la propiedad.

</dd> <dt>

*prop-param-list* 
</dt> <dd>

Lista de cero o más parámetros asociados a la propiedad .

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ atributo defaultcollelem \]** se usa para la optimización ® código de Visual Basic. Si un miembro de una interfaz o dispinterface se marca como una función de accessor, la llamada irá directamente a ese miembro.

El uso **\[ de \] defaultcollelem** debe ser coherente para una propiedad. Por ejemplo, si usa el atributo en una *propiedad Get,* también debe estar presente en una *propiedad Let.*

### <a name="typeflags-representation"></a>Representación de typeflags

Presencia de FUNCFLAG \_ FDEFAULTCOLLELEM o VARFLAG \_ FDEFAULTCOLLELEM.

## <a name="examples"></a>Ejemplos

``` syntax
//A form has a button on it named Button1. 
//To enable use of the property syntax and efficient use of the !
//syntax, the form describes itself in type info this way.
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is IForm"),
    restricted
]
interface IForm1: IForm
{
    [propget, defaultcollelem] HRESULT Button1(
        [out, retval] Button *Value);
}

//User code may access the button using property syntax or ! syntax.

Sub Test()
Dim f as Form1
Dim b1 As Button
Dim b2 As Button

Set f = Form1

Set b1 = f.Button1        ' Property syntax
Set b = f!Button1        ' ! syntax
End Sub
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 