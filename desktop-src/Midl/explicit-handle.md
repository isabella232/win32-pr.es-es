---
title: explicit_handle atributo
description: El atributo \ explicit handle\ ACF especifica que cada procedimiento tiene, como primer parámetro, un identificador primitivo, como un \_ tipo t de \_ identificador.
ms.assetid: c95d005e-dcc7-4d83-885d-91c0773c0ed8
keywords:
- explicit_handle atributo MIDL
topic_type:
- apiref
api_name:
- explicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13b50aa69c43e27b4797f6619b4efa14b90f16dd2b4bee45df2db6b708e58f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013923"
---
# <a name="explicit_handle-attribute"></a>atributo \_ de identificador explícito

El atributo ACF del identificador explícito especifica que cada procedimiento tiene, como primer parámetro, un identificador primitivo, como un \[ **\_** \] tipo t [**de \_**](handle-t.md) identificador.

``` syntax
[
    explicit_handle
] 
interface interface-name
{
    ...
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*interface-name* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Cuando se usa el **\[ atributo \_ de \]** identificador explícito, cada procedimiento tiene un identificador primitivo como primer parámetro, incluso si el archivo IDL no contiene este identificador en su lista de parámetros. Los prototipos emitidos al archivo de encabezado y a las rutinas de código auxiliar contienen el parámetro adicional y ese parámetro se usa como identificador para dirigir la llamada remota.

El **\[ atributo de \_ identificador \]** explícito afecta tanto a los procedimientos remotos como a los procedimientos de serialización. Para la serialización de tipos, las rutinas de compatibilidad se generan con el parámetro inicial como un identificador explícito (serialización). Si no **\[ se usa \_ el \]** atributo de identificador explícito, la aplicación todavía puede especificar que una operación tenga un identificador explícito (enlace o serialización) que dirija la llamada. Para ello, se proporciona un prototipo con un argumento que contiene un tipo de identificador al archivo IDL. Tenga en cuenta que, en el modo predeterminado, un argumento que no aparece primero también se puede usar como identificador que dirige la llamada.

Por lo tanto, aunque el atributo **\[ \_ de \]** identificador explícito es una manera de proporcionar al prototipo de IDL **\[ \_ \]** un atributo de identificador explícito primitivo, no requiere necesariamente un cambio en el archivo IDL. En [**el modo /osf,**](-osf.md) solo se puede usar el primer argumento como un tipo de identificador explícito.

El **\[ atributo \_ de \]** identificador explícito se puede usar como atributo de interfaz o como atributo de operación. Como atributo de interfaz, afecta a todas las operaciones de la interfaz y a todos los tipos que requieren compatibilidad con la serialización. Sin embargo, si se usa como atributo de operación, solo afecta a esa operación determinada. Si un método contiene uno o varios identificadores de contexto, el identificador de contexto más a la izquierda se usa como identificador de enlace y no se crea ningún identificador \[ \] explícito \[ \] adicional.

## <a name="examples"></a>Ejemplos

``` syntax
/* ACF File */ 
[
    explicit_handle
] 
interface iface
{ 
    // Interface definition statements.
};
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**identificador \_ automático**](auto-handle.md)
</dt> <dt>

[**identificador \_ implícito**](implicit-handle.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 




