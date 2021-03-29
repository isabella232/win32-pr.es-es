---
title: Desarrollo del servidor
description: Al crear un programa de servidor para una aplicación distribuida, debe utilizar el archivo de encabezado y el código auxiliar de servidor que genera el compilador MIDL.
ms.assetid: 2b7b14f5-5692-41b8-bb98-7edd36309d21
keywords:
- RPC llamada a procedimiento remoto, tareas, desarrollar el servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fc3405c52c48f531572ab159ad083bad93f95e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359287"
---
# <a name="developing-the-server"></a>Desarrollo del servidor

Al crear un programa de servidor para una aplicación distribuida, debe utilizar el archivo de encabezado y el código auxiliar de servidor que genera el compilador MIDL. Para obtener más información, vea [desarrollar la interfaz](developing-the-interface.md). Incluya el archivo de encabezado en el archivo de programa del servidor C. Compile el código auxiliar del servidor con los archivos de código fuente de C que componen la aplicación. Vincule los archivos objeto resultantes junto con la biblioteca de importación. Este proceso se ilustra en el diagrama siguiente.

![proceso de creación de un programa de servidor para una aplicación distribuida](images/srvrdev.png)

Como puede ver en el ejemplo de la ilustración, se utilizó un archivo MIDL denominado MyApp. idl para definir la interfaz. El compilador MIDL usó MyApp. idl para generar MyApp \_ s. c y MyApp. h. También genera un archivo de código fuente de C para el código auxiliar del cliente, pero no es relevante para esta discusión concreta. El archivo de código fuente de C para el programa de servidor (en este caso, Mysrvr. C) debe incluir el archivo myapp. h. También tendrá que incluir los archivos RPC. h y Rpcndr. h.

La aplicación de servidor se desarrolló en dos archivos, Mysrvr. c y Rprocs. c. El archivo Mysrvr. c contiene las funciones necesarias para poner en marcha el programa de servidor. Los procedimientos remotos que ofrece el programa de servidor se encuentran en el archivo Rprocs. c.

Los archivos Mysrvr. c y Rprocs. c se compilaron junto con MyApp \_ s. c para generar archivos de objeto. Después, los archivos objeto se vincularon a la biblioteca en tiempo de ejecución de RPC y a cualquier otra biblioteca que puedan necesitar. El resultado es un programa de servidor ejecutable denominado Mysrvr.exe.

Si no compila el archivo IDL en el modo de compatibilidad Open Software Foundation (OSF) ([**/OSF**](/windows/desktop/Midl/-osf)), el programa de servidor debe proporcionar una función para asignar memoria y una función para desasignarla. En Windows 2000 y versiones posteriores de Windows, el modo recomendado es [**/Oicf**](/windows/desktop/Midl/-oi). Para obtener más información, consulte [cómo se asigna y desasigna la memoria](how-memory-is-allocated-and-deallocated.md), y los [punteros y la asignación de memoria](pointers-and-memory-allocation.md).

 

 