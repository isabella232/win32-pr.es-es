---
title: auto_handle atributo)
description: El atributo \ auto \_ Handle \ ACF indica al código auxiliar que establezca automáticamente el enlace para una función que no tenga un parámetro de control de enlace explícito. Tenga en cuenta que este atributo está obsoleto y ya no se admite.
ms.assetid: a402b933-f69b-4dfe-b0c5-b034d65d4a84
keywords:
- auto_handle el atributo MIDL
topic_type:
- apiref
api_name:
- auto_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e9a4c91fac8553867536f4f5a8c3094e0f0ff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487118"
---
# <a name="auto_handle-attribute"></a>\_atributo de control automático

El atributo ACF de **\[ \_ control \] automático** indica al código auxiliar que establezca automáticamente el enlace para una función que no tenga un parámetro de control de enlace explícito.

> [!Note]  
> Este atributo está obsoleto y ya no se admite. Se recomienda el uso del modificador [**/Robust**](-robust.md) .

 

``` syntax
[ 
    auto_handle [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*interfaz-atributo-lista* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la interfaz en conjunto, como [**código**](code.md) o [**nocode**](nocode.md). Separe los atributos de interfaz con comas.

</dd> <dt>

*nombre de interfaz* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*definición de interfaz* 
</dt> <dd>

Especifica las instrucciones IDL que forman la definición de la interfaz.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo de **\[ \_ identificador \] automático** aparece en el encabezado de la interfaz del ACF. También aparece en el encabezado de interfaz del archivo IDL cuando se especifica el modificador de compilador MIDL [**/App \_ config**](-app-config.md).

Cuando el cliente llama a una función que utiliza el enlace automático y no existe ningún enlace a un servidor, el código auxiliar establece automáticamente el enlace. El enlace se reutiliza para las llamadas posteriores a otras funciones de la interfaz que utilizan el enlace automático. El programa de aplicación cliente no tiene que declarar ni realizar ningún procesamiento relacionado con el identificador de enlace.

Cuando el ACF no está presente o no incluye el atributo de [**\[ \_ identificador \] implícito**](implicit-handle.md) , el compilador MIDL usa el **\[ \_ \] identificador automático** y emite un mensaje informativo. El compilador MIDL también utiliza el **\[ \_ identificador \] automático**, si es necesario, para establecer el enlace inicial de un [**\[ \_ identificador \] de contexto**](context-handle.md).

El atributo de **\[ \_ identificador \] automático** solo puede producirse si no se produce el [**\[ \_ identificador \] implícito**](implicit-handle.md) o el atributo de [**\[ \_ identificador \] explícito**](explicit-handle.md) . El atributo de **\[ \_ identificador \] automático** puede aparecer en el encabezado de la interfaz ACF o IDL como máximo una vez.

> [!Note]  
> No puede usar el enlace automático (ya sea con el atributo de **\[ \_ control \] automático** o de forma predeterminada) si está procesando datos a través de canalizaciones.

 

## <a name="examples"></a>Ejemplos

``` syntax
[
    auto_handle
] 
interface MyInterface 
{ 
    /* Interface definition goes here*/
} 
[
    auto_handle, 
    code
] 
interface MyInterface
{ 
    /* Interface definition goes here*/
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**configuración de/APP \_**](-app-config.md)
</dt> <dt>

[**codifica**](code.md)
</dt> <dt>

[**\_identificador explícito**](explicit-handle.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[**\_identificador implícito**](implicit-handle.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> </dl>

 

 




