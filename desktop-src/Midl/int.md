---
title: int (atributo)
description: La palabra clave int especifica un entero con signo de 32 bits en plataformas de 32 bits. En las plataformas de 16 bits, la palabra clave INT es una palabra clave opcional que puede acompañar a las palabras clave Small, Short y Long.
ms.assetid: ad6ce0ff-e87b-4701-b9d2-a69c34e0339b
keywords:
- atributo int de tipo MIDL
topic_type:
- apiref
api_name:
- int
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f916c4f03023c756b71a2e3cbb38acd9f41f1e8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783599"
---
# <a name="int-attribute"></a>int (atributo)

La palabra clave **int** especifica un entero con signo de 32 bits en plataformas de 32 bits. En las plataformas de 16 bits, la palabra clave **int** es una palabra clave opcional que puede acompañar a las palabras clave [**Small**](small.md), [**Short**](short.md)y [**Long**](long.md).

``` syntax
[ signed | unsigned ] integer-modifier [ int ] declarator-list;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Integer-modificador* 
</dt> <dd>

Especifica la palabra clave [**Small**](small.md), [**Short**](short.md), [**Long**](long.md), [**Hyper**](hyper.md), [**\_ \_ int3264**](--int3264.md)o [**\_ \_ Int64**](--int64.md), que selecciona el tamaño de los datos enteros. En las plataformas de 16 bits, el calificador de tamaño debe estar presente.

</dd> <dt>

*lista de declaradores* 
</dt> <dd>

Especifica uno o más declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. (Los declaradores de función y las declaraciones de campo de bits no se permiten en las estructuras que se transmiten en llamadas a procedimientos remotos. Estos declaradores se permiten en estructuras que no se transmiten). Separe varios declaradores con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los tipos enteros se encuentran entre los tipos base del lenguaje de definición de interfaz (IDL). Pueden aparecer como especificadores de tipo en declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como especificador de tipo de valor devuelto de función y como especificador de tipo de parámetro). Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).

Si no se proporciona ninguna especificación de signo de entero, el tipo entero tiene como valor predeterminado [**signed**](signed.md).

Los compiladores de DCE IDL no permiten que la palabra clave [**signed**](signed.md) especifique el signo de los tipos enteros. Por lo tanto, esta característica no está disponible cuando se usa el modificador [**/OSF**](-osf.md) del compilador MIDL.

Microsoft no recomienda el uso de \_ \_ int3264 para la comunicación remota si se puede evitar. Consulte el tema sobre [**\_ \_ int3264**](--int3264.md) para obtener más información sobre su uso y limitaciones.

## <a name="examples"></a>Ejemplos

``` syntax
signed short int i = 0; 
int j = i; 
typedef struct 
{ 
    small int         i1; 
    short             i2; 
    unsigned long int i3; 
} INTSIZETYPE; 
 
HRESULT MyFunc([in] long int lCount);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**enumeración**](enum.md)
</dt> <dt>

[**Thread**](hyper.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**tal**](long.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**conectado**](signed.md)
</dt> <dt>

[**pequeño**](small.md)
</dt> <dt>

[**Destructor**](struct.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**Unión**](union.md)
</dt> </dl>

 

 




