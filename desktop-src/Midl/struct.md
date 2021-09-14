---
title: Atributo struct
description: La palabra clave struct se usa en un especificador de tipo de estructura.
ms.assetid: 89e18f0e-185a-408e-812d-3d11f228b473
keywords:
- ATRIBUTO DE ESTRUCTURA MIDL
topic_type:
- apiref
api_name:
- struct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5c97ca9a2dbbfeddc5416b517e85e0926434c5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159372"
---
# <a name="struct-attribute"></a>Atributo struct

La **palabra clave struct** se usa en un especificador de tipo de estructura.

``` syntax
struct [[ struct-tag ]] 
{
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
    ...
};
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*struct-tag* 
</dt> <dd>

Especifica una etiqueta opcional para la estructura .

</dd> <dt>

*field-attribute-list* 
</dt> <dd>

Especifica cero o más atributos de campo que se aplican al miembro de estructura. Los atributos de campo válidos incluyen primero , el último es , length es , max es y size es ; el atributo de uso string y ignore ; el atributo de puntero **\[** [**\_**](first-is.md) **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md); **\]** **\[** [**\_**](switch-type.md) **\]** y el tipo de modificador de atributo union . Separe varios atributos de campo con comas.

</dd> <dt>

*type-specifier* 
</dt> <dd>

Especifica un tipo [base](midl-base-types.md), **struct**, [**unión**](union.md)o tipo [**de enumeración**](enum.md) o identificador de tipo. Una especificación de almacenamiento opcional puede *preceder al especificador de tipo*.

</dd> <dt>

*declarator-list* 
</dt> <dd>

Especifica uno o varios declaradores de C estándar, como identificadores, declaradores de puntero y declaradores de matriz. (Los declaradores de función y las declaraciones de campo de bits no se permiten en estructuras que se transmiten en llamadas a procedimientos remotos. Estos declaradores se permiten en estructuras que no se transmiten). Separe varios declaradores con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El especificador de tipo de estructura IDL, **struct**, difiere del especificador de tipo C estándar de las maneras siguientes:

-   Cada miembro de estructura se puede asociar a atributos de campo opcionales que describen las características de ese miembro de estructura para los fines de una llamada a procedimiento remoto.
-   No se permiten campos de bits ni declaradores de función en estructuras que se usan en llamadas a procedimientos remotos. Estas construcciones de declarador de C estándar solo se pueden usar si la estructura no se transmite en la red.

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

[**Matrices**](arrays-1.md)
</dt> <dt>

[Matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Atributos de matriz Sized-Pointer matriz](array-and-sized-pointer-attributes.md)
</dt> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**/c \_ ext**](-c-ext.md)
</dt> <dt>

[**identificador de \_ contexto**](context-handle.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**en primer \_ lugar es**](first-is.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Ignorar**](ignore.md)
</dt> <dt>

[**el \_ último es**](last-is.md)
</dt> <dt>

[**length \_ es**](length-is.md)
</dt> <dt>

[**max \_ is**](max-is.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**el \_ tamaño es**](size-is.md)
</dt> <dt>

[**Cadena**](string.md)
</dt> <dt>

[**tipo \_ de conmutador**](switch-type.md)
</dt> <dt>

[**union**](union.md)
</dt> <dt>

[**Único**](unique.md)
</dt> </dl>

 

 