---
title: range (atributo)
description: El atributo \ range\ permite especificar un intervalo de valores permitidos para argumentos o campos cuyos valores se establecen en tiempo de ejecución. Cuando se usa con un tipo de canalización, el atributo especifica el intervalo permitido para el recuento de elementos en los fragmentos de canalización.
ms.assetid: 1609fea5-e82c-4389-b4f4-2cd8d0622cde
keywords:
- atributo range MIDL
topic_type:
- apiref
api_name:
- range
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8be59ef1b212d0f6953063ce7ac3239d8940a5ea54a623990fc3d7af9f36ad3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764315"
---
# <a name="range-attribute"></a>range (atributo)

El **\[ atributo range \]** permite especificar un intervalo de valores permitidos para argumentos o campos cuyos valores se establecen en tiempo de ejecución. Cuando se usa con un tipo de canalización, el atributo especifica el intervalo permitido para el recuento de elementos en los fragmentos de canalización.

``` syntax
[range(low-val,high-val)] type-specifier declarator
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*low-val* 
</dt> <dd>

El valor más bajo permitido que puede contener el parámetro o el campo.

</dd> <dt>

*high-val* 
</dt> <dd>

Valor máximo permitido que puede contener el parámetro o campo.

</dd> <dt>

*type-specifier* 
</dt> <dd>

Un tipo entero distinto de [**hyper**](hyper.md) o [**\_ \_ int64,**](--int64.md)un identificador de tipo para un tipo entero, [**un tipo de**](enum.md) enumeración o un nombre de tipo de canalización.

</dd> <dt>

*declarador* 
</dt> <dd>

Declarador de C estándar, como un identificador.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Use el atributo **\[ range \]** para modificar el significado de parámetros o campos confidenciales, como los que se usan para el tamaño o la longitud, con matrices compatibles o variables; o siempre que desee comprobar un parámetro o valor de campo con un intervalo de valores válidos. El atributo es aplicable a los parámetros de nivel superior, así como a los parámetros y campos de nivel inferior. Agregar el **\[ atributo de \]** intervalo a un tipo no cambia su formato de conexión, por lo que no afecta a la compatibilidad con versiones anteriores.

El **\[ atributo range \]** también se puede usar en datos compatibles, como búferes o matrices con un atributo de conformidad. El efecto es limitar todos los tamaños de conformidad de los datos conformes al intervalo especificado. Si los datos compatibles son una matriz multidimensional, cada dimensión de matriz se limita al intervalo especificado.

El uso **\[ del intervalo \]** en los datos compatibles requiere que el destino de compilación sea â€"target NT60 o superior.

Tenga en cuenta que debe usar la opción del compilador [**/robust**](-robust.md) al compilar el archivo IDL para generar el código auxiliar que realizará estas comprobaciones. Sin el **modificador /robust,** el compilador midl omite este atributo.

## <a name="examples"></a>Ejemplos

``` syntax
HRESULT Method1(
    [in, range(0,100)] ULONG m,
    [in, range(0,100)] ULONG n,
    [size_is(m,n)] ULONG **pplong);

void InPipe(
    [in, range(0, MAX_CHUNK) LONG_PIPE pipe_date);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[matrices](/windows/desktop/Rpc/arrays)
</dt> <dt>

[**en \_ primer lugar es**](first-is.md)
</dt> <dt>

[**el \_ último es**](last-is.md)
</dt> <dt>

[**length \_ es**](length-is.md)
</dt> <dt>

[**max \_ is**](max-is.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**el \_ tamaño es**](size-is.md)
</dt> <dt>

[**switch \_ es**](switch-is.md)
</dt> </dl>

 

 