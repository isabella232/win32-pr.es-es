---
description: Sugerencias para la solución de problemas
ms.assetid: e87ad3bd-07ae-4b9d-b465-2ce4688bdd83
title: Sugerencias para la solución de problemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fe361af291c29f8784235066f341d940ab38205cd3b8238896011f85021a9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651247"
---
# <a name="troubleshooting-tips"></a>Sugerencias para la solución de problemas

Estas sugerencias le ayudarán a evitar interbloqueos o bloqueos en la DirectShow aplicación.

**Objetos globales**

Un objeto de C++ global no debe crear DirectShow en su método constructor ni liberarlos en su método destructor. Esto puede hacer que la aplicación se bloquee indefinidamente, por el siguiente motivo:

Los subprocesos no pueden salir mientras están dentro de la función de punto de entrada de un archivo DLL. Kernel 32 contiene un bloqueo de proceso global durante la función de punto de entrada y el bloqueo impide que el subproceso salga. Dado que algunos DirectShow objetos poseen subprocesos, pueden bloquearse si se liberan desde dentro de una función de punto de entrada de DLL. Si una aplicación tiene un objeto de C++ global, el archivo DLL en tiempo de ejecución de C llama al destructor del objeto cuando se descarga el archivo DLL. Si el destructor libera DirectShow objetos , se puede bloquear como resultado.

Por motivos similares, un archivo DLL no debe crear ni liberar objetos DirectShow en su rutina de punto de entrada.

**Liberar interfaces**

Debe liberar todos los DirectShow de interfaz mientras la aplicación sigue procesando mensajes, antes de salir del bucle de mensajes. De lo contrario, es posible que vea varias aserciones, ya que algunos objetos DirectShow envían mensajes durante sus rutinas de limpieza.

(Como corolario, si usa la clase **ATL CWindowImpl,** no espere hasta **OnFinalMessage** para liberar las interfaces. En su lugar, liberarlos cuando controle el mensaje \_ WM CLOSE).

**Recuentos de referencias**

Cuando la versión de depuración Quartz.dll descarga, comprueba si los objetos de DirectShow tienen recuentos de referencias que no se liberaron. Si es así, produce una aserción:


```C++
g_cFGObjects == 0 
```



Cuando se produce un error en esta aserción, significa que la aplicación ha filtrado un recuento de referencias. Revise el código y asegúrese de liberar todos los punteros de interfaz.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Depuración en DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



