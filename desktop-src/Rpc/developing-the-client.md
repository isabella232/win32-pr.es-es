---
title: Desarrollo del cliente
description: Desarrollar un programa cliente RPC es similar al desarrollo del programa de servidor. Para obtener información sobre el desarrollo de un programa de servidor RPC, vea Desarrollo del servidor.
ms.assetid: 92276326-d478-479e-8fa4-02a2fce58eb6
keywords:
- Llamada a procedimiento remoto RPC, tareas, desarrollo del cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fccc719d724ecdcc5631c5f72c5190870f864e06affd45bcce3e7f2da79fb709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021905"
---
# <a name="developing-the-client"></a>Desarrollo del cliente

Desarrollar un programa cliente RPC es similar al desarrollo del programa de servidor. Para obtener información sobre el desarrollo de un programa de servidor RPC, vea [Desarrollar el servidor](developing-the-server.md).

Al igual que en el desarrollo del servidor, el programa cliente debe incluir el archivo de encabezado que el compilador MIDL genera a partir del archivo .idl. El compilador midl también genera un archivo de código fuente de C que contiene el código auxiliar del cliente. Debe compilar este archivo de código fuente de C y vincularlo al programa cliente. (Además, el compilador MIDL genera un archivo de código fuente de C que contiene el código auxiliar del servidor, pero eso no es pertinente para esta explicación).

Además de compilar y vincular el código auxiliar de cliente con los archivos de programa, debe vincular la biblioteca de importación (y cualquier otra biblioteca que necesite el programa cliente) al programa cliente. El proceso de creación de un programa cliente RPC se ilustra en el diagrama siguiente.

![proceso de creación de un programa cliente para una aplicación distribuida](images/clntdev.png)

En el ejemplo de la ilustración anterior se muestra la creación de un programa cliente RPC denominado MyClnt.exe. El primer paso consiste en definir la interfaz en el archivo MyApp.idl. El compilador MIDL usa MyApp.idl para generar el archivo MyApp \_ c.c, que contiene el código auxiliar del cliente. También genera el archivo MyApp.h, que el programa cliente debe incluir. El programa cliente también tendrá que incluir los archivos RPC.h y RPC RPC RPC.h.

El propio programa cliente se crea en el archivo MyClnt.c. En un proyecto real, el programa cliente normalmente se compone de varios archivos de código fuente de C. Todas ellas tendrían que compilarse y vincularse juntas. Sin embargo, en este ejemplo solo se usa un archivo para simplificar.

Los archivos MyClnt.c y MyApp c.c se compilan y vinculan junto con la biblioteca en tiempo de ejecución rpc y cualquier otra biblioteca que el programa \_ cliente necesite. El resultado es un programa cliente ejecutable denominado MyClnt.exe.

Si no compila el archivo IDL en modo de compatibilidad de OSF ([**/osf**](/windows/desktop/Midl/-osf)), el programa cliente debe proporcionar una función para asignar memoria y una función para desasignar. Para Windows 2000 y versiones posteriores, el modo recomendado [**es /Oicf**](/windows/desktop/Midl/-oi). Para obtener más información, vea [How Memory Is Allocated and Deallocated](how-memory-is-allocated-and-deallocated.md), y [Pointers and Memory Allocation](pointers-and-memory-allocation.md).

 

 