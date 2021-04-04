---
title: iid_is (atributo)
description: El atributo \ IID \_ es \ Pointer especifica el IID de la interfaz com a la que apunta un puntero de interfaz.
ms.assetid: 7fb5eb87-15d8-4717-b79a-e8a81f2f7293
keywords:
- iid_is el atributo MIDL
topic_type:
- apiref
api_name:
- iid_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94c6f46a6828e81817e45ff6eb6eb8245b00a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076580"
---
# <a name="iid_is-attribute"></a>el \_ atributo IID es

El atributo **\[ IID \_ es \]** Pointer especifica el IID de la interfaz com a la que apunta un puntero de interfaz.

``` syntax
[ iid_is(limited-expression) ]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Limited-Expression* 
</dt> <dd>

Especifica una expresión del lenguaje C. El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas. MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede usar **\[ IID \_ está \]** en listas de atributos para los parámetros de función y para los miembros de estructura o Unión. El código auxiliar usa el IID para determinar cómo calcular las referencias del puntero de interfaz. Esto resulta útil para un puntero de interfaz que se escribe como un parámetro de clase base.

Los archivos que utilizan el **\[ IID \_ es \]** deben compilarse con el compilador MIDL en el modo predeterminado, que no usa el modificador [**/OSF**](-osf.md)

## <a name="examples"></a>Ejemplos

``` syntax
HRESULT    CreateInstance( 
    [in] REFIID riid, 
    [out, iid_is(riid)] IUnknown ** ppvObject);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**objeto**](object.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> </dl>

 

 




