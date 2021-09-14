---
title: dispinterface (atributo)
description: La instrucción dispinterface define un conjunto de propiedades y métodos en los que puede llamar a IDispatch Invoke.
ms.assetid: d85a8e2b-0155-4d68-bb38-e86f4807e7de
keywords:
- Atributo dispinterface MIDL
topic_type:
- apiref
api_name:
- dispinterface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7cc2b6087b53ff81aa7270a209266dd8248884
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159615"
---
# <a name="dispinterface-attribute"></a>dispinterface (atributo)

La **instrucción dispinterface** define un conjunto de propiedades y métodos en los que puede llamar a **IDispatch::Invoke**. Una interfaz dispinterface se puede definir enumerando explícitamente el conjunto de métodos y propiedades admitidos (sintaxis 1) o enumerando una sola interfaz (sintaxis 2).

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

Especifica los atributos que se aplican a toda **la interfaz dispinterface**. Se aceptan los atributos siguientes: **\[** [**helpstring**](helpstring.md) **\]** , **\[** [**helpcontext**](helpcontext.md) **\]** , **\[** [**helpfile**](helpfile.md), **\]** **\[** [**hidden**](hidden.md), **\]** **\[** [**nonextensible,**](nonextensible.md) **\]** **\[** [**oleautomation**](oleautomation.md), **\]** **\[** [**restricted**](restricted.md), **\]** **\[** [**uuid**](uuid.md)y **\]** **\[** [**version**](version.md) **\]** .

</dd> <dt>

*dispinterface-name* 
</dt> <dd>

Nombre por el que se **conoce la interfaz dispinterface** en la biblioteca de tipos. Este nombre debe ser único dentro de la biblioteca de tipos.

</dd> <dt>

*property-list* 
</dt> <dd>

(Sintaxis 1) Lista opcional de propiedades admitidas por el objeto , declaradas en forma de variables. Este es el formato corto para declarar las funciones de propiedad en la lista de métodos. Consulte la sección de comentarios para obtener más información.

</dd> <dt>

*method-list* 
</dt> <dd>

(Sintaxis 1) Lista que contiene un prototipo de función para cada método y propiedad de **la interfaz dispinterface**. Cualquier número de definiciones de función puede aparecer en *la lista de methlist.* Una función de *methlist* tiene el formato siguiente:

**\[**_atributos_ *_\]_* *returntype methname type paramname***(**_params_*_);_*

Los atributos siguientes se aceptan en un método en una **interfaz dispinterface:** **\[ \] helpstring**, **\[ helpcontext \]**, **\[** [**propget,**](propget.md) **\]** **\[** [**propput,**](propput.md) **\]** **\[** [**propputref**](propputref.md), **\]** **\[** [**string**](string.md)y **\]** **\[** [**.**](vararg.md) **\]** Si **\[ se \] especifica ,** el último parámetro debe ser una matriz segura de tipo **VARIANT.**

La lista de parámetros es una lista delimitada por comas, cada elemento de la que tiene la forma siguiente:

**\[**_Atributos_*_\]_*

El *tipo* puede ser cualquier tipo declarado o integrado, o un puntero a cualquier tipo. Los atributos de los parámetros son:

**\[**[**en**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** , **\[** [**opcional**](optional.md) **\]** , **\[ cadena \]**

</dd> <dt>

*interface-name* 
</dt> <dd>

(Sintaxis 2) Nombre de la interfaz que se declara como interfaz IDispatch.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El compilador MIDL acepta la siguiente ordenación de parámetros (de izquierda a derecha):

1.  Parámetros obligatorios (parámetros que no tienen el \[ valor predeterminado u atributos \] \[ \] opcionales),
2.  Parámetros opcionales con o sin el \[ atributo \] defaultvalue,
3.  parámetros con el \[ atributo opcional y sin el atributo \] \[ \] defaultvalue,
4.  \[[**parámetro lcid,**](lcid.md) \] si lo hay,
5.  \[[**retval**](retval.md) \] Parámetro

Las funciones de método se especifican exactamente como se describe en la página de referencia del [**módulo,**](module.md) salvo que no se permite \[ [](entry.md) \] el atributo de entrada. Tenga en cuenta que STDOLE32. TLB (STDOLE. TLB en sistemas de 16 bits) debe importarse, porque **una interfaz dispinterface** hereda de IDispatch.

Puede declarar propiedades en las listas de propiedades o métodos. La declaración de propiedades en la lista de propiedades no indica el tipo de acceso que admite la propiedad (es decir, get, put o putref). Especifique el \[ [**atributo readonly**](readonly.md) \] para las propiedades que no admiten put o putref. Si declara las funciones de propiedad en la lista de métodos, todas las funciones de una propiedad tienen el mismo identificador.

Con la primera sintaxis, se requieren las etiquetas properties: y methods: . El \[ [**atributo id**](id.md) \] también es necesario en cada miembro. Por ejemplo:

``` syntax
properties: 
    [id(0)] int Value;    // Default property. 
methods: 
    [id(1)] HRESULT Show();
```

A diferencia de los miembros de interfaz, los miembros dispinterface no pueden usar el atributo [**retval**](retval.md) para devolver un valor además de un código de error HRESULT. El \[ [**atributo lcid**](lcid.md) tampoco es válido para \] las interfaces dispinterface, porque IDispatch::Invoke pasa un LCID. Sin embargo, es posible volver a declarar una interfaz que use estos atributos.

Con la segunda sintaxis, las interfaces que admiten IDispatch y se declaran anteriormente en un script ODL se pueden volver a declarar como interfaces IDispatch como las siguientes:

``` syntax
dispinterface helloPro 
{ 
    interface hello; 
};
```

En el ejemplo anterior se declaran todos los miembros de hello y todos los miembros que hello hereda como compatibles con IDispatch. En este caso, si hello se declarase anteriormente con miembros lcid y retval que devolvían \[ \] \[ \] HESULT, MkTypLib quitaría cada \[ parámetro lcid \] \[ y tipo \] de valor devuelto HRESULT y, en su lugar, marcaría el tipo de valor devuelto como el del parámetro retval.

> [!Note]  
> La Mktyplib.exe está obsoleta. En su lugar, use el compilador MIDL.

 

Las propiedades y los métodos de una interfaz dispinterface no forman parte del VTBL de la interfaz dispinterface. Por lo tanto, [CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) y [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) no se pueden usar para implementar IDispatch::Invoke. La interfaz dispinterface se usa cuando una aplicación necesita exponer funciones existentes que no son VTBL a través de Automation. Estas aplicaciones pueden implementar IDispatch::Invoke examinando el parámetro dispidMember y llamando directamente a la función correspondiente.

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

[**Oculto**](hidden.md)
</dt> <dt>

[**En**](in.md)
</dt> <dt>

[**Interfaz**](interface.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Opcional**](optional.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**nonextensible**](nonextensible.md)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**Restringido**](restricted.md)
</dt> <dt>

[**Cadena**](string.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**version**](version.md)
</dt> </dl>

 

 