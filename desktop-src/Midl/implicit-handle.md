---
title: implicit_handle atributo)
description: El atributo \ \_ ACF de identificador implícito especifica el identificador que se usa para las funciones que no incluyen un identificador explícito como parámetro de procedimiento.
ms.assetid: 09c17473-87b5-4fd6-beb9-3d9b7bc82d8c
keywords:
- implicit_handle el atributo MIDL
topic_type:
- apiref
api_name:
- implicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22f410fa048a27e1f7626690e6308de4c1a31c2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904016"
---
# <a name="implicit_handle-attribute"></a>\_atributo de identificador implícito

El atributo ACF de **\[ \_ identificador \] implícito** especifica el identificador que se usa para las funciones que no incluyen un identificador explícito como parámetro de procedimiento.

``` syntax
implicit_handle(handle-type handle-name)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*tipo de identificador* 
</dt> <dd>

Especifica el tipo de datos Handle, como el identificador de tipo base [**\_ t**](handle-t.md) o un tipo de identificador definido por el usuario.

</dd> <dt>

*identificador: nombre* 
</dt> <dd>

Especifica el nombre del identificador.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El identificador especificado por el atributo de **\[ \_ identificador \] implícito** se utiliza de maneras diferentes en función de la naturaleza del procedimiento. Si el procedimiento es remoto, el identificador se utilizará como identificador de enlace para la llamada remota. El identificador implícito también puede usarse para establecer un enlace inicial para una función que usa un identificador de contexto. Si el procedimiento es un procedimiento de serialización, el identificador se usa como un identificador de serialización que controla la operación. En el caso de la serialización de tipos, el identificador se usa como el identificador de serialización para todos los tipos serializados.

El atributo de **\[ \_ identificador \] implícito** especifica una variable global que contiene un identificador usado por cualquier función que necesite identificadores implícitos.

El tipo de identificador de enlace implícito debe ser [**Handle \_ t**](handle-t.md) (o un tipo basado en el **identificador \_ t**) o un tipo de identificador definido por el usuario especificado con el atributo [**Handle**](handle.md) . El identificador de serialización implícito debe ser un tipo basado en el **identificador \_ t**.

Si el tipo de identificador implícito no está definido en el archivo IDL o en los archivos incluidos y importados por el archivo IDL para el equipo MIDL, debe proporcionar el archivo que contiene la definición del tipo de identificador al compilar el código auxiliar. Utilice la instrucción ACF [**include**](include.md) para incluir el archivo que contiene la definición del tipo de identificador.

El atributo de **\[ \_ identificador \] implícito** puede aparecer una vez, como máximo. El atributo de **\[ \_ identificador \] implícito** solo puede producirse [**\[ \_ \]**](auto-handle.md) si no se producen los atributos de identificador automático y [**\[ \_ identificador \] explícito**](explicit-handle.md) .

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

[**\_identificador automático**](auto-handle.md)
</dt> <dt>

[**\_identificador explícito**](explicit-handle.md)
</dt> <dt>

[**identificador \_ t**](handle-t.md)
</dt> <dt>

[**inclui**](include.md)
</dt> </dl>

 

 




