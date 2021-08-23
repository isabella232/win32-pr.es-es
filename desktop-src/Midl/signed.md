---
title: atributo signed
description: La palabra clave signed indica que el bit más significativo de una variable de entero representa un bit de signo en lugar de un bit de datos.
ms.assetid: 6116089a-647e-485b-8f79-9c9267aa4810
keywords:
- atributo firmado MIDL
topic_type:
- apiref
api_name:
- signed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f3db15bc46d6d8ab3ec108c648d094ebf706d9286a8c4b0a823fa409e118e3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641343"
---
# <a name="signed-attribute"></a>atributo signed

La **palabra clave signed** indica que el bit más significativo de una variable de entero representa un bit de signo en lugar de un bit de datos.

``` syntax
[[ signed ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*type-qualifier* 
</dt> <dd>

Puede ser cualquiera de [**char,**](char-idl.md) [**wchar \_ t,**](wchar-t.md) [**long,**](long.md) [**short**](short.md)y [**small.**](small.md)

</dd> <dt>

*identifier-name* 
</dt> <dd>

Especifica un identificador MIDL válido. Los identificadores MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado y deben comenzar con un carácter alfabético o de subrayado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta palabra clave es opcional y se puede usar con cualquiera de los tipos de caracteres y enteros [**char**](char-idl.md), [**wchar \_ t**](wchar-t.md), [**long**](long.md), [**short**](short.md)y [**small**](small.md). Opcionalmente, puede incluir la palabra clave [**int**](int.md) después de los calificadores de tipo **long**, **short** y **small**.

Cuando se usa el modificador del compilador MIDL [**char**](char-idl.md), los tipos de caracteres y enteros que aparecen en el archivo IDL sin palabras clave de signo explícitas pueden aparecer con las palabras clave **signed** o [**unsigned**](unsigned.md) en el archivo de encabezado generado. Para evitar confusiones, especifique el signo de los tipos de entero y carácter.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**/char**](-char.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**Pequeño**](small.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> <dt>

[**wchar \_ t**](wchar-t.md)
</dt> </dl>

 

 




