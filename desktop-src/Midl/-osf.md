---
title: Modificador /osf
description: El modificador /osf fuerza la compatibilidad estricta con OSF DCE.
ms.assetid: d94228fa-24af-43d7-9596-cf3a14690e0b
keywords:
- /osf switch MIDL
topic_type:
- apiref
api_name:
- /osf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2936401d59bb8c2c2bcfdcffce27ba9ed978d506
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159721"
---
# <a name="osf-switch"></a>Modificador /osf

El **modificador /osf** fuerza la compatibilidad estricta con OSF DCE.

``` syntax
midl /osf
```

## <a name="switch-options"></a>Cambiar opciones

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Use este modificador si la aplicación requiere una compatibilidad estricta con OSF DCE por motivos de portabilidad.

En el modo **/osf,** el paquete RpcSs se habilita automáticamente cuando se usan punteros completos, los argumentos requieren asignación de memoria o cuando se usa el atributo [**\_ enable allocate.**](enable-allocate.md) Esto significa que no tiene que proporcionar las funciones de asignación de usuario de nivel medio y libre de usuario medio en la aplicación cliente y servidor. [**\_ \_**](/windows/desktop/Rpc/the-midl-user-allocate-function) [**\_ \_**](/windows/desktop/Rpc/the-midl-user-free-function)

Las siguientes características extendidas por Microsoft no están disponibles al compilar con el **modificador /osf:**

-   Declaradores abstractos (parámetros sin nombre) en el archivo IDL.
-   Definiciones de interfaz para objetos COM.
-   Nombres de interfaz con más de 17 caracteres.
-   Atributos de solo MIDL, como las referencias de conexión, las referencias de usuario y las extensiones de la biblioteca de tipos (ODL). [**\_**](wire-marshal.md) [**\_**](user-marshal.md)
-   Usar palabras clave de ACF en un archivo IDL (la opción midl **/app \_ config).**
-   Funciones de devolución de llamada estáticas en el cliente.
-   Atributo [**asincrónico.**](async.md)
-   [**cpp \_ quote**](cpp-quote.md) y **\# pragma midl \_ echo**.
-   [**wchar \_ t**](wchar-t.md) tipos de caracteres anchos, constantes y cadenas.
-   [**inicialización de**](enum.md) enumeración (enumeradores dispersos).
-   [**out**](out-idl.md)-only size specification.
-   Punteros de tamaño mixtos y matrices de tamaño.
-   Expresiones usadas para especificadores de tamaño y discriminador.
-   Parámetros de identificador explícitos en cualquier posición de la lista de argumentos. En **el modo /osf,** el compilador midl busca un identificador de enlace explícito como primer parámetro. Cuando el primer parámetro no es un identificador de enlace y se especifican uno o varios identificadores de contexto, se usa el identificador de contexto situado más a la izquierda como identificador de enlace. Cuando el primer parámetro no es un identificador y no hay identificadores [**de \_**](implicit-handle.md) contexto, el procedimiento usa el enlace implícito mediante el identificador implícito del atributo ACF o el [**identificador \_ automático**](auto-handle.md).
-   Herencia de tipo de atributo de puntero. OSF DCE no permite punteros sin atributos. Por lo tanto, **en el modo /osf,** cada archivo IDL debe definir atributos para sus punteros. Si algún puntero no tiene un atributo explícito, [**el \_**](pointer-default.md) archivo IDL debe tener una especificación predeterminada de puntero para establecer el tipo de puntero.
-   Varias interfaces en un archivo IDL.
-   Definiciones fuera del bloque de interfaz.
-   Calificadores de tipo como **far** y **stdcall**.
-   Omitir atributos direccionales.

Las siguientes extensiones de lenguaje C/C++ no están disponibles al compilar con el **modificador /osf:**

-   Campos de bits en estructuras y uniones.
-   Comentarios de una sola línea delimitados con dos caracteres de barra diagonal (//).
-   Declaraciones externas.
-   Procedimientos con puntos suspensivos en la lista de parámetros.
-   Escriba [**int**](int.md).
-   Escriba **\* void* _ (excepto con el [atributo _ context *\_ handle).* *](context-handle.md)
-   Los calificadores de tipo, incluido el formulario con el prefijo compatible con ANSI, contienen dos caracteres de subrayado: **\_ \_ cdecl**, **cdecl**, [**const**](const.md), **const**, **\_ \_ export**, **export**, **\_ \_ far**, **far**, **\_ \_ loadds**, **loadds**, **\_ \_ near**, **near**, **\_ \_ pascal**, **\_ \_ stdcall**, **stdcall**, **\_ \_ volatile** y **volatile.** 
-   Cualquier \# [**advertencia de pragma**](pragma.md) o **\# comentario de pragma.**
-   Serialización de tipos.
-   Tipo [**\_ \_ de datos int3264.**](--int3264.md)
-   El [**modificador /protocol**](-protocol.md) y la sintaxis de transferencia band64.

## <a name="examples"></a>Ejemplos

**midl /osf filename.idl**

**midl /osf /app \_ config filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/app \_ config**](-app-config.md)
</dt> <dt>

[**/ms \_ ext**](-ms-ext.md)
</dt> <dt>

[Paquete de administración de memoria rpcss](/windows/desktop/Rpc/rpcss-memory-management-package)
</dt> </dl>

 

 