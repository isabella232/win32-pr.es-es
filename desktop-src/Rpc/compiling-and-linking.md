---
title: Compilación y vinculación
description: El siguiente archivo Make muestra las dependencias entre los archivos necesarios para compilar las aplicaciones cliente y servidor y vincularlas a la biblioteca en tiempo de ejecución rpc y a la biblioteca en tiempo de ejecución de C estándar.
ms.assetid: 9182baea-7307-4db0-8d66-7fba14227ac9
keywords:
- Llamada a procedimiento remoto RPC, tareas, compilación y vinculación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2500a763db149eca914060dd7920548883fa57fbd5642485a41f5a55c65cd2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931718"
---
# <a name="compiling-and-linking"></a>Compilación y vinculación

El siguiente archivo Make muestra las dependencias entre los archivos necesarios para compilar las aplicaciones cliente y servidor y vincularlas a la biblioteca en tiempo de ejecución rpc y a la biblioteca en tiempo de ejecución de C estándar.

Este archivo Make se puede usar para compilar aplicaciones cliente y servidor a partir del código fuente de este tutorial. Los códigos auxiliares y los encabezados que se muestran aquí se generaron con MIDL versión 2.0. Los comandos y argumentos del compilador y del vinculador pueden ser diferentes para la configuración del equipo. Consulte la documentación del compilador para obtener más información.

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

 

 




