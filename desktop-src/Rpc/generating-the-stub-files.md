---
title: Generar los archivos de código auxiliar
description: Después de definir la interfaz de cliente/servidor, normalmente desarrollará los archivos de origen de cliente y servidor.
ms.assetid: e4d08bee-ab9a-4426-a1af-72a7d763797f
keywords:
- Llamada a procedimiento remoto RPC, tareas, generación de archivos de código auxiliar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e092663711be60a3a0dc0dd8a4e99c0fa92a3ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244718"
---
# <a name="generating-the-stub-files"></a>Generar los archivos de código auxiliar

Después de definir la interfaz de cliente/servidor, normalmente desarrollará los archivos de origen de cliente y servidor. A continuación, use un único archivo Make para generar los archivos de código auxiliar y de encabezado. Compile y vincule las aplicaciones cliente y servidor. Sin embargo, si esta es la primera exposición al entorno informático distribuido, es posible que quiera invocar el compilador midl ahora para ver qué genera MIDL antes de continuar. El compilador MIDL (Midl.exe) se instala automáticamente al instalar el Kit de desarrollo de software (SDK) de plataforma.

Al compilar estos archivos, asegúrese de que Hello.idl y Hello.acf se encuentran en el mismo directorio. El comando siguiente generará el archivo de encabezado Hello.h y los códigos auxiliares de cliente y servidor, Hello \_ c.c y Hello \_ s.c.

**midl hello.idl**

Observe que Hello.h contiene prototipos de función para HelloProc y Shutdown, así como declaraciones de reenvío para dos funciones de administración de memoria, **midl \_ user \_ allocate** y **midl \_ user \_ free**. Proporcionará estas dos funciones en la aplicación de servidor. Si los datos se transmiten desde el servidor al cliente (mediante un parámetro out), también tendría que proporcionar estas dos funciones de administración de memoria \[  \] en la aplicación cliente.

Tenga en cuenta las definiciones de la variable de identificador global, hello IfHandle y los nombres de identificador de interfaz de cliente y \_ servidor, hello \_ v1 \_ 0 c ifspec y \_ hello \_ \_ v1 \_ 0 \_ s \_ ifspec. Las aplicaciones cliente y servidor usarán los nombres de identificador de interfaz en llamadas en tiempo de ejecución.

En este momento, no es necesario hacer nada con los archivos de código auxiliar Hello \_ c.c y hello \_ s.c.

``` syntax
/*file: hello.h */
/* this ALWAYS GENERATED file contains the definitions for the interfaces */
/* File created by MIDL compiler version 3.00.06 
/* at Tue Feb 20 11:33:32 1996 */
/* Compiler settings for hello.idl:
    Os, W1, Zp8, env=Win32, ms_ext, c_ext
    error checks: none */
//@@MIDL_FILE_HEADING(  )
#include "Rpc.h"
#include "rpcndr.h"
 
#ifndef __hello_h_
#define __hello_h_
 
#ifdef __cplusplus
extern "C"{
#endif 
 
/* Forward Declarations */ 
 
void __RPC_FAR * __RPC_USER MIDL_user_allocate(size_t);
void __RPC_USER MIDL_user_free( void __RPC_FAR * ); 
 
#ifndef __hello_INTERFACE_DEFINED__
#define __hello_INTERFACE_DEFINED__
 
/****************************************
 * Generated header for interface: hello
 * at Tue Feb 20 11:33:32 1996
 * using MIDL 3.00.06
 ****************************************/
/* [implicit_handle][version][uuid] */ 
 
            /* size is 0 */
void HelloProc( 
    /* [string][in] */ unsigned char __RPC_FAR *pszString);
    /* size is 0 */
void Shutdown( void);
extern handle_t hello_IfHandle;
 
extern RPC_IF_HANDLE hello_v1_0_c_ifspec;
extern RPC_IF_HANDLE hello_v1_0_s_ifspec;
#endif /* __hello_INTERFACE_DEFINED__ */
 
/* Additional Prototypes for ALL interfaces */
/* end of Additional Prototypes */
#ifdef __cplusplus
}
#endif
#endif
```

 

 




