---
title: handle_t atributo
description: La palabra clave handle t declara que un objeto es del identificador de \_ tipo de identificador primitivo \_ t. Un identificador de enlace primitivo es un objeto de datos que la aplicación puede usar para representar el enlace.
ms.assetid: 94962ed6-5c17-43e7-853f-1e9c4b3118a7
keywords:
- handle_t atributo MIDL
topic_type:
- apiref
api_name:
- handle_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 435dcfcf620bd33043d8c8c7d948bccd74eb4e77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159571"
---
# <a name="handle_t-attribute"></a>atributo \_ handle t

La **palabra clave handle \_ t** declara que un objeto es del identificador de tipo de **identificador primitivo \_ t**. Un identificador de enlace primitivo es un objeto de datos que la aplicación puede usar para representar el enlace.

``` syntax
typedef RPC_BINDING_HANDLE handle_t;
```

## <a name="parameters"></a>Parámetros

Este atributo no tiene parámetros.

## <a name="remarks"></a>Observaciones

El **tipo de identificador \_ t** es uno de los tipos predefinidos del lenguaje de definición de interfaz (IDL). Puede aparecer como un especificador de tipo en declaraciones [**typedef,**](typedef.md) declaraciones generales y declaradores de función (como un especificador function-return-type y un especificador de tipo de parámetro). Para obtener el contexto en el que aparecen los especificadores de tipo, vea [Archivo de definición de interfaz (IDL).](interface-definition-idl-file.md)

En RPC de Microsoft, los parámetros de **tipo \_ handle t** solo se pueden producir como en **\[** [**los**](in.md) **\]** parámetros. Los identificadores primitivos no pueden **\[** [**tener el**](unique.md) **\]** atributo único o **\[** [**ptr.**](ptr.md) **\]**

Los parámetros del **identificador de \_ tipo t** (parámetros de identificador primitivos) no se transmiten en la red.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[Enlace y identificadores](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**En**](in.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**Único**](unique.md)
</dt> </dl>

 

 