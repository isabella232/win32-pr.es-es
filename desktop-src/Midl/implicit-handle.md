---
title: implicit_handle atributo
description: El atributo \ implicit handle\ ACF especifica el identificador utilizado para las funciones que no incluyen un identificador \_ explícito como parámetro de procedimiento.
ms.assetid: 09c17473-87b5-4fd6-beb9-3d9b7bc82d8c
keywords:
- implicit_handle atributo MIDL
topic_type:
- apiref
api_name:
- implicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22f410fa048a27e1f7626690e6308de4c1a31c2a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159541"
---
# <a name="implicit_handle-attribute"></a>atributo \_ de identificador implícito

El **\[ atributo \_ \]** ACF del identificador implícito especifica el identificador utilizado para las funciones que no incluyen un identificador explícito como parámetro de procedimiento.

``` syntax
implicit_handle(handle-type handle-name)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*handle-type* 
</dt> <dd>

Especifica el tipo de datos de identificador, como el identificador de tipo base [**\_ t**](handle-t.md) o un tipo de identificador definido por el usuario.

</dd> <dt>

*handle-name* 
</dt> <dd>

Especifica el nombre del identificador.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El identificador especificado por el **\[ atributo de identificador \_ \] implícito** se usa de maneras diferentes en función de la naturaleza del procedimiento. Si el procedimiento es remoto, el identificador se usará como identificador de enlace para la llamada remota. El identificador implícito también se puede usar para establecer un enlace inicial para una función que usa un identificador de contexto. Si el procedimiento es un procedimiento de serialización, el identificador se usa como identificador de serialización que controla la operación. En el caso de la serialización de tipos, el identificador se usa como identificador de serialización para todos los tipos serializados.

El **\[ atributo de \_ identificador \]** implícito especifica una variable global que contiene un identificador utilizado por cualquier función que necesite identificadores implícitos.

El tipo de identificador de enlace implícito debe ser [**\_ handle t**](handle-t.md) (o un tipo basado en handle **\_ t)** o un tipo de identificador definido por el usuario especificado con el [**atributo handle.**](handle.md) El identificador de serialización implícita debe ser un tipo basado en **el \_ identificador t**.

Si el tipo de identificador implícito no está definido en el archivo IDL o en los archivos incluidos e importados por el archivo IDL para el equipo MIDL, debe proporcionar el archivo que contiene la definición de tipo de identificador al compilar los códigos auxiliares. Use la instrucción [**include**](include.md) de ACF para incluir el archivo que contiene la definición de tipo de identificador.

El **\[ atributo de \_ identificador \]** implícito puede producirse una vez, como máximo. El **\[ atributo de \_ identificador \]** implícito solo puede [**\[ \_ \]**](explicit-handle.md) [**\[ \_ \]**](auto-handle.md) producirse si no se producen los atributos de identificador automático y de identificador explícito.

## <a name="examples"></a>Ejemplos

``` syntax
/* ACF file */ 
[
    implicit_handle(handle_t hMyHandle)
] 
interface iface
{ 
    // Attribute configuration statements
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**identificador \_ automático**](auto-handle.md)
</dt> <dt>

[**identificador \_ explícito**](explicit-handle.md)
</dt> <dt>

[**handle \_ t**](handle-t.md)
</dt> <dt>

[**incluír**](include.md)
</dt> </dl>

 

 




