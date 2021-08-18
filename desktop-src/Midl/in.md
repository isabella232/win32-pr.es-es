---
title: in (atributo)
description: El atributo \ in\ indica que se va a pasar un parámetro del procedimiento que realiza la llamada al procedimiento llamado.
ms.assetid: 85d5617e-8b73-449a-9627-2c8d5ab2b629
keywords:
- en el atributo MIDL
topic_type:
- apiref
api_name:
- in
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb78ad08dd5ba5494181d3fb2adecb7a8441e4716c42ba6cd4f1c119b3ccb046
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067235"
---
# <a name="in-attribute"></a>in (atributo)

El **\[ atributo in \]** indica que se va a pasar un parámetro del procedimiento que realiza la llamada al procedimiento llamado.

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ in [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*function-attribute-list* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son **\[ la \]** devolución de llamada , **\[ \] local**, el atributo de puntero **\[ ref \]**, **\[ unique \]** o **\[ ptr \]**, **\[ \]** **\[ \_ \]** **\[ \]** y la cadena de atributos de uso , omitir y el identificador de contexto .

</dd> <dt>

*type-specifier* 
</dt> <dd>

Especifica un tipo base , [**struct**](struct.md), [**union**](union.md)o [**tipo de enumeración**](enum.md) o identificador de tipo. **\_** Una especificación de almacenamiento opcional puede *preceder al especificador de tipo*.

</dd> <dt>

*pointer-declarator* 
</dt> <dd>

Especifica cero o más declaradores de puntero. Un declarador de puntero es el mismo que el declarador de puntero usado en C; se construye a partir del \* designador, modificadores como **, y** el calificador [**const**](const.md).

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Especifica cero o más atributos adecuados para el tipo de parámetro especificado. Los atributos de parámetro con el atributo **\[ in \]** **\[ \_ \]** **\[ \]** **\[ \]** **\[ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \]** también pueden sacar el atributo direccional; **\[ \_ \]** los atributos de campo primero son , **\[ \_ \]** el último es , length es , max es , size es y switch type ; el atributo de puntero ref , unique o **\[ ptr \]**; y el identificador de contexto de los atributos de uso y la cadena . El atributo usage **\[ ignore no \]** se puede usar como atributo de parámetro. Separe varios atributos con comas.

</dd> <dt>

*declarador* 
</dt> <dd>

Especifica declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers). El declarador de parámetros del declarador de función, como el nombre del parámetro, es opcional.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **\[ atributo in \]** tiene un atributo inverso, out , que indica que se va a devolver un parámetro del procedimiento llamado al procedimiento que realiza la **\[** [](out-idl.md) **\]** llamada. Los **\[ atributos de \]** entrada **\[ y \]** salida se conocen como atributos de parámetro direccionales porque especifican la dirección en la que se pasan los parámetros. Un parámetro se puede definir como **\[ en \]**, **\[ out \]** o **\[ en**, **out \]**.

El **\[ atributo in \]** identifica los parámetros serializados por el código auxiliar de cliente para la transmisión al servidor.

El **\[ atributo in \]** se aplica a un parámetro de forma predeterminada cuando no se especifica ningún atributo de parámetro direccional.

## <a name="examples"></a>Ejemplos

``` syntax
HRESULT MyFunction([in] short count);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**asignación de usuario midl \_ \_**](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[**out**](out-idl.md)
</dt> </dl>

 

 