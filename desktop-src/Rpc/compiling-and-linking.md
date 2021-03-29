---
title: Compilar y vincular
description: En el siguiente archivo make se muestran las dependencias entre los archivos necesarios para compilar las aplicaciones cliente y de servidor, y vincularlas a la biblioteca en tiempo de ejecución de RPC y la biblioteca estándar en tiempo de ejecución de C.
ms.assetid: 9182baea-7307-4db0-8d66-7fba14227ac9
keywords:
- RPC llamada a procedimiento remoto, tareas, compilación y vinculación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1991e39cc028c01066cd8f13344765787374fa08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994290"
---
# <a name="compiling-and-linking"></a><span data-ttu-id="a7c5d-104">Compilar y vincular</span><span class="sxs-lookup"><span data-stu-id="a7c5d-104">Compiling and Linking</span></span>

<span data-ttu-id="a7c5d-105">En el siguiente archivo make se muestran las dependencias entre los archivos necesarios para compilar las aplicaciones cliente y de servidor, y vincularlas a la biblioteca en tiempo de ejecución de RPC y la biblioteca estándar en tiempo de ejecución de C.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-105">The following makefile shows the dependencies among the files needed to compile the client and server applications and link them to the RPC run-time library and the standard C run-time library.</span></span>

<span data-ttu-id="a7c5d-106">Este archivo make se puede usar para compilar aplicaciones cliente y de servidor a partir del código fuente de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-106">This makefile can be used to build client and server applications from the source code in this tutorial.</span></span> <span data-ttu-id="a7c5d-107">El código auxiliar y los encabezados que se muestran aquí se generaron con la versión 2,0 de MIDL.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-107">The stubs and headers shown here were generated with MIDL version 2.0.</span></span> <span data-ttu-id="a7c5d-108">Los comandos y argumentos del compilador y del vinculador pueden ser diferentes para la configuración del equipo.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-108">The compiler and linker commands and arguments may be different for your computer configuration.</span></span> <span data-ttu-id="a7c5d-109">Consulte la documentación del compilador para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-109">See your compiler documentation for more information.</span></span>

``` syntax
#makefile for helloc.exe and hellos.exe
#link refers to the linker
#conflags refers to flags for console applications
#conlibs refers to libraries for console applications
 
!include <ntwin32.mak>
 
all : helloc hellos
 
# Make the client side application helloc
helloc : helloc.exe
helloc.exe : helloc.obj hello_c.obj
    $(link) $(linkdebug) $(conflags) -out:helloc.exe \
        helloc.obj hello_c.obj \
        rpcrt4.lib $(conlibs)
 
# helloc main program
helloc.obj : helloc.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvars) $*.c
 
# helloc stub
hello_c.obj : hello_c.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvars) $*.c
 
# Make the server side application
hellos : hellos.exe
hellos.exe : hellos.obj hellop.obj hello_s.obj
    $(link) $(linkdebug) $(conflags) -out:hellos.exe \
        hellos.obj hello_s.obj hellop.obj \
        rpcrt4.lib $(conlibsmt)
 
# hello server main program
hellos.obj : hellos.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvarsmt) $*.c
 
# remote procedures
hellop.obj : hellop.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvarsmt) $*.c
 
# hellos stub file
hello_s.obj : hello_s.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvarsmt) $*.c
 
# Stubs and header file from the IDL file
hello.h hello_c.c hello_s.c : hello.idl hello.acf
    midl hello.idl
```

 

 




