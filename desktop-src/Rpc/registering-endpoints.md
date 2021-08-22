---
title: Registro de puntos de conexión
description: El registro del programa de servidor en el mapa de puntos de conexión del equipo host del servidor permite a los programas cliente determinar qué punto de conexión (normalmente un puerto TCP/IP o una canalización con nombre) escucha el programa de servidor.
ms.assetid: d09874f8-2b55-4af2-bfe1-8978301d6692
keywords:
- Llamada a procedimiento remoto RPC, tareas, registro de puntos de conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6674d20eefa9ebd690f618c36f1dfe69f37dcf7743a0830e06cb38bc85ccfd56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926865"
---
# <a name="registering-endpoints"></a>Registro de puntos de conexión

El registro del programa de servidor en el mapa de puntos de conexión del equipo host del servidor permite a los programas cliente determinar qué punto de conexión (normalmente un puerto TCP/IP o una canalización con nombre) escucha el programa de servidor. Para registrarse en la asignación de puntos de conexión del sistema host del servidor, un programa de servidor llama a la [**función RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) como se muestra en el fragmento de código siguiente:


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



El primer parámetro de [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) es la estructura que representa la interfaz . Puede encontrarlo en el archivo de encabezado que el compilador de MIDL generó a partir del archivo MIDL para esta aplicación distribuida. Consulte [Desarrollo de la interfaz](developing-the-interface.md). A **continuación, RpcEpRegister** necesita que la aplicación pase un conjunto de identificadores de enlace que se almacenan en un vector de enlace.

Además de registrar nombres de interfaz, la aplicación de servidor también puede registrar UUID de objeto en el mapa de puntos de conexión. En este ejemplo, no hay ningún UUID de objeto para registrar, por lo que el tercer parámetro de [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) se establece en **NULL.**

El último parámetro es una cadena de comentario. Aunque la biblioteca rpc en tiempo de ejecución no usa esta cadena, se recomienda establecer la cadena, ya que mejora la capacidad de administración del sistema. Un administrador del sistema puede usar la cadena para detectar qué puertos usan las aplicaciones, que luego se pueden usar para determinar qué puertos van a administrar los firewalls.

 

 




