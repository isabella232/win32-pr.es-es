---
title: v1_enum (atributo)
description: El atributo \ v1 \_ enum \ indica que el tipo enumerado especificado se transmitirá como una entidad de 32 bits, en lugar del valor predeterminado de 16 bits.
ms.assetid: 46016131-b78e-4a7f-94c8-41ff1780b0b8
keywords:
- v1_enum el atributo MIDL
topic_type:
- apiref
api_name:
- v1_enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8183b8b91c4a061e6b91c67ab83bca6393751f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904121"
---
# <a name="v1_enum-attribute"></a>V1 ( \_ atributo de enumeración)

El atributo de **\[ \_ enumeración \] v1** indica que el tipo enumerado especificado se transmitirá como una entidad de 32 bits, en lugar del valor predeterminado de 16 bits.

``` syntax
[v1_enum] enum 
{
    ...
};
```

## <a name="parameters"></a>Parámetros

Este atributo no tiene parámetros.

## <a name="remarks"></a>Observaciones

El uso del atributo de **\[ \_ enumeración \] v1** para transmitir un tipo enumerado como una entidad de 32 bits aumenta la eficacia de la serialización y la desserialización de datos cuando una enumeración de este tipo se incrusta en estructuras o uniones.

Para mejorar el rendimiento, se recomienda aplicar el atributo de **\[ \_ enumeración \] v1** a los enumeradores de las aplicaciones de 32 bits. Sin embargo, tenga en cuenta que en las plataformas de 16 bits el compilador de C trata un tipo enumerado como un [**int**](int.md)de 16 bits. Por lo tanto, las aplicaciones cliente de 16 bits deben convertir los tipos de [**enumeración**](enum.md) en [**Long**](long.md) para la transmisión remota con el fin de evitar sobrescribir los datos o enviar valores incorrectos.

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

[**enumeración**](enum.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**tal**](long.md)
</dt> </dl>

 

 




