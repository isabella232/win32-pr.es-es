---
title: in (atributo)
description: El atributo \ in \ indica que se va a pasar un parámetro del procedimiento que realiza la llamada al procedimiento llamado.
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
ms.openlocfilehash: b606a834b394197960777fa485d112a94212ec45
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791374"
---
# <a name="in-attribute"></a>in (atributo)

El atributo **\[ in \]** indica que se va a pasar un parámetro del procedimiento que realiza la llamada al procedimiento llamado.

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ in [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*lista de atributos de función* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son **\[ \] callback**, **\[ \] local**, el atributo de puntero **\[ ref \]**, **\[ \] Unique** o **\[ ptr \]**, y los atributos de uso **\[ cadena \]**, **\[ omitir \]** y **\[ \_ identificador \] de contexto**.

</dd> <dt>

*Type-Specifier* 
</dt> <dd>

Especifica un **tipo \_ base**, un [**struct**](struct.md), una [**Unión**](union.md)o un tipo de [**enumeración**](enum.md) o un identificador de tipo. Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.

</dd> <dt>

*declarador de puntero* 
</dt> <dd>

Especifica cero o más declaradores de puntero. Un declarador de puntero es el mismo que el declarador de puntero utilizado en C; se construye a partir del \* designador, modificadores como **Far** y el calificador [**const**](const.md).

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Especifica cero o más atributos adecuados para el tipo de parámetro especificado. Los atributos de parámetro con el atributo in también pueden sacar el **\[ atributo \] direccional; los** atributos **\[ \] de** campo **\[ primero \_ \] son**, **\[ Last \_ es \]**, **\[ length \_ \]** es, **\[ Max \_ is \]**, **\[ size \_ is \]** y **\[ Switch \_ Type \]**; el atributo de puntero **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]**; y el **\[ \_ identificador \] de contexto** y la **\[ cadena \]** de atributos de uso. El atributo de uso **\[ Ignore \]** no se puede usar como atributo de parámetro. Separe varios atributos con comas.

</dd> <dt>

*clara* 
</dt> <dd>

Especifica los declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers). El declarador de parámetro del declarador de la función, como el nombre del parámetro, es opcional.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ in \]** tiene un atributo opuesto, **\[** [**out**](out-idl.md) **\]** , que indica que un parámetro se devolverá desde el procedimiento llamado al procedimiento que realiza la llamada. Los atributos in y **\[ out \]** se conocen como atributos **\[ de \]** parámetro direccional porque especifican la dirección en la que se pasan los parámetros. Un parámetro se puede definir como **\[ in \]**, **\[ out \]** o **\[ in**, **out \]**.

El atributo **\[ in \]** identifica los parámetros cuyas referencias se calculan mediante el código auxiliar de cliente para su transmisión al servidor.

El atributo in se aplica a un parámetro de forma predeterminada cuando no se especifica ningún atributo **\[ de \]** parámetro direccional.

## <a name="examples"></a>Ejemplos

``` syntax
HRESULT MyFunction([in] short count);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**\_asignación de usuarios de MIDL \_**](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[**enuncia**](out-idl.md)
</dt> </dl>

 

 