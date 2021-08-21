---
title: iid_is (atributo)
description: El atributo de puntero \ iid is\ especifica el IID de la interfaz COM a la que apunta \_ un puntero de interfaz.
ms.assetid: 7fb5eb87-15d8-4717-b79a-e8a81f2f7293
keywords:
- iid_is atributo MIDL
topic_type:
- apiref
api_name:
- iid_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74553fdb1e3020d49eca7dfdd219354a4690056c45126b3af208395117ade991
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383872"
---
# <a name="iid_is-attribute"></a>iid \_ es atributo

El **\[ atributo de \_ puntero \] iid** es especifica el IID de la interfaz COM a la que apunta un puntero de interfaz.

``` syntax
[ iid_is(limited-expression) ]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*limited-expression* 
</dt> <dd>

Especifica una expresión de lenguaje C. El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas. MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Puede usar **\[ iid is \_ en \] listas** de atributos para parámetros de función y para miembros de estructura o unión. Los códigos auxiliares usan el IID para determinar cómo serializar el puntero de interfaz. Esto es útil para un puntero de interfaz que se escribe como un parámetro de clase base.

Los archivos que usan el **\[ atributo iid \_ is \]** deben compilarse con el compilador MIDL en modo predeterminado, que no usa el [**modificador /osf.**](-osf.md)

## <a name="examples"></a>Ejemplos

``` syntax
HRESULT    CreateInstance( 
    [in] REFIID riid, 
    [out, iid_is(riid)] IUnknown ** ppvObject);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**object**](object.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> </dl>

 

 




