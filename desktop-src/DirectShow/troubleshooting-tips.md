---
description: Sugerencias para la solución de problemas
ms.assetid: e87ad3bd-07ae-4b9d-b465-2ce4688bdd83
title: Sugerencias para la solución de problemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0280702c7ce2131d1252ec75b8bee4be231e29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667638"
---
# <a name="troubleshooting-tips"></a>Sugerencias para la solución de problemas

Las siguientes sugerencias le ayudarán a evitar interbloqueos o bloqueos en la aplicación de DirectShow.

**Objetos globales**

Un objeto de C++ global no debe crear objetos de DirectShow en su método de constructor ni publicarlos en su método de destructor. Esto puede hacer que la aplicación se bloquee indefinidamente, por el siguiente motivo:

Los subprocesos no pueden salir mientras se encuentren dentro de la función de punto de entrada de un archivo DLL. El kernel 32 mantiene un bloqueo de proceso global durante la función de punto de entrada y el bloqueo impide que el subproceso se salga. Dado que algunos objetos de DirectShow poseen subprocesos, se pueden bloquear si se liberan desde una función de punto de entrada de DLL. Si una aplicación tiene un objeto global de C++, la DLL en tiempo de ejecución de C llama al destructor del objeto cuando se descarga el archivo DLL. Si el destructor libera objetos de DirectShow, puede bloquearse como resultado.

Por motivos similares, un archivo DLL no debe crear ni liberar objetos de DirectShow en su rutina de punto de entrada.

**Liberar interfaces**

Debe liberar todos los punteros de la interfaz de DirectShow mientras la aplicación sigue procesando los mensajes antes de salir del bucle de mensajes. De lo contrario, podría ver varias aserciones, porque algunos objetos de DirectShow envían mensajes durante sus rutinas de limpieza.

(Como consecuencia, si usa la clase ATL **CWindowImpl** , no espere hasta que **OnFinalMessage** libere las interfaces. En su lugar, libere al controlar el mensaje de \_ cierre de WM).

**Recuentos de referencias**

Cuando se descarga la versión de depuración de Quartz.dll, comprueba si los objetos de DirectShow tienen recuentos de referencias que no se han liberado. Si es así, se produce una aserción:


```C++
g_cFGObjects == 0 
```



Cuando se produce un error en esta aserción, significa que la aplicación ha perdido un recuento de referencias. Revise el código y asegúrese de que libera todos los punteros de interfaz.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Depurar en DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



