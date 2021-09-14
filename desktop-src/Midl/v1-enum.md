---
title: v1_enum (atributo)
description: El atributo \v1 enum\ indica que el tipo enumerado especificado se transmite como una entidad de 32 bits, en lugar del valor predeterminado de \_ 16 bits.
ms.assetid: 46016131-b78e-4a7f-94c8-41ff1780b0b8
keywords:
- v1_enum atributo MIDL
topic_type:
- apiref
api_name:
- v1_enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8183b8b91c4a061e6b91c67ab83bca6393751f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159325"
---
# <a name="v1_enum-attribute"></a>Atributo \_ de enumeración v1

El **\[ atributo \_ \] de enumeración v1** indica que el tipo enumerado especificado se transmite como una entidad de 32 bits, en lugar del valor predeterminado de 16 bits.

``` syntax
[v1_enum] enum 
{
    ...
};
```

## <a name="parameters"></a>Parámetros

Este atributo no tiene parámetros.

## <a name="remarks"></a>Observaciones

El uso del atributo **\[ \_ \] de** enumeración v1 para transmitir un tipo enumerado como una entidad de 32 bits aumenta la eficacia de serializar y desmarque de datos cuando dicha enumeración se incrusta en estructuras o uniones.

Para mejorar el rendimiento, se recomienda aplicar el atributo **\[ \_ \] de enumeración v1** a enumeradores en aplicaciones de 32 bits. Sin embargo, tenga en cuenta que, en plataformas de 16 bits, el compilador de C trata un tipo enumerado como un valor int de 16 [**bits.**](int.md) Por lo tanto, las aplicaciones [](enum.md) cliente de 16 bits deben convertir los tipos de enumeración en [**long**](long.md) para la transmisión remota con el fin de evitar sobrescribir datos o enviar valores incorrectos.

## <a name="examples"></a>Ejemplos

``` syntax
typedef [v1_enum] enum 
{
    value1, 
    value2, ...
};
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Enum**](enum.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Largo**](long.md)
</dt> </dl>

 

 




