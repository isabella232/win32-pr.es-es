---
title: struct (atributo)
description: La palabra clave struct se usa en un especificador de tipo de estructura.
ms.assetid: 89e18f0e-185a-408e-812d-3d11f228b473
keywords:
- atributo de estructura MIDL
topic_type:
- apiref
api_name:
- struct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5c97ca9a2dbbfeddc5416b517e85e0926434c5d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665807"
---
# <a name="struct-attribute"></a>struct (atributo)

La palabra clave **struct** se usa en un especificador de tipo de estructura.

``` syntax
struct [[ struct-tag ]] 
{
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
    ...
};
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*struct: etiqueta* 
</dt> <dd>

Especifica una etiqueta opcional para la estructura.

</dd> <dt>

*lista de atributos de campo* 
</dt> <dd>

Especifica cero o más atributos de campo que se aplican al miembro de estructura. Entre los atributos de campo válidos **\[** [**se incluyen First \_ es**](first-is.md) **\]** , **\[** [**Last \_ es**](last-is.md) **\]** , **\[** [**length \_**](length-is.md)is **\]** , **\[** [**Max \_ is**](max-is.md) **\]** y **\[** [**size \_ es**](size-is.md) **\]** ; la cadena de atributos de uso **\[** [](string.md) **\]** y **\[** [**Ignore**](ignore.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** y el **\[** [**\_ tipo de modificador**](switch-type.md)de atributo Union **\]** . Separe varios atributos de campo con comas.

</dd> <dt>

*Type-Specifier* 
</dt> <dd>

Especifica un tipo [base](midl-base-types.md), un **struct**, una [**Unión**](union.md)o un tipo de [**enumeración**](enum.md) o un identificador de tipo. Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.

</dd> <dt>

*lista de declaradores* 
</dt> <dd>

Especifica uno o más declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. (Los declaradores de función y las declaraciones de campo de bits no se permiten en las estructuras que se transmiten en llamadas a procedimientos remotos. Estos declaradores se permiten en estructuras que no se transmiten). Separe varios declaradores con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El especificador de tipo de estructura IDL, **struct**, difiere del especificador de tipo C estándar de las maneras siguientes:

-   Cada miembro de la estructura puede asociarse a atributos de campo opcionales que describen las características de ese miembro de estructura para los fines de una llamada a procedimiento remoto.
-   Los campos de bits y los declaradores de función no se permiten en estructuras que se utilizan en llamadas a procedimientos remotos. Estas construcciones de declarador de C estándar solo se pueden usar si la estructura no se transmite en la red.

La forma de las estructuras debe ser la misma en todas las plataformas para garantizar la interconectividad.

## <a name="examples"></a>Ejemplos

``` syntax
typedef struct _PITCHER_RECORD_TYPE 
{ 
    short flag; 
    [switch_is(flag)] union PITCHER_STATISTICS_TYPE p; 
} PITCHER_RECORD_TYPE;
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**matrices**](arrays-1.md)
</dt> <dt>

[Matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Atributos array y Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**/c \_ ext**](-c-ext.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[**enumeración**](enum.md)
</dt> <dt>

[**el primero \_ es**](first-is.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**omitir**](ignore.md)
</dt> <dt>

[**última \_ es**](last-is.md)
</dt> <dt>

[**la longitud \_ es**](length-is.md)
</dt> <dt>

[**Max \_ es**](max-is.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**el tamaño \_ es**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**tipo de conmutador \_**](switch-type.md)
</dt> <dt>

[**Unión**](union.md)
</dt> <dt>

[**espeficarse**](unique.md)
</dt> </dl>

 

 