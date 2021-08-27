---
title: type_strict_context_handle atributo
description: Use \type \_ strict \_ context \_ handle\ en un archivo ACF para establecer restricciones en los identificadores de contexto.
ms.assetid: b67caad2-e87d-4eba-8555-8f347aadd515
keywords:
- type_strict_context_handle atributo MIDL
topic_type:
- apiref
api_name:
- type_strict_context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7e10c6231ac41287a08df7b9a0fa4e5361eddec9eb72bb6059b9f00dea5106
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105625"
---
# <a name="type_strict_context_handle-attribute"></a>Atributo de \_ identificador de contexto strict de \_ \_ tipo

Use el **\[ identificador de contexto strict \_ de \_ \_ tipo \]** en un archivo ACF para establecer restricciones en los identificadores de contexto.

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

Para usar este atributo, la marca -target debe establecerse en NT60 (o superior) al ejecutar midl.exe.

\[el \_ identificador de contexto estricto de tipo es un \_ \_ \] superconjunto funcional de \[ identificador de contexto \_ \_ \] estricto. En el identificador de contexto estricto , el identificador de tipo del identificador siempre es 0; en el identificador de contexto estricto de tipo , el compilador MIDL asigna un identificador de \[ \_ tipo \_ \] \[ \_ \_ \_ \] único.

Se recomienda usar el identificador \[ de contexto estricto de tipo en lugar del identificador de \_ contexto estricto \_ \_ \] \[ \_ \_ \] . Los identificadores de contexto no están asociados a un tipo específico de forma predeterminada. Cuando se usan varios tipos de identificadores de contexto en el mismo proceso, es posible que un cliente malintencionado pase un identificador de contexto en lugar de otro para generar resultados no deseados. El uso del identificador de contexto estricto de tipo permite a las aplicaciones aplicar la coherencia del tipo de identificador de contexto y evitar cualquier uso de tipos de identificador de \[ \_ contexto no \_ \_ \] coincidentes.

Un identificador de contexto atribuido con \[ el identificador de contexto estricto de tipo tampoco se puede atribuir con un identificador \_ de contexto \_ \_ \] \[ \_ \_ \] estricto.

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

[control \_ de contexto \_ estricto](strict-context-handle.md)
</dt> </dl>

 

 