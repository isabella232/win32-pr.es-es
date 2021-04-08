---
title: Macros de portabilidad (RPC. h)
description: Las herramientas de RPC logran el modelo, la llamada y la independencia de la Convención de nomenclatura al asociar los tipos de datos y los tipos de valor devueltos en los archivos de código auxiliar y los archivos de encabezado generados con definiciones que son específicas de cada plataforma.
ms.assetid: 94de1138-5a84-41d8-bf88-97f0ac630f5f
keywords:
- Macros de portabilidad RPC
topic_type:
- apiref
api_name:
- Portability Macros
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c184365496db7757524a12f1b0807c3c53e24b27
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104003297"
---
# <a name="portability-macros"></a>Macros de portabilidad

Las herramientas de RPC logran el modelo, la llamada y la independencia de la Convención de nomenclatura al asociar los tipos de datos y los tipos de valor devueltos en los archivos de código auxiliar y los archivos de encabezado generados con definiciones que son específicas de cada plataforma. Estas definiciones de macro garantizan que todos los tipos de datos y funciones que requieran la designación de **\_ \_ Far** se especifiquen como objetos Far.

La siguiente ilustración muestra las definiciones de macro que el compilador MIDL aplica a las llamadas de función entre los componentes RPC:

![Diagrama que muestra las definiciones de macros MIDL se aplica a las llamadas a funciones.](images/prog-a29.png)

Las macros RPC se definen como se indica a continuación.



| Definición    | Descripción                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| \_\_API de RPC \_  | Se aplica a las llamadas realizadas por el código auxiliar a la aplicación de usuario. Ambas funciones se encuentran en el mismo programa ejecutable.                                       |
| \_\_extremo de RPC \_  | Se aplica a la definición de macro estándar para los punteros. Esta definición de macro debe aparecer como parte de la firma de todas las funciones proporcionadas por el usuario. |
| \_\_\_código auxiliar de RPC | Se aplica a las llamadas realizadas desde la biblioteca en tiempo de ejecución al código auxiliar. Estas llamadas se pueden considerar privadas.                                                 |
| \_\_\_usuario RPC | Se aplica a las llamadas realizadas por la biblioteca en tiempo de ejecución a la aplicación de usuario. Estos cruzan el límite entre un archivo DLL y una aplicación.                   |
| \_entrada RPC    | Se aplica a las llamadas realizadas por la aplicación o el código auxiliar a la biblioteca en tiempo de ejecución. Esta definición de macro se aplica a todas las funciones de tiempo de ejecución de RPC.           |



 

Para vincular correctamente las bibliotecas en tiempo de ejecución de Microsoft RPC, los códigos auxiliares y las rutinas de soporte técnico, algunas funciones proporcionadas por el usuario también deben incluir estas macros en la definición de función. Use la **\_ \_ \_ API de RPC** de macros al definir las funciones asociadas a la administración de memoria, identificadores de enlace definidos por el usuario y el atributo **transmitir \_ como** , y use la macro **\_ \_ RPC \_ User** cuando defina la rutina de ejecución de contexto asociada al identificador de contexto. Especifique las funciones como:

<dl> <dt>

<span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_\_Asignación de *\_ usuarios de MIDL* de usuario RPC \_ (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_Usuario de RPC \_ usuario de *MIDL \_* \_ gratis (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_\_Enlace de *handletype* de usuario de RPC \_ (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_Handletype de usuario de RPC \_  \_ Desenlazar (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_\_ *Tipo* de usuario RPC \_ a \_ local
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_\_ *Tipo* de usuario RPC \_ de \_ local
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_\_Tipo de usuario RPC \_ para la \_ transmisión (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_\_ *Tipo* de usuario RPC \_ de \_ transmisión (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_\_ *Tipo* de usuario RPC \_ gratis \_ local
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_\_Inst. de *tipo* de usuario RPC \_ \_ (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_\_Transmisión gratuita del *tipo* de usuario RPC \_ \_ (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_Detención de contexto de usuario de RPC \_ \_ (...)
</dt> <dd></dd> </dl>

> [!Note]  
> Todos los parámetros de puntero en estas funciones se deben especificar mediante la macro **\_ \_ RPC \_ Far**.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>RPC. h</dt> </dl> |



 

 





