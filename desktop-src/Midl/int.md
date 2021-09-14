---
title: atributo int
description: La palabra clave int especifica un entero de 32 bits con signo en plataformas de 32 bits. En las plataformas de 16 bits, la palabra clave int es una palabra clave opcional que puede acompaña a las palabras clave small, short y long.
ms.assetid: ad6ce0ff-e87b-4701-b9d2-a69c34e0339b
keywords:
- atributo int MIDL
topic_type:
- apiref
api_name:
- int
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f916c4f03023c756b71a2e3cbb38acd9f41f1e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159527"
---
# <a name="int-attribute"></a>atributo int

La palabra **clave int** especifica un entero de 32 bits con signo en plataformas de 32 bits. En las plataformas de 16 bits, la palabra clave **int** es una palabra clave opcional que puede acompaña a las palabras clave [**small**](small.md), [**short**](short.md)y [**long.**](long.md)

``` syntax
[ signed | unsigned ] integer-modifier [ int ] declarator-list;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*integer-modifier* 
</dt> <dd>

Especifica la palabra clave [**small**](small.md), [**short**](short.md), [**long**](long.md), [**hyper**](hyper.md), [**\_ \_ int3264**](--int3264.md)o [**\_ \_ int64**](--int64.md), que selecciona el tamaño de los datos enteros. En las plataformas de 16 bits, el calificador de tamaño debe estar presente.

</dd> <dt>

*declarator-list* 
</dt> <dd>

Especifica uno o varios declaradores de C estándar, como identificadores, declaradores de puntero y declaradores de matriz. (Los declaradores de función y las declaraciones de campo de bits no se permiten en estructuras que se transmiten en llamadas a procedimientos remotos. Estos declaradores se permiten en estructuras que no se transmiten). Separe varios declaradores con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los tipos enteros se encuentran entre los tipos base del lenguaje de definición de interfaz (IDL). Pueden aparecer como especificadores de tipo en declaraciones [**typedef,**](typedef.md) declaraciones generales y declaradores de función (como especificador function-return-type y como especificador de tipo de parámetro). Para obtener el contexto en el que aparecen los especificadores de tipo, vea [Archivo de definición de interfaz (IDL).](interface-definition-idl-file.md)

Si no se proporciona ninguna especificación de signo entero, el tipo entero tiene como valor predeterminado [**signed**](signed.md).

Los compiladores IDL de DCE no permiten que la palabra clave [**signed**](signed.md) especifique el signo de tipos enteros. Por lo tanto, esta característica no está disponible cuando se usa el modificador [**/osf**](-osf.md) del compilador midL.

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

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**hyper**](hyper.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Largo**](long.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Corto**](short.md)
</dt> <dt>

[**Firmado**](signed.md)
</dt> <dt>

[**Pequeño**](small.md)
</dt> <dt>

[**Estructura**](struct.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**union**](union.md)
</dt> </dl>

 

 




