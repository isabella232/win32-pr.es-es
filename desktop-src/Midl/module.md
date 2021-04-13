---
title: Module (atributo)
description: La instrucción Module define un grupo de funciones, normalmente un conjunto de puntos de entrada de DLL.
ms.assetid: 4dec207f-98bc-4784-a3c9-506ffe7523fe
keywords:
- atributo de módulo MIDL
topic_type:
- apiref
api_name:
- module
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1eb310c3e126caf9b25b8c015b840aea11791d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358888"
---
# <a name="module-attribute"></a>Module (atributo)

La instrucción **Module** define un grupo de funciones, normalmente un conjunto de puntos de entrada de dll.

``` syntax
[
    attributes
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*attributes* 
</dt> <dd>

Los \[ atributos [**UUID**](uuid.md) \] , \[ [**version**](version.md) \] , \[ [**HelpString**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**Hidden**](hidden.md) \] y \[ [**DllName**](dllname-str-.md) \] se aceptan antes de una instrucción **Module** . Vea [descripciones de atributos](/previous-versions/windows/desktop/automat/attribute-descriptions), en el libro de automatización OLE, para obtener más información sobre los atributos aceptados antes de la definición de un módulo. El \[ atributo **DllName** \] es obligatorio. Si \[  \] se omite el atributo UUID, el módulo no se especifica de forma única en el sistema.

</dd> <dt>

*ModuleName* 
</dt> <dd>

El nombre del módulo.

</dd> <dt>

*elementlist* 
</dt> <dd>

Lista de definiciones constantes y prototipos de función para cada función del archivo DLL. Puede aparecer cualquier número de definiciones de función en la lista de funciones. Una función de la lista de funciones tiene el formato siguiente:

\[*atributos* \] de *ReturnType* \[ *Convención de llamada funcName* \] (*params*);

\[*atributos* \] de [**const**](const.md) constantType *constname*  =  *constval*;

Solo \[ [](helpstring.md) \] se aceptan los atributos HelpString y \[ [**HelpContext**](helpcontext.md) \] para [**const**](const.md).

Los siguientes atributos se aceptan en una función de un módulo: \[ [**HelpString**](helpstring.md) \] , \[ [**HelpContext**](helpcontext.md) \] , \[ [**String**](string.md) \] , \[ [**entry**](entry.md) \] , \[ [**propget**](propget.md) \] , \[ [**PROPPUT**](propput.md) \] , \[ [**PROPPUTREF**](propputref.md) \] y \[ [**vararg**](vararg.md) \] . Si \[  \] se especifica vararg, el último parámetro debe ser una matriz segura de tipo **Variant** .

La Convención de llamada opcional puede ser una de \_ \_ Pascal/ \_ Pascal/Pascal, \_ \_ Cdecl/ \_ Cdecl/Cdecl o \_ \_ Stdcall/ \_ Stdcall/Stdcall. El *tipo de Convención de llamada paramName* puede incluir hasta dos subrayados iniciales.

La lista de parámetros es una lista delimitada por comas de:

\[*sus*\]

El tipo puede ser cualquier tipo declarado previamente o tipo integrado, un puntero a cualquier tipo o un puntero a un tipo integrado. Los atributos de los parámetros son:

\[[**in**](in.md) \] , \[ [**out**](out-idl.md) \] , \[ [**opcional**](optional.md) \] .

Si \[ [](optional.md) \] se utiliza opcional, los tipos de esos parámetros deben ser **variantes** o **variantes** \* .

</dd> </dl>

## <a name="remarks"></a>Observaciones

La salida del archivo de encabezado (. h) para los módulos es una serie de prototipos de función. La palabra clave **Module** y los corchetes adyacentes se quitan de la salida del archivo de encabezado (. h), pero se inserta un Comentario (// **módulo** *ModuleName*) antes que los prototipos. La palabra clave **extern** se inserta antes que las declaraciones.

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("This is not GDI.EXE"), 
    helpcontext(190), 
    dllname("MATH.DLL")
] 
module somemodule
{ 
    [helpstring("Color for the frame")] 
            unsigned long const COLOR_FRAME = 0xH80000006; 
    [helpstring("Not a rectangle but a square"), 
     entry(1)] 
            pascal double square([in] double x); 
};
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**const**](const.md)
</dt> <dt>

[Contenido de una biblioteca de tipos](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**DllName**](dllname-str-.md)
</dt> <dt>

[**movimientos**](entry.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**plusvalía**](hidden.md)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**PROPPUT**](propput.md)
</dt> <dt>

[**PROPPUTREF**](propputref.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**uuid**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**Versión**](version.md)
</dt> </dl>

 

 