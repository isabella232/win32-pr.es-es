---
title: coclass (atributo)
description: La instrucción coclass proporciona una lista de las interfaces admitidas para un objeto de componente.
ms.assetid: 2c636327-ad18-4087-b495-d1aa84a07f48
keywords:
- atributo de coclase MIDL
topic_type:
- apiref
api_name:
- coclass
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba95b38675869637c679a2409a82fb812709ec8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420649"
---
# <a name="coclass-attribute"></a>coclass (atributo)

La instrucción **CoClass** proporciona una lista de las interfaces admitidas para un objeto de componente.

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

*coclass-Attribute-List* 
</dt> <dd>

El **\[** atributo [**UUID**](uuid.md) **\]** es necesario en una **coclase**. Es el mismo **\[ UUID \]** que se registra como CLSID en la base de datos de registro del sistema. Los **\[** atributos [**HelpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**licensed**](licensed.md) **\]** , **\[** [**version**](version.md) **\]** , **\[** [**control**](control.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** y **\[** [**appobject**](appobject.md) **\]** se aceptan, pero no es necesario, antes de una definición de **coclase** .

</dd> <dt>

*classname* 
</dt> <dd>

Nombre por el que se conoce el objeto común en la biblioteca de tipos.

</dd> <dt>

*interfaz: atributos* 
</dt> <dd>

Atributos opcionales para la interfaz o dispinterface. Los **\[** atributos [**source**](source.md) **\]** , **\[** [**default**](default.md) **\]** y **\[** [**Restricted**](restricted.md) **\]** se aceptan en una interfaz o dispinterface dentro de una **coclase**.

</dd> <dt>

*interfaz* 
</dt> <dd>

Una interfaz declarada con la palabra clave [**interface**](interface.md) o una dispinterface declarada con la palabra clave [**dispinterface**](dispinterface.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

El modelo de objetos componentes de Microsoft define una clase como una implementación de que permite **QueryInterface** entre un conjunto de interfaces.

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

[**control**](control.md)
</dt> <dt>

[**predeterminada**](default.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**plusvalía**](hidden.md)
</dt> <dt>

[**interfaz**](interface.md)
</dt> <dt>

[**bajo**](licensed.md)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Restrict**](restricted.md)
</dt> <dt>

[**fuentes**](source.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**uuid**](uuid.md)
</dt> <dt>

[**Versión**](version.md)
</dt> </dl>

 

 