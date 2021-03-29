---
title: Generar archivos de código auxiliar
description: Después de definir la interfaz cliente/servidor, normalmente desarrolla los archivos de origen de cliente y servidor.
ms.assetid: e4d08bee-ab9a-4426-a1af-72a7d763797f
keywords:
- RPC llamada a procedimiento remoto, tareas, generar archivos de código auxiliar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e092663711be60a3a0dc0dd8a4e99c0fa92a3ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903436"
---
# <a name="generating-the-stub-files"></a><span data-ttu-id="ce220-104">Generar archivos de código auxiliar</span><span class="sxs-lookup"><span data-stu-id="ce220-104">Generating the Stub Files</span></span>

<span data-ttu-id="ce220-105">Después de definir la interfaz cliente/servidor, normalmente desarrolla los archivos de origen de cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="ce220-105">After defining the client/server interface, you usually develop your client and server source files.</span></span> <span data-ttu-id="ce220-106">A continuación, use un solo archivo make para generar el código auxiliar y los archivos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="ce220-106">Next use a single makefile to generate the stub and header files.</span></span> <span data-ttu-id="ce220-107">Compile y vincule las aplicaciones de cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="ce220-107">Compile and link the client and server applications.</span></span> <span data-ttu-id="ce220-108">Sin embargo, si esta es la primera vez que se expone al entorno de computación distribuida, es posible que desee invocar el compilador MIDL ahora para ver qué genera MIDL antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="ce220-108">However, if this is your first exposure to the distributed computing environment, you may want to invoke the MIDL compiler now to see what MIDL generates before you continue.</span></span> <span data-ttu-id="ce220-109">El compilador MIDL (Midl.exe) se instala automáticamente al instalar el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="ce220-109">The MIDL compiler (Midl.exe) is automatically installed when you install the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="ce220-110">Al compilar estos archivos, asegúrese de que Hello. idl y Hello. ACF están en el mismo directorio.</span><span class="sxs-lookup"><span data-stu-id="ce220-110">When you compile these files, make sure that Hello.idl and Hello.acf are in the same directory.</span></span> <span data-ttu-id="ce220-111">El siguiente comando generará el archivo de encabezado Hello. h y los códigos auxiliares de cliente y servidor, Hello \_ c. c y Hello \_ s.c.</span><span class="sxs-lookup"><span data-stu-id="ce220-111">The following command will generate the header file Hello.h, and the client and server stubs, Hello\_c.c and Hello\_s.c.</span></span>

<span data-ttu-id="ce220-112">**Hola. idl de MIDL**</span><span class="sxs-lookup"><span data-stu-id="ce220-112">**midl hello.idl**</span></span>

<span data-ttu-id="ce220-113">Observe que Hello. h contiene prototipos de función para HelloProc y shutdown, así como declaraciones adelantadas para dos funciones de administración de memoria, la **\_ \_ asignación de usuarios de MIDL** y el usuario de **MIDL \_ \_ Free**.</span><span class="sxs-lookup"><span data-stu-id="ce220-113">Notice that Hello.h contains function prototypes for HelloProc and Shutdown, as well as forward declarations for two memory management functions, **midl\_user\_allocate** and **midl\_user\_free**.</span></span> <span data-ttu-id="ce220-114">Proporcionará estas dos funciones en la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="ce220-114">You will provide these two functions in the server application.</span></span> <span data-ttu-id="ce220-115">Si los datos se transmitieron del servidor al cliente (por medio de un parámetro de \[ **salida** \] ), también deberá proporcionar estas dos funciones de administración de memoria en la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="ce220-115">If data were being transmitted from the server to the client (by means of an \[**out**\] parameter) you would also need to provide these two memory management functions in the client application.</span></span>

<span data-ttu-id="ce220-116">Tenga en cuenta las definiciones de la variable de identificador global, Hello \_ IfHandle y el cliente y el identificador de la interfaz de servidor, Hola \_ v1 \_ 0 \_ c \_ ifspec y Hola \_ v1 \_ 0 \_ s \_ ifspec.</span><span class="sxs-lookup"><span data-stu-id="ce220-116">Note the definitions for the global handle variable, hello\_IfHandle, and the client and server interface handle names, hello\_v1\_0\_c\_ifspec and hello\_v1\_0\_s\_ifspec.</span></span> <span data-ttu-id="ce220-117">Las aplicaciones de cliente y servidor usarán los nombres de identificador de interfaz en las llamadas en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ce220-117">The client and server applications will use the interface handle names in run-time calls.</span></span>

<span data-ttu-id="ce220-118">En este momento, no es necesario hacer nada con los archivos de código auxiliar Hola \_ c. c y Hola \_ s.c.</span><span class="sxs-lookup"><span data-stu-id="ce220-118">At this point, you don't need to do anything with the stub files Hello\_c.c and hello\_s.c.</span></span>

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

 

 




