---
title: defaultcollelem (atributo)
description: El atributo \ defaultcollelem \ marca una propiedad como una función de descriptor de acceso para un elemento de la colección predeterminada.
ms.assetid: e409f845-3f26-4551-abda-86c4776160aa
keywords:
- defaultcollelem (atributo) MIDL
topic_type:
- apiref
api_name:
- defaultcollelem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45fdbd59ca954d955fc5598b2bc2dc7a39ee14b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077698"
---
# <a name="defaultcollelem-attribute"></a>defaultcollelem (atributo)

El atributo **\[ defaultcollelem \]** marca una propiedad como una función de descriptor de acceso para un elemento de la colección predeterminada.

``` syntax
[property-attribute-list, defaultcollelem] return-type property-name(prop-param-list)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Property-Attribute-List* 
</dt> <dd>

Otros atributos que se aplican a la propiedad.

</dd> <dt>

*tipo de valor devuelto* 
</dt> <dd>

Especifica el tipo de valor devuelto de la función.

</dd> <dt>

*nombre de propiedad* 
</dt> <dd>

Nombre de la propiedad.

</dd> <dt>

*prop-param-List* 
</dt> <dd>

Lista de cero o más parámetros asociados a la propiedad.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ defaultcollelem \]** se usa para la optimización del código de Visual BasicÂ®. Si un miembro de una interfaz o dispinterface se marca como una función de descriptor de acceso, la llamada irá directamente a ese miembro.

El uso de **\[ defaultcollelem \]** debe ser coherente para una propiedad. Por ejemplo, si usa el atributo en una propiedad *Get* , también debe estar presente en una propiedad *Let* .

### <a name="typeflags-representation"></a>Representación TYPEFLAGS

La presencia de FUNCFLAG \_ FDEFAULTCOLLELEM o VARFLAG \_ FDEFAULTCOLLELEM.

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

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 