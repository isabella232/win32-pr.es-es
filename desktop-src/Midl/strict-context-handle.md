---
title: strict_context_handle atributo)
description: El atributo \ \_ \_ ACF de identificador de contexto \ STRICT establece restricciones en los identificadores de contexto.
ms.assetid: c34f9018-d519-4a75-ad6f-70d386a20817
keywords:
- strict_context_handle el atributo MIDL
topic_type:
- apiref
api_name:
- strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e66fd0754ec82de2354983e10e23ffc6329569
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995129"
---
# <a name="strict_context_handle-attribute"></a>atributo de identificador de \_ contexto estricto \_

El atributo ACF de **\[ \_ \_ identificador \] de contexto estricto** establece restricciones en los identificadores de contexto.

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

*interfaz-atributo-lista* 
</dt> <dd>

Otros atributos ACF que se aplican a la interfaz en conjunto. Los atributos válidos incluyen el [**\_ identificador automático**](auto-handle.md), el [**\_ identificador implícito**](implicit-handle.md), el [**\_ identificador explícito**](explicit-handle.md)y [**Optimize**](optimize.md), [**code**](code.md)o [**nocode**](nocode.md). Separe varios atributos con comas.

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

Nombre de la interfaz.

</dd> <dt>

*instrucciones de interface-Definition* 
</dt> <dd>

Una o más instrucciones de MIDL que definen los elementos de la [**interfaz**](interface.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Normalmente, cuando una llamada a un método de interfaz genera un identificador de contexto, ese identificador está disponible libremente para cualquier otra interfaz. Cuando use el atributo de **\[ \_ \_ identificador \] de contexto STRICT** , garantizará que los métodos de esa interfaz solo aceptarán los identificadores de contexto creados por un método de la misma interfaz. Las interfaces compiladas sin un **\[ \_ \_ identificador \] de contexto estricto** no pueden aceptar identificadores de contexto creados en interfaces compiladas con un **\[ \_ \_ \] identificador de contexto estricto**.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**codifica**](code.md)
</dt> <dt>

[Identificadores de contexto](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**\_serializar identificador de contexto \_**](context-handle-serialize.md)
</dt> <dt>

[**identificador de contexto de \_ \_ noserialización**](context-handle-noserialize.md)
</dt> <dt>

[**\_identificador explícito**](explicit-handle.md)
</dt> <dt>

[**\_identificador implícito**](implicit-handle.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**optimiz**](optimize.md)
</dt> <dt>

[escribir \_ el \_ identificador de contexto STRICT \_](type-strict-context-handle.md)
</dt> </dl>

 

 