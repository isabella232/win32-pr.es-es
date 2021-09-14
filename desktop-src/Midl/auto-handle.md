---
title: auto_handle atributo
description: 'El atributo \ auto handle\ ACF dirige el código auxiliar para establecer automáticamente el enlace para una función que no tiene un parámetro de identificador \_ de enlace explícito. Nota: Este atributo está obsoleto y ya no se admite.'
ms.assetid: a402b933-f69b-4dfe-b0c5-b034d65d4a84
keywords:
- auto_handle atributo MIDL
topic_type:
- apiref
api_name:
- auto_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e9a4c91fac8553867536f4f5a8c3094e0f0ff9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159673"
---
# <a name="auto_handle-attribute"></a>atributo \_ de identificador automático

El **\[ atributo \_ \]** ACF del identificador automático dirige el código auxiliar para establecer automáticamente el enlace de una función que no tiene un parámetro de identificador de enlace explícito.

> [!Note]  
> Este atributo está obsoleto y ya no se admite. Se recomienda el uso del modificador [**/robust.**](-robust.md)

 

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

*interface-attribute-list* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la interfaz como un todo, como [**código**](code.md) o [**codificación**](nocode.md). Separe los atributos de interfaz con comas.

</dd> <dt>

*interface-name* 
</dt> <dd>

Especifica el nombre de la interfaz.

</dd> <dt>

*interface-definition* 
</dt> <dd>

Especifica instrucciones IDL que forman la definición de la interfaz .

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ atributo de \_ identificador \]** automático aparece en el encabezado de interfaz del ACF. También aparece en el encabezado de interfaz del archivo IDL cuando se especifica el modificador del compilador MIDL [**/app \_ config**](-app-config.md).

Cuando el cliente llama a una función que usa el enlace automático y no existe ningún enlace a un servidor, el código auxiliar establece automáticamente el enlace. El enlace se reutiliza para las llamadas posteriores a otras funciones de la interfaz que usan el enlace automático. El programa de aplicación cliente no tiene que declarar ni realizar ningún procesamiento relacionado con el identificador de enlace.

Cuando el ACF no está presente [**\[ \_ \]**](implicit-handle.md) o no incluye el atributo de identificador implícito, el compilador midL **\[ \_ \]** usa el identificador automático y emite un mensaje informativo. El compilador MIDL también usa **\[ el identificador \_ automático \]**, si es necesario, para establecer el enlace inicial para un [**\[ identificador de \_ contexto \]**](context-handle.md).

El **\[ atributo de \_ identificador \]** automático solo puede producirse si no se produce el identificador [**\[ \_ \]**](explicit-handle.md) [**\[ \_ \] implícito**](implicit-handle.md) o el atributo de identificador explícito. El **\[ atributo de \_ identificador \]** automático puede producirse en el encabezado de interfaz ACF o IDL como máximo una vez.

> [!Note]  
> No puede usar el enlace automático (ya sea con el atributo **\[ \_ de identificador \]** automático o de forma predeterminada) si está procesando datos a través de canalizaciones.

 

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

[**/app \_ config**](-app-config.md)
</dt> <dt>

[**Código**](code.md)
</dt> <dt>

[**identificador \_ explícito**](explicit-handle.md)
</dt> <dt>

[**identificador de \_ contexto**](context-handle.md)
</dt> <dt>

[**identificador \_ implícito**](implicit-handle.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> </dl>

 

 




