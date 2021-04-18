---
title: enum (atributo)
description: La palabra clave enum identifica un tipo enumerado.
ms.assetid: 1aaa3c36-17f7-42ff-8f4c-66133fcf4a1a
keywords:
- atributo de enumeración MIDL
topic_type:
- apiref
api_name:
- enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681244c9d852c25d8e63ad389b03f16e6db8148c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358000"
---
# <a name="enum-attribute"></a>enum (atributo)

La palabra clave **enum** identifica un tipo enumerado.

``` syntax
enum [tag ] 
{ 
    identifier [=integer-value ] 
    [ , ... ] 
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*etiqueta* 
</dt> <dd>

Especifica una etiqueta opcional para el tipo enumerado.

</dd> <dt>

*identifier* 
</dt> <dd>

Especifica la enumeración concreta.

</dd> <dt>

*valor entero:* 
</dt> <dd>

Especifica un valor entero constante.

</dd> </dl>

## <a name="remarks"></a>Observaciones

los tipos de **enumeración** pueden aparecer como especificadores de tipo en declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como function-return-type o como especificador de tipo de parámetro). Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).

En el modo predeterminado del compilador MIDL, puede asignar valores enteros a los enumeradores. (Esta característica no está disponible cuando se compila con el modificador [**/OSF**](-osf.md) ). Al igual que con los enumeradores de lenguaje C, los nombres de enumerador deben ser únicos, pero los valores del enumerador no deben ser.

Cuando no se proporcionan operadores de asignación, los identificadores se asignan a enteros consecutivos de izquierda a derecha, empezando por cero. Cuando se proporcionan operadores de asignación, los valores asignados empiezan por el valor asignado más recientemente.

El número máximo de identificadores es 65.535.

Los objetos de tipo **enum** son tipos [**int**](int.md) y su tamaño depende del sistema. De forma predeterminada, los objetos de tipos de **enumeración** se tratan como objetos de 16 bits de tipo [**Short**](short.md) [**sin signo**](unsigned.md) cuando se transmiten a través de una red. Los valores que están fuera del intervalo de 0 a 32.767 provocan que el valor de enumeración de RPC X de la excepción en tiempo de ejecución esté \_ \_ \_ \_ fuera \_ del \_ intervalo. Para transmitir objetos como entidades de 32 bits, aplique el **\[** atributo de [**\_ enumeración v1**](v1-enum.md) **\]** al typedef **enum** .

## <a name="examples"></a>Ejemplos

``` syntax
typedef enum {Monday=2, Tuesday, Wednesday, Thursday, Friday} workdays; 
 
typedef enum {Clemens=21, Palmer=22, Ryan=34} pitchers;
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Inter**](int.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**sin signo**](unsigned.md)
</dt> <dt>

[**\_enumeración v1**](v1-enum.md)
</dt> </dl>

 

 




