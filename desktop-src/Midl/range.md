---
title: range (atributo)
description: El atributo \ Range \ permite especificar un intervalo de valores permitidos para los argumentos o campos cuyos valores se establecen en tiempo de ejecución. Cuando se usa con un tipo de canalización, el atributo especifica el intervalo permitido para el recuento de elementos de los fragmentos de la canalización.
ms.assetid: 1609fea5-e82c-4389-b4f4-2cd8d0622cde
keywords:
- atributo de intervalo MIDL
topic_type:
- apiref
api_name:
- range
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e095d420afc433c1f01a63dff51868e57efc50f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665785"
---
# <a name="range-attribute"></a>range (atributo)

El atributo **\[ Range \]** permite especificar un intervalo de valores permitidos para los argumentos o campos cuyos valores se establecen en tiempo de ejecución. Cuando se usa con un tipo de canalización, el atributo especifica el intervalo permitido para el recuento de elementos de los fragmentos de la canalización.

``` syntax
[range(low-val,high-val)] type-specifier declarator
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*bajo-Val* 
</dt> <dd>

El valor mínimo permitido que puede contener el parámetro o el campo.

</dd> <dt>

*alto-Val* 
</dt> <dd>

Valor máximo permitido que puede contener el parámetro o el campo.

</dd> <dt>

*Type-Specifier* 
</dt> <dd>

Un tipo entero distinto de [**Hyper**](hyper.md) o [**\_ \_ Int64**](--int64.md), un identificador de tipo de un tipo entero, un tipo de [**enumeración**](enum.md) o un nombre de tipo de canalización.

</dd> <dt>

*clara* 
</dt> <dd>

Un declarador estándar de C, como un identificador.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use el atributo **\[ Range \]** para modificar el significado de los parámetros o campos confidenciales, como los que se usan para el tamaño o la longitud, con matrices compatibles o variables, o siempre que desee comprobar un valor de parámetro o campo con respecto a un intervalo de valores válidos. El atributo se aplica a los parámetros de nivel superior, así como a los campos y parámetros de nivel inferior. Agregar el atributo de **\[ intervalo \]** a un tipo no cambia su formato de conexión, por lo que no afecta a la compatibilidad con versiones anteriores.

El atributo **\[ Range \]** también se puede utilizar en datos compatibles, como búferes o matrices con un atributo de conformidad. El efecto es limitar todos los tamaños de conformidad para los datos compatibles con el intervalo especificado. Si los datos conformes son una matriz multidimensional, cada dimensión de la matriz se limita al intervalo especificado.

El uso del **\[ intervalo \]** en los datos conformes requiere que el destino de compilación sea â € "Target NT60 o superior.

Tenga en cuenta que debe utilizar la opción del compilador [**/Robust**](-robust.md) al compilar el archivo IDL para generar el código auxiliar que realizará estas comprobaciones. Sin el modificador **/Robust** , el compilador MIDL omite este atributo.

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

[**el primero \_ es**](first-is.md)
</dt> <dt>

[**última \_ es**](last-is.md)
</dt> <dt>

[**la longitud \_ es**](length-is.md)
</dt> <dt>

[**Max \_ es**](max-is.md)
</dt> <dt>

[**/Robust**](-robust.md)
</dt> <dt>

[**el tamaño \_ es**](size-is.md)
</dt> <dt>

[**el modificador \_ es**](switch-is.md)
</dt> </dl>

 

 