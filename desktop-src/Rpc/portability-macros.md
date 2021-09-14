---
title: Macros de portabilidad (Rpc.h)
description: Las herramientas RPC logran la independencia de modelo, llamada y convención de nomenclatura mediante la asociación de tipos de datos y tipos de valor devuelto de función en los archivos de código auxiliar generados y archivos de encabezado con definiciones específicas de cada plataforma.
ms.assetid: 94de1138-5a84-41d8-bf88-97f0ac630f5f
keywords:
- RPC de macros de portabilidad
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161033"
---
# <a name="portability-macros"></a>Macros de portabilidad

Las herramientas RPC logran la independencia de modelo, llamada y convención de nomenclatura mediante la asociación de tipos de datos y tipos de valor devuelto de función en los archivos de código auxiliar generados y archivos de encabezado con definiciones específicas de cada plataforma. Estas definiciones de macro garantizan que los tipos de datos y las funciones que requieren la designación de lejos se especifican como objetos lejos. **\_ \_**

En la ilustración siguiente se muestran las definiciones de macro que el compilador MIDL aplica a las llamadas de función entre componentes RPC:

![Diagrama que muestra las definiciones de macros que MIDL se aplica a las llamadas de función.](images/prog-a29.png)

Las macros RPC se definen como se muestra a continuación.



| Definición    | Descripción                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| \_\_\_API de RPC  | Se aplica a las llamadas realizadas por el código auxiliar a la aplicación de usuario. Ambas funciones están en el mismo programa ejecutable.                                       |
| \_\_RPC \_ FAR  | Se aplica a la definición de macro estándar para punteros. Esta definición de macro debe aparecer como parte de la firma de todas las funciones proporcionadas por el usuario. |
| \_\_CÓDIGO AUXILIAR \_ DE RPC | Se aplica a las llamadas realizadas desde la biblioteca en tiempo de ejecución al código auxiliar. Estas llamadas se pueden considerar privadas.                                                 |
| \_\_USUARIO \_ RPC | Se aplica a las llamadas realizadas por la biblioteca en tiempo de ejecución a la aplicación de usuario. Cruzan el límite entre un archivo DLL y una aplicación.                   |
| ENTRADA \_ RPC    | Se aplica a las llamadas realizadas por la aplicación o el código auxiliar a la biblioteca en tiempo de ejecución. Esta definición de macro se aplica a todas las funciones en tiempo de ejecución de RPC.           |



 

Para vincular correctamente con las bibliotecas en tiempo de ejecución, los códigos auxiliares y las rutinas de compatibilidad de RPC de Microsoft, algunas funciones proporcionadas por el usuario también deben incluir estas macros en la definición de función. Use la API RPC de **\_ \_ \_ macro** al definir las funciones asociadas a la administración de memoria, los identificadores de enlace definidos por el usuario y el atributo **de \_** transmisión como, y use la macro **\_ \_ RPC \_ USER** al definir la rutina de ejecución de contexto asociada al identificador de contexto. Especifique las funciones como:

<dl> <dt>

<span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_Rpc \_ USER *midl \_ user* \_ allocate(...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_RPC \_ USER *midl \_ user* \_ free(...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_Rpc \_ USER *handletype* \_ bind(...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_Rpc \_ USER *handletype* \_ unbind(...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_TIPO DE USUARIO DE RPC \_  \_ en \_ local
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_Tipo DE USUARIO DE RPC \_  \_ de \_ local
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_Rpc \_ USER type to \_ \_ xmit(...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_Tipo \_ DE USUARIO *RPC* \_ de \_ xmit(...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_RPC \_ USER escribe *local* \_ \_ gratis
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_RPC \_ USER *escribe* \_ free \_ inst(...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_RPC \_ USER *type* \_ free \_ xmit(...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_Informe de contexto de RPC \_ \_ USER(...)
</dt> <dd></dd> </dl>

> [!Note]  
> Todos los parámetros de puntero de estas funciones deben especificarse mediante la macro **\_ \_ RPC \_ FAR**.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Rpc.h</dt> </dl> |



 

 





