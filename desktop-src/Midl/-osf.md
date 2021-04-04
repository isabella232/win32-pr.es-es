---
title: modificador/OSF
description: El conmutador/OSF fuerza la compatibilidad estricta con el DCE de OSF.
ms.assetid: d94228fa-24af-43d7-9596-cf3a14690e0b
keywords:
- /OSF modificador MIDL
topic_type:
- apiref
api_name:
- /osf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2936401d59bb8c2c2bcfdcffce27ba9ed978d506
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077637"
---
# <a name="osf-switch"></a>modificador/OSF

El conmutador **/OSF** fuerza la compatibilidad estricta con el DCE de OSF.

``` syntax
midl /osf
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Use este modificador si la aplicación requiere una compatibilidad estricta con OSF DCE por motivos de portabilidad.

En el modo **/OSF** , el paquete RPCSS se habilita automáticamente cuando se usan punteros completos, los argumentos requieren la asignación de memoria o cuando se usa el atributo [**enable \_ allocate**](enable-allocate.md) . Esto significa que no es necesario proporcionar las funciones de [**\_ \_ asignación**](/windows/desktop/Rpc/the-midl-user-allocate-function) de usuarios de MIDL y de [**\_ \_ usuario de MIDL**](/windows/desktop/Rpc/the-midl-user-free-function) en la aplicación de cliente y de servidor.

Las siguientes características extendidas de Microsoft no están disponibles al compilar con el modificador **/OSF** :

-   Declaradores abstractos (parámetros sin nombre) en el archivo IDL.
-   Definiciones de interfaz para objetos COM.
-   Nombres de interfaz con más de 17 caracteres.
-   Atributos de solo MIDL, como las [**\_ referencias de conexión**](wire-marshal.md), las [**\_ referencias de usuario**](user-marshal.md)y las extensiones typelib (ODL).
-   Usar palabras clave ACF en un archivo IDL (la opción de **\_ configuración/App** de MIDL).
-   Funciones de devolución de llamada estáticas en el cliente.
-   Atributo [**Async**](async.md) .
-   [**CPP \_ Quote**](cpp-quote.md) y **\# pragma MIDL \_ echo**.
-   tipos de caracteres anchos, constantes y cadenas de [**WCHAR \_ t**](wchar-t.md) .
-   inicialización de [**enumeración**](enum.md) (enumeradores dispersos).
-   Especificación de tamaño de solo [**salida**](out-idl.md).
-   Punteros de tamaño mixto y matrices de tamaño.
-   Expresiones usadas para los especificadores de tamaño y discriminador.
-   Parámetros de identificador explícitos en cualquier posición de la lista de argumentos. En el modo **/OSF** , el compilador MIDL busca un identificador de enlace explícito como primer parámetro. Cuando el primer parámetro no es un identificador de enlace y se especifican uno o más identificadores de contexto, se usa el identificador de contexto situado más a la izquierda como identificador de enlace. Cuando el primer parámetro no es un identificador y no hay identificadores de contexto, el procedimiento utiliza el enlace implícito mediante el [**\_ identificador implícito**](implicit-handle.md) del atributo ACF o el [**\_ identificador automático**](auto-handle.md).
-   Herencia de tipos de atributos de puntero. OSF DCE no permite punteros sin atributos. Por lo tanto, en el modo **/OSF** cada archivo IDL debe definir atributos para sus punteros. Si un puntero no tiene un atributo explícito, el archivo IDL debe tener una especificación [**\_ predeterminada de puntero**](pointer-default.md) para establecer el tipo de puntero.
-   Varias interfaces en un archivo IDL.
-   Definiciones fuera del bloque de interfaz.
-   Calificadores de tipo, como **Far** y **Stdcall**.
-   Omitir atributos direccionales.

Las siguientes extensiones del lenguaje C/C++ no están disponibles al compilar con el modificador **/OSF** :

-   Campos de bits en estructuras y uniones.
-   Comentarios de una sola línea delimitados con dos caracteres de barra diagonal (//).
-   Declaraciones externas.
-   Procedimientos con puntos suspensivos en la lista de parámetros.
-   Escriba [**int**](int.md).
-   Escriba **void \*** (excepto con el atributo de [**\_ identificador de contexto**](context-handle.md) ).
-   Los calificadores de tipo, incluido el formulario con el prefijo compatible con ANSI, contienen dos caracteres de subrayado: **\_ \_ Cdecl**, **Cdecl**, [**const**](const.md), **const**, **\_ \_ Export**, **Export**, **\_ \_ Far**, **Far**, **\_ \_ loadds**, **loadds**, **\_ \_ Near**, **Near**, **\_ \_ Pascal**, **Pascal**, **\_ \_ Stdcall**, **Stdcall**, **\_ \_ volatile** y **volatile**.
-   Cualquier \# Advertencia [**pragma**](pragma.md) o comentario **\# pragma** .
-   Serialización de tipo.
-   El tipo de datos [**\_ \_ int3264**](--int3264.md) .
-   El modificador [**/Protocolo**](-protocol.md) y la sintaxis de transferencia ndr64.

## <a name="examples"></a>Ejemplos

**MIDL/OSF nombrearchivo. idl**

**MIDL/OSF/APP \_ config nombreDeArchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**configuración de/APP \_**](-app-config.md)
</dt> <dt>

[**\_ext/MS**](-ms-ext.md)
</dt> <dt>

[Paquete de administración de memoria RPCSS](/windows/desktop/Rpc/rpcss-memory-management-package)
</dt> </dl>

 

 