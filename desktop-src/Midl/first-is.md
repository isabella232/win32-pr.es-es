---
title: first_is (atributo)
description: El atributo \ first is\ especifica el índice del primer elemento de \_ matriz que se va a transmitir.
ms.assetid: 1de7821c-19e7-4b2c-98fc-2fae3563831c
keywords:
- first_is atributo MIDL
topic_type:
- apiref
api_name:
- first_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d08be3ce14074c126a35272ede1b670121634f75d0b3d6cfb0db34e4f305760
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067285"
---
# <a name="first_is-attribute"></a>first \_ es el atributo

El \[ **primer atributo \_ es** especifica el índice del primer elemento de \] matriz que se va a transmitir.

``` syntax
first_is(limited-expression-list)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*limited-expression-list* 
</dt> <dd>

Especifica una o varias expresiones de lenguaje C. Cada expresión se evalúa como un entero que representa el índice de matriz del primer elemento de matriz que se va a transmitir. El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas. MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento. Separe varias expresiones con comas.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si el **\[ primer atributo \_ es \]** no está presente, o si el índice especificado es un número negativo, el elemento de matriz cero es el primer elemento transmitido.

El **\[ primer atributo \_ es \]** también puede ayudar a determinar los valores de los índices de matriz correspondientes al último atributo is o **\[** [**\_**](last-is.md) length **\]** **\[** [**\_ is**](length-is.md) **\]** attribute cuando no se especifican estos atributos. La relación entre estos índices de matriz es:

``` syntax
length = last - first + 1
```

La relación siguiente también debe contener:

``` syntax
0 <= first_is <= max_is
```

La siguiente relación debe contener cuando **\[** [**max es \_ <**](max-is.md) **\] = 0:**

``` syntax
first_is == 0
```

El **\[ primer atributo \_ es \]** no se puede usar al mismo tiempo que el **\[** [**atributo de**](string.md) **\]** cadena.

El uso de una expresión constante con **\[ el primer atributo \_ es \]** un uso inadecuado del atributo. Es legal, pero ineficaz, y dará lugar a un código de serialización más lento.

## <a name="examples"></a>Ejemplos

``` syntax
HRESULT Proc1(
    [in] short First,
    [first_is(First)] Arr[10]);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[atributos de \_ campo](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**el \_ último es**](last-is.md)
</dt> <dt>

[**length \_ es**](length-is.md)
</dt> <dt>

[**max \_ is**](max-is.md)
</dt> <dt>

[**min \_ es**](min-is.md)
</dt> <dt>

[**el \_ tamaño es**](size-is.md)
</dt> <dt>

[**Cadena**](string.md)
</dt> </dl>

 

 