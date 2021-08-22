---
title: strict_context_handle atributo
description: El atributo \strict \_ context \_ handle\ ACF establece restricciones en los identificadores de contexto.
ms.assetid: c34f9018-d519-4a75-ad6f-70d386a20817
keywords:
- strict_context_handle atributo MIDL
topic_type:
- apiref
api_name:
- strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db19c74efa323fa7e3abc4bfd17c14a471cbb9c81414ae78064f84bfc19fa7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013583"
---
# <a name="strict_context_handle-attribute"></a>atributo \_ strict context \_ handle

El **\[ identificador de contexto \_ estricto \_ del \]** atributo ACF establece restricciones en los identificadores de contexto.

``` syntax
[ 
    strict_context_handle 
    [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition-statements
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Otros atributos de ACF que se aplican a la interfaz en su conjunto. Entre los atributos válidos [**se incluyen el \_ identificador**](auto-handle.md)automático , [**el identificador \_ implícito,**](implicit-handle.md)el [**identificador \_**](explicit-handle.md)explícito y [**la optimización,**](optimize.md) [**el código**](code.md)o la [**codificación .**](nocode.md) Separe varios atributos con comas.

</dd> <dt>

*interface-name* 
</dt> <dd>

Nombre de la interfaz.

</dd> <dt>

*interface-definition-statements* 
</dt> <dd>

Una o varias instrucciones MIDL que definen los elementos de la [**interfaz**](interface.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Normalmente, cuando una llamada a un método de interfaz genera un identificador de contexto, ese identificador pasa a estar disponible libremente para cualquier otra interfaz. Cuando se usa el atributo **\[ strict context \_ \_ handle, \]** se garantiza que los métodos de esa interfaz solo acepten identificadores de contexto creados por un método a partir de la misma interfaz. Las interfaces compiladas sin **\[ un identificador de contexto \_ \_ estricto \]** no pueden aceptar identificadores de contexto creados en interfaces compiladas con **\[ un identificador de \_ contexto \_ estricto. \]**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Código**](code.md)
</dt> <dt>

[Identificadores de contexto](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**serialización \_ del \_ identificador de contexto**](context-handle-serialize.md)
</dt> <dt>

[**context \_ handle \_ noserialize**](context-handle-noserialize.md)
</dt> <dt>

[**identificador \_ explícito**](explicit-handle.md)
</dt> <dt>

[**identificador \_ implícito**](implicit-handle.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**Optimizar**](optimize.md)
</dt> <dt>

[identificador \_ de contexto estricto de \_ \_ tipo](type-strict-context-handle.md)
</dt> </dl>

 

 