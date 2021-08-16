---
title: atributo module
description: La instrucción module define un grupo de funciones, normalmente un conjunto de puntos de entrada dll.
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
ms.openlocfilehash: 3a83528a1ec632fcf2309438e6228220544a32408b310ea90260b8bcfda3cb6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642813"
---
# <a name="module-attribute"></a>atributo module

La **instrucción** module define un grupo de funciones, normalmente un conjunto de puntos de entrada dll.

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

Los \[ [**atributos uuid**](uuid.md) \] , \[ [**version**](version.md) \] , \[ [**helpstring**](helpstring.md), helpcontext , hidden y \] \[ [](helpcontext.md) \] \[ [](hidden.md) \] \[ [**dllname**](dllname-str-.md) se aceptan antes que una instrucción \] **de** módulo. Vea [Descripciones de atributos](/previous-versions/windows/desktop/automat/attribute-descriptions), en el libro automatización OLE, para obtener más información sobre los atributos aceptados antes de una definición de módulo. Se \[ **requiere el atributo** \] dllname. Si se omite el atributo \[ **uuid,** el módulo no se especifica de forma \] única en el sistema.

</dd> <dt>

*modulename* 
</dt> <dd>

El nombre del módulo.

</dd> <dt>

*elementlist* 
</dt> <dd>

Lista de definiciones de constantes y prototipos de función para cada función del archivo DLL. Cualquier número de definiciones de función puede aparecer en la lista de funciones. Una función de la lista de funciones tiene el formato siguiente:

\[*atributos* \] *returntype* \[ *funcname de convención de llamada* \] (*params*);

\[*atributos* \] [**const**](const.md) constanttype *constname*  =  *constval*;

Solo se \[ [**aceptan los atributos**](helpstring.md) \] \[ [**helpstring y helpcontext**](helpcontext.md) para un elemento \] [**const.**](const.md)

Los atributos siguientes se aceptan en una función de un módulo: \[ [**helpstring**](helpstring.md) \] , \[ [**helpcontext**](helpcontext.md) \] , \[ [**string**](string.md) \] , \[ [**entry**](entry.md) \] , \[ [**propget**](propget.md), \] \[ [**propput,**](propput.md) \] \[ [**propputref**](propputref.md) \] \[ [**yutorg**](vararg.md) \] . Si se especifica , el último parámetro \[  \] debe ser una matriz segura de **tipo VARIANT.**

La convención de llamada opcional puede ser una de \_ \_ \_ pascal/pascal/pascal, \_ \_ cdecl/ \_ cdecl/cdecl, \_ \_ o stdcall/ \_ stdcall/stdcall. El tipo de convención de llamada *paramname* puede incluir hasta dos caracteres de subrayado iniciales.

La lista de parámetros es una lista delimitada por comas de:

\[*Atributos*\]

El tipo puede ser cualquier tipo declarado previamente o un tipo integrado, un puntero a cualquier tipo o un puntero a un tipo integrado. Los atributos de los parámetros son:

\[[**en**](in.md) \] , \[ [**out**](out-idl.md) \] , \[ [**opcional.**](optional.md) \]

Si \[ [**se**](optional.md) \] usa opcional, los tipos de esos parámetros deben ser **VARIANT** o **VARIANT.** \*

</dd> </dl>

## <a name="remarks"></a>Comentarios

La salida del archivo de encabezado (.h) para los módulos es una serie de prototipos de función. La **palabra** clave module y los corchetes circundantes se quitan de la salida del archivo de encabezado (.h), pero se inserta un comentario (// **modulename** ) antes de los prototipos. La palabra clave **extern** se inserta antes de las declaraciones.

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

[**Dllname**](dllname-str-.md)
</dt> <dt>

[**Entrada**](entry.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**Oculto**](hidden.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**Cadena**](string.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**Versión**](version.md)
</dt> </dl>

 

 