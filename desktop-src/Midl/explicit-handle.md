---
title: explicit_handle atributo)
description: El atributo \ \_ ACF de identificador explícito especifica que cada procedimiento tiene, como su primer parámetro, un identificador primitivo, como un tipo de identificador \_ t.
ms.assetid: c95d005e-dcc7-4d83-885d-91c0773c0ed8
keywords:
- explicit_handle el atributo MIDL
topic_type:
- apiref
api_name:
- explicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4fa677f1bb5a3414e6cf6dc761b83414c2d68b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105651332"
---
# <a name="explicit_handle-attribute"></a>\_atributo de identificador explícito

El \[ atributo ACF de **\_ identificador explícito** \] especifica que cada procedimiento tiene, como su primer parámetro, un identificador primitivo, como un tipo de [**identificador \_ t**](handle-t.md) .

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

*nombre de interfaz* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando se usa el atributo de **\[ \_ identificador \] explícito** , cada procedimiento tiene un identificador primitivo como primer parámetro aunque el archivo IDL no contenga este identificador en su lista de parámetros. Los prototipos emitidos para el archivo de encabezado y las rutinas de código auxiliar contienen el parámetro adicional, y ese parámetro se usa como identificador para dirigir la llamada remota.

El atributo de **\[ \_ identificador \] explícito** afecta tanto a los procedimientos remotos como a los procedimientos de serialización. Para la serialización de tipos, las rutinas de soporte se generan con el parámetro inicial como un identificador explícito (serialización). Si no se utiliza el atributo de **\[ \_ identificador \] explícito** , la aplicación puede seguir especificando que una operación tiene un identificador explícito (enlace o serialización) que dirige la llamada. Para ello, se proporciona un prototipo con un argumento que contiene un tipo de identificador al archivo IDL. Tenga en cuenta que en el modo predeterminado, un argumento que no aparece en primer lugar también se puede usar como un identificador que dirige la llamada.

Por lo tanto, mientras que el atributo de **\[ \_ identificador \] explícito** es una forma de asignar al prototipo IDL un atributo de **\[ \_ identificador \] explícito** primitivo, no requiere necesariamente un cambio en el archivo IDL. En el modo [**/OSF**](-osf.md) , solo se puede usar el primer argumento como un tipo de identificador explícito.

El atributo de **\[ \_ identificador \] explícito** se puede usar como un atributo de interfaz o un atributo de operación. Como atributo de interfaz, afecta a todas las operaciones de la interfaz y a todos los tipos que requieren compatibilidad con la serialización. Sin embargo, si se usa como atributo de operación, solo afecta a esa operación concreta. Si un método contiene uno o más \[ \] identificadores de contexto, se usa la parte más a la izquierda \[ en \] el identificador de contexto como identificador de enlace y no se crea ningún identificador explícito adicional.

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

[**\_identificador automático**](auto-handle.md)
</dt> <dt>

[**\_identificador implícito**](implicit-handle.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 




