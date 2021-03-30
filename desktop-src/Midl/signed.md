---
title: atributo signed
description: La palabra clave signed indica que el bit más significativo de una variable de entero representa un bit de signo en lugar de un bit de datos.
ms.assetid: 6116089a-647e-485b-8f79-9c9267aa4810
keywords:
- atributo con signo MIDL
topic_type:
- apiref
api_name:
- signed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500b87c849f31082a036d605db0947650e914bed
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103903944"
---
# <a name="signed-attribute"></a>atributo signed

La palabra clave **signed** indica que el bit más significativo de una variable de entero representa un bit de signo en lugar de un bit de datos.

``` syntax
[[ signed ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*type-qualifier* 
</dt> <dd>

Puede ser cualquiera de [**Char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)y [**Small**](small.md).

</dd> <dt>

*identificador: nombre* 
</dt> <dd>

Especifica un identificador de MIDL válido. Los identificadores de MIDL válidos constan de hasta 31 caracteres alfanuméricos o de subrayado, y deben comenzar por un carácter alfabético o de subrayado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta palabra clave es opcional y se puede usar con cualquiera de los tipos de carácter y entero [**Char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)y [**Small**](small.md). Opcionalmente, puede incluir la palabra clave [**int**](int.md) después de los calificadores de tipo **Long**, **Short** y **Small**.

Al usar el compilador MIDL [**, los tipos de carácter y**](char-idl.md)entero que aparecen en el archivo IDL sin palabras clave explícitas de signo pueden aparecer con las palabras clave **signed** o [**unsigned**](unsigned.md) en el archivo de encabezado generado. Para evitar confusiones, especifique el signo del entero y los tipos de caracteres.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**/Char**](-char.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Inter**](int.md)
</dt> <dt>

[**tal**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**pequeño**](small.md)
</dt> <dt>

[**sin signo**](unsigned.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 




