---
title: type_strict_context_handle atributo)
description: Use el controlador de \_ contexto \ tipo STRICT \_ \_ en un archivo ACF para establecer restricciones en los identificadores de contexto.
ms.assetid: b67caad2-e87d-4eba-8555-8f347aadd515
keywords:
- type_strict_context_handle el atributo MIDL
topic_type:
- apiref
api_name:
- type_strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e16c9ae74d618b1b0cafef2c5bf618085d79284
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487558"
---
# <a name="type_strict_context_handle-attribute"></a>escribir \_ \_ atributo de identificador de contexto STRICT \_

Use el **\[ tipo \_ de \_ \_ identificador \] de contexto STRICT** en un archivo ACF para establecer restricciones en los identificadores de contexto.

``` syntax
[ 
    type_strict_context_handle 
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

Para usar este atributo, la marca-Target se debe establecer en NT60 (o superior) cuando se ejecuta midl.exe.

\[\_el tipo \_ \_ de identificador de contexto STRICT \] es un supraconjunto funcional de \[ identificador de contexto estricto \_ \_ \] . En el identificador de \[ \_ contexto estricto \_ \] , el identificador de tipo del identificador es siempre 0; en \[ \_ el identificador de contexto de tipo STRICT \_ \_ \] , el compilador MIDL asigna un identificador de tipo único.

Se recomienda usar un \[ \_ \_ identificador de contexto estricto \_ \] en lugar de \[ un \_ identificador de contexto estricto \_ \] . Los identificadores de contexto no se asocian a un tipo específico de forma predeterminada. Cuando se usan varios tipos de identificadores de contexto en el mismo proceso, es posible que un cliente malintencionado pase un identificador de contexto en lugar de otro para producir resultados no deseados. El uso del \[ \_ identificador de contexto STRICT de tipo \_ \_ \] permite a las aplicaciones aplicar la coherencia del tipo de identificador de contexto y evitar el uso del tipo de identificador de contexto no coincidente.

Un identificador de contexto con el atributo de \[ \_ identificador de \_ contexto STRICT \_ \] no se puede atribuir con un \[ identificador de contexto estricto \_ \_ \] .

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

[\_identificador de contexto estricto \_](strict-context-handle.md)
</dt> </dl>

 

 