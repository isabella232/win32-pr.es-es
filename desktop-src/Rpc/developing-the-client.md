---
title: Desarrollo del cliente
description: El desarrollo de un programa cliente RPC es similar al desarrollo del programa de servidor. Para obtener información sobre el desarrollo de un programa de servidor RPC, vea desarrollar el servidor.
ms.assetid: 92276326-d478-479e-8fa4-02a2fce58eb6
keywords:
- RPC llamada a procedimiento remoto, tareas, desarrollar el cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ceddedc4ccfd1d068e3452b64ed8c6b54a621d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995535"
---
# <a name="developing-the-client"></a>Desarrollo del cliente

El desarrollo de un programa cliente RPC es similar al desarrollo del programa de servidor. Para obtener información sobre el desarrollo de un programa de servidor RPC, vea [desarrollar el servidor](developing-the-server.md).

Al igual que en el desarrollo de servidores, el programa cliente debe incluir el archivo de encabezado que el compilador MIDL genera a partir del archivo. idl. El compilador MIDL también genera un archivo de código fuente de C que contiene el código auxiliar del cliente. Debe compilar este archivo de código fuente de C y vincularlo al programa cliente. (Además, el compilador MIDL genera un archivo de código fuente de C que contiene el código auxiliar del servidor, pero no es relevante para este debate).

Además de compilar y vincular el código auxiliar de cliente con los archivos de programa, debe vincular la biblioteca de importación (y cualquier otra biblioteca que el programa cliente necesite) al programa cliente. El proceso de creación de un programa cliente RPC se muestra en el diagrama siguiente.

![proceso de creación de un programa cliente para una aplicación distribuida](images/clntdev.png)

En el ejemplo de la ilustración anterior se muestra la creación de un programa cliente RPC denominado MyClnt.exe. El primer paso es definir la interfaz en el archivo MyApp. idl. El compilador MIDL usa MyApp. idl para generar el archivo MyApp \_ c. c, que contiene el código auxiliar del cliente. También genera el archivo MyApp. h, que debe incluir el programa cliente. El programa cliente también tendrá que incluir los archivos RPC. h y RPCNDR. h.

El propio programa cliente se crea en el archivo MyClnt. c. En un proyecto real, el programa cliente normalmente se compone de varios archivos de código fuente de C. Todos ellos deben compilarse y vincularse juntos. Sin embargo, en este ejemplo solo se usa un archivo por simplicidad.

Los archivos MyClnt. c y MyApp \_ c. c se compilan y vinculan junto con la biblioteca en tiempo de ejecución de RPC y cualquier otra biblioteca que necesite el programa cliente. El resultado es un programa cliente ejecutable denominado MyClnt.exe.

Si no compila el archivo IDL en el modo de compatibilidad de OSF ([**/OSF**](/windows/desktop/Midl/-osf)), el programa cliente debe proporcionar una función para asignar memoria y una función para desasignarla. En Windows 2000 y versiones posteriores, el modo recomendado es [**/Oicf**](/windows/desktop/Midl/-oi). Para obtener más información, consulte [cómo se asigna y desasigna la memoria](how-memory-is-allocated-and-deallocated.md), y los [punteros y la asignación de memoria](pointers-and-memory-allocation.md).

 

 