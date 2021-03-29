---
title: dispinterface (atributo)
description: La instrucción dispinterface define un conjunto de propiedades y métodos en los que se puede llamar a IDispatch Invoke.
ms.assetid: d85a8e2b-0155-4d68-bb38-e86f4807e7de
keywords:
- atributo dispinterface MIDL
topic_type:
- apiref
api_name:
- dispinterface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7cc2b6087b53ff81aa7270a209266dd8248884
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904591"
---
# <a name="dispinterface-attribute"></a>dispinterface (atributo)

La instrucción **dispinterface** define un conjunto de propiedades y métodos en los que se puede llamar a **IDispatch:: Invoke**. Se puede definir una interfaz dispinterface indicando explícitamente el conjunto de métodos y propiedades admitidos (sintaxis 1), o bien enumerando una sola interfaz (sintaxis 2).

``` syntax
[
    [attributes]
]
dispinterface dispinterface-name
{
    properties:
        property-list
    methods:
        method-list
};

[
  [attributes]
]
dispinterface dispinterface-name
{
    interface interface-name
};
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*attributes* 
</dt> <dd>

Especifica los atributos que se aplican a toda la **dispinterface**. Se aceptan los siguientes atributos: **\[** [**HelpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**HelpFile**](helpfile.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , **\[** [**nonextensible (**](nonextensible.md) **\]** , **\[** [**oleautomation**](oleautomation.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** , **\[** [**UUID**](uuid.md) **\]** y **\[** [**version**](version.md) **\]** .

</dd> <dt>

*dispinterface: nombre* 
</dt> <dd>

Nombre por el que se conoce la **dispinterface** en la biblioteca de tipos. Este nombre debe ser único en la biblioteca de tipos.

</dd> <dt>

*lista de propiedades* 
</dt> <dd>

(Sintaxis 1) Lista opcional de propiedades admitidas por el objeto, declaradas en forma de variables. Esta es la forma abreviada para declarar las funciones de propiedad en la lista de métodos. Vea la sección Comentarios para obtener más información.

</dd> <dt>

*lista de métodos* 
</dt> <dd>

(Sintaxis 1) Lista que consta de un prototipo de función para cada método y propiedad de la **dispinterface**. Puede aparecer cualquier número de definiciones de función en *methlist*. Una función de *methlist* tiene el formato siguiente:

**\[ \] ***attributes***** *ReturnType methname Type paramName ***(*** params * * *);**

Se aceptan los siguientes atributos en un método de una **interfaz dispinterface**: **\[ HelpString \]**, **\[ HelpContext \]**, **\[** [**propget**](propget.md) **\]** , **\[** [**PROPPUT**](propput.md) **\]** , **\[** [**PROPPUTREF**](propputref.md) **\]** , **\[** [**String**](string.md) **\]** y **\[** [**vararg**](vararg.md) **\]** . Si se especifica **\[ \] vararg** , el último parámetro debe ser una matriz segura de tipo **Variant** .

La lista de parámetros es una lista delimitada por comas, donde cada elemento tiene el formato siguiente:

**\[***sus***\]**

El *tipo* puede ser cualquier tipo declarado o integrado, o un puntero a cualquier tipo. Los atributos de los parámetros son:

**\[**[**in**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** , **\[** [**Optional**](optional.md) **\]** , **\[ String \]**

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

(Sintaxis 2) Nombre de la interfaz que se va a declarar como interfaz IDispatch.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El compilador MIDL acepta el siguiente orden de parámetros (de izquierda a derecha):

1.  Parámetros obligatorios (parámetros que no tienen los \[ \] atributos DefaultValue u \[ opcional \] ),
2.  parámetros opcionales con o sin el \[ \] atributo DefaultValue,
3.  parámetros con el \[ \] atributo opcional y sin el \[ \] atributo DefaultValue,
4.  \[parámetro [**LCID**](lcid.md) \] , si existe,
5.  \[[**retval**](retval.md) \] parámetro

Las funciones de método se especifican exactamente como se describe en la página de referencia del [**módulo**](module.md) , con la excepción de que \[ [](entry.md) \] no se permite el atributo de entrada. Tenga en cuenta que STDOLE32. TLB (STDOLE. TLB en sistemas de 16 bits) debe importarse, ya que una **dispinterface** hereda de IDispatch.

Puede declarar propiedades en las listas propiedades o métodos. Al declarar las propiedades en la lista de propiedades, no se indica el tipo de acceso que admite la propiedad (es decir, get, Put o putref). Especifique el \[ atributo [**ReadOnly**](readonly.md) \] para las propiedades que no admiten Put o putref. Si declara las funciones de propiedad en la lista de métodos, las funciones de una propiedad tienen el mismo identificador.

Con la primera sintaxis, las propiedades: y METHODS: Tags son obligatorias. \[ [](id.md) \] También se requiere el atributo ID en cada miembro. Por ejemplo:

``` syntax
properties: 
    [id(0)] int Value;    // Default property. 
methods: 
    [id(1)] HRESULT Show();
```

A diferencia de los miembros de interfaz, los miembros dispinterface no pueden usar el atributo [**retval**](retval.md) para devolver un valor además de un código de error HRESULT. El \[ [](lcid.md) \] atributo LCID tampoco es válido para dispinterfaces, porque IDispatch:: Invoke pasa un LCID. Sin embargo, es posible volver a declarar una interfaz que utilice estos atributos.

Con la segunda sintaxis, las interfaces que admiten IDispatch y que se declaran anteriormente en un script ODL se pueden volver a declarar como interfaces IDispatch como se indica a continuación:

``` syntax
dispinterface helloPro 
{ 
    interface hello; 
};
```

En el ejemplo anterior se declaran todos los miembros de Hello y todos los miembros que Hello hereda como compatibles con IDispatch. En este caso, si Hello se declaró anteriormente con \[ \] \[ los miembros LCID y retval \] que devolvieron Valores HRESULT, MkTypLib quitaría cada \[ \] parámetro de LCID y el tipo de valor devuelto HRESULT, y en su lugar marcaría el tipo de valor devuelto como el del \[ \] parámetro retval.

> [!Note]  
> La herramienta Mktyplib.exe está obsoleta. En su lugar, utilice el compilador de MIDL.

 

Las propiedades y los métodos de una interfaz dispinterface no forman parte de la VTBL de la dispinterface. Por consiguiente, [CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) y [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) no se pueden usar para implementar IDispatch:: Invoke. La dispinterface se utiliza cuando una aplicación necesita exponer funciones existentes que no son VTBL a través de la automatización. Estas aplicaciones pueden implementar IDispatch:: Invoke examinando el parámetro dispidMember y llamando directamente a la función correspondiente.

## <a name="examples"></a>Ejemplos

``` syntax
[ 
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("Useful help string."), 
    helpcontext(2480)
] 
dispinterface MyDispatchObject 
{ 
    properties: 
        [id(1)] int x;    //An integer property named x 
        [id(2)] BSTR y;   //A string property named y 
    methods: 
        [id(3)] HRESULT show();    //No arguments, no result 
        [id(11)] int computeit(int inarg, double *outarg); 
}; 
 
[
    uuid(1e123456-1f3c-1069-996b-00dd010fe676)
] 
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
 
        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[**defaultbind**](defaultbind.md)
</dt> <dt>

[**displaybind**](displaybind.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpfile**](helpfile.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**plusvalía**](hidden.md)
</dt> <dt>

[**de**](in.md)
</dt> <dt>

[**interfaz**](interface.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**opta**](optional.md)
</dt> <dt>

[**enuncia**](out-idl.md)
</dt> <dt>

[**nonextensible**](nonextensible.md)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**PROPPUT**](propput.md)
</dt> <dt>

[**PROPPUTREF**](propputref.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**Restrict**](restricted.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**Versión**](version.md)
</dt> </dl>

 

 