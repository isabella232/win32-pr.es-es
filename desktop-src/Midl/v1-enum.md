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
ms.openlocfilehash: 4d7afb814cde879f0ada5124b1a19d8ac8b8c851deafcda7e75295a6e5338f68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382789"
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

## <a name="remarks"></a>Comentarios

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

[**long**](long.md)
</dt> </dl>

 

 




