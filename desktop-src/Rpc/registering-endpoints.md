---
title: Registro de puntos de conexión
description: El registro del programa de servidor en la asignación de extremo del equipo host del servidor permite a los programas cliente determinar qué punto de conexión (normalmente un puerto TCP/IP o una canalización con nombre) está escuchando el programa de servidor.
ms.assetid: d09874f8-2b55-4af2-bfe1-8978301d6692
keywords:
- RPC llamada a procedimiento remoto, tareas, registrar extremos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23e02aaae18a9d28b989d16850693a8a8f0678e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772864"
---
# <a name="registering-endpoints"></a>Registro de puntos de conexión

El registro del programa de servidor en la asignación de extremo del equipo host del servidor permite a los programas cliente determinar qué punto de conexión (normalmente un puerto TCP/IP o una canalización con nombre) está escuchando el programa de servidor. Para registrarse en la asignación de punto de conexión del sistema host del servidor, un programa de servidor llama a la función [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) , tal como se muestra en el siguiente fragmento de código:


```C++
// This example assumes that MyInterface_v1_0_s_ifspec is a valid data
// structure that represents the interface being registered. The 
// variable is a valid pointer to a binding vector.
RPC_STATUS status;
status = RpcEpRegister(
    MyInterface_v1_0_s_ifspec,
    rpcBindingVector,
    NULL,
    NULL);
```



El primer parámetro de [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) es la estructura que representa la interfaz. Puede encontrarlo en el archivo de encabezado que el compilador MIDL generó a partir del archivo MIDL para esta aplicación distribuida. Vea [desarrollar la interfaz](developing-the-interface.md). A continuación, **RpcEpRegister** necesita que la aplicación pase un conjunto de identificadores de enlace que se almacenan en un vector de enlace.

Además de registrar los nombres de interfaz, la aplicación de servidor también puede registrar UUID de objeto en la asignación de punto de conexión. En este ejemplo, no hay ningún UUID de objeto para registrar, por lo que el tercer parámetro de [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) se establece en **null**.

El último parámetro es una cadena de comentario. Aunque la biblioteca en tiempo de ejecución de RPC no usa esta cadena, se recomienda establecer la cadena, ya que mejora la capacidad de administración del sistema. Un administrador del sistema puede usar la cadena para detectar qué puertos usan las aplicaciones, que se pueden usar para determinar qué puertos se van a administrar mediante firewalls.

 

 




