---
title: coclass (atributo)
description: La instrucción coclass proporciona una lista de las interfaces admitidas para un objeto de componente.
ms.assetid: 2c636327-ad18-4087-b495-d1aa84a07f48
keywords:
- atributo coclass MIDL
topic_type:
- apiref
api_name:
- coclass
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba95b38675869637c679a2409a82fb812709ec8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159651"
---
# <a name="coclass-attribute"></a>coclass (atributo)

La **instrucción coclass** proporciona una lista de las interfaces admitidas para un objeto de componente.

``` syntax
[
    coclass-attribute-list
]
coclass classname
{
    [
        interface-attributes
    ] 
    [interface | dispinterface] interfacename 
    {
  . . . 
    }
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*coclass-attribute-list* 
</dt> <dd>

El **\[** [**atributo uuid**](uuid.md) **\]** es necesario en una **coclase**. Se trata del mismo **\[ uuid \]** que se registra como CLSID en la base de datos de registro del sistema. Los atributos helpstring , helpcontext , licensed , version , control , hidden y appobject se aceptan, pero no son necesarios, antes de una **\[** [](helpstring.md) **\]** **\[** [](helpcontext.md) **\]** **\[** [](licensed.md) **\]** **\[** [](version.md) **\]** **\[** [](control.md) **\]** **\[** [](hidden.md) **\]** **\[** [](appobject.md) **\]** **definición de la coclase.**

</dd> <dt>

*classname* 
</dt> <dd>

Nombre por el que se conoce el objeto común en la biblioteca de tipos.

</dd> <dt>

*interface-attributes* 
</dt> <dd>

Atributos opcionales para la interfaz o dispinterface. Los atributos de origen , predeterminado y restringido **\[** [](source.md) **\]** se **\[** [](default.md) **\]** aceptan en **\[** [](restricted.md) **\]** una interfaz o interfaz dispinterface dentro de **una coclase**.

</dd> <dt>

*interfacename* 
</dt> <dd>

Una interfaz declarada con la palabra clave [**interface**](interface.md) o una interfaz dispinterface declarada con la [**palabra clave dispinterface.**](dispinterface.md)

</dd> </dl>

## <a name="remarks"></a>Observaciones

El modelo de objetos componentes de Microsoft define una clase como una implementación que permite **QueryInterface** entre un conjunto de interfaces.

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("A class"), 
    helpcontext(2481), appobject
] 
coclass myapp 
{ 
    [source] interface IMydocfuncs : IUnknown; 
    dispinterface DMydocfuncs; 
}; 
 
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
coclass mycoclass 
{ 
    [restricted] interface iface1; 
    interface iface2; 
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**appobject**](appobject.md)
</dt> <dt>

[**Control**](control.md)
</dt> <dt>

[**Predeterminado**](default.md)
</dt> <dt>

[**Dispinterface**](dispinterface.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**Oculto**](hidden.md)
</dt> <dt>

[**Interfaz**](interface.md)
</dt> <dt>

[**Licencia**](licensed.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Restringido**](restricted.md)
</dt> <dt>

[**Fuente**](source.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> <dt>

[**version**](version.md)
</dt> </dl>

 

 