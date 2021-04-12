---
title: handle_t atributo)
description: La \_ palabra clave handler t declara un objeto para que sea del identificador de tipo de identificador primitivo \_ t. Un identificador de enlace primitivo es un objeto de datos que la aplicación puede usar para representar el enlace.
ms.assetid: 94962ed6-5c17-43e7-853f-1e9c4b3118a7
keywords:
- handle_t el atributo MIDL
topic_type:
- apiref
api_name:
- handle_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 435dcfcf620bd33043d8c8c7d948bccd74eb4e77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358869"
---
# <a name="handle_t-attribute"></a>Handle \_ t (atributo)

La palabra clave **handler \_ t** declara un objeto para que sea del identificador de tipo de identificador primitivo **\_ t**. Un identificador de enlace primitivo es un objeto de datos que la aplicación puede usar para representar el enlace.

``` syntax
typedef RPC_BINDING_HANDLE handle_t;
```

## <a name="parameters"></a>Parámetros

Este atributo no tiene parámetros.

## <a name="remarks"></a>Observaciones

El **tipo \_ t de identificador** es uno de los tipos predefinidos del lenguaje de definición de interfaz (IDL). Puede aparecer como un especificador de tipo en declaraciones [**typedef**](typedef.md) , declaraciones generales y declaradores de función (como un especificador de tipo de valor devuelto de función y un especificador de tipo de parámetro). Para el contexto en el que aparecen los especificadores de tipo, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).

En Microsoft RPC, los parámetros de **identificador \_** de tipo t solo se pueden producir como **\[** parámetros [**in**](in.md) **\]** . Los identificadores primitivos no pueden tener el **\[** atributo [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** .

Los parámetros de **identificador \_** de tipo t (parámetros de identificador primitivo) no se transmiten en la red.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[Enlace y controladores](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**de**](in.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**espeficarse**](unique.md)
</dt> </dl>

 

 