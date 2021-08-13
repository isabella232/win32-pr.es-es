---
title: atributo enum
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
ms.openlocfilehash: 1519e6208e8bccae0288d6e0b31d7897faba4e1c9c7add8987f5dd493f4f5f3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384494"
---
# <a name="enum-attribute"></a>atributo enum

La palabra **clave enum** identifica un tipo enumerado.

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

Especifica la enumeración determinada.

</dd> <dt>

*integer-value* 
</dt> <dd>

Especifica un valor entero constante.

</dd> </dl>

## <a name="remarks"></a>Comentarios

**Los tipos de** enumeración pueden aparecer como especificadores de tipo en declaraciones [**typedef,**](typedef.md) declaraciones generales y declaradores de función (ya sea como function-return-type o como un especificador de tipo de parámetro). Para obtener el contexto en el que aparecen los especificadores de tipo, vea [Archivo de definición de interfaz (IDL).](interface-definition-idl-file.md)

En el modo predeterminado del compilador MIDL, puede asignar valores enteros a enumeradores. (Esta característica no está disponible cuando se compila con el [**modificador /osf).**](-osf.md) Al igual que con los enumeradores del lenguaje C, los nombres de enumerador deben ser únicos, pero los valores del enumerador no deben ser.

Cuando no se proporcionan operadores de asignación, los identificadores se asignan a enteros consecutivos de izquierda a derecha, empezando por cero. Cuando se proporcionan operadores de asignación, los valores asignados comienzan por el valor asignado más recientemente.

El número máximo de identificadores es 65 535.

Los objetos de **tipo enum** son [**tipos int**](int.md) y su tamaño depende del sistema. De forma predeterminada, los objetos **de tipos de** enumeración se tratan como objetos de 16 bits de tipo [**unsigned**](unsigned.md) [**short**](short.md) cuando se transmiten a través de una red. Los valores fuera del intervalo de 0 a 32 767 provocan la excepción en tiempo de ejecución RPC \_ X \_ ENUM \_ VALUE OUT \_ \_ OF \_ RANGE. Para transmitir objetos como entidades de 32 bits, aplique el atributo **\[** [**\_ de enumeración v1**](v1-enum.md) a **\]** la **definición de** tipo de enumeración.

## <a name="examples"></a>Ejemplos

``` syntax
typedef enum {Monday=2, Tuesday, Wednesday, Thursday, Friday} workdays; 
 
typedef enum {Clemens=21, Palmer=22, Ryan=34} pitchers;
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**int**](int.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> <dt>

[**Enumeración \_ v1**](v1-enum.md)
</dt> </dl>

 

 




