---
title: Identificadores de enlace explícitos
description: Para obtener el máximo control sobre el proceso de enlace, las aplicaciones cliente/servidor pueden utilizar identificadores de enlace explícitos.
ms.assetid: e711ce37-92f0-4e60-a126-148c27662c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b391c339ac3747928e3394152e9c0de7c1c7aa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676181"
---
# <a name="explicit-binding-handles"></a>Identificadores de enlace explícitos

Para obtener el máximo control sobre el proceso de enlace, las aplicaciones cliente/servidor pueden utilizar identificadores de enlace explícitos. Al igual que los identificadores implícitos, los identificadores de enlace explícitos permiten que la aplicación cliente seleccione un servidor para ejecutar sus llamadas. Además, los identificadores de enlace explícitos permiten que la aplicación cliente/servidor cree una sesión de comunicación RPC autenticada. Con los identificadores explícitos, el cliente puede conectarse a más de un servidor y ejecutar procedimientos remotos en varios servidores. Las aplicaciones cliente multiproceso y asincrónicas incluso pueden conectarse a varios servidores y ejecutar varios procedimientos remotos al mismo tiempo.

La aplicación cliente debe pasar el identificador explícito como parámetro a cada llamada a procedimiento remoto. Para ajustarse al estándar de OSF, el identificador debe especificarse como el primer parámetro en cada procedimiento remoto. Sin embargo, las extensiones de Microsoft para RPC le permiten especificar el controlador de enlace en otras posiciones. Para obtener más información, vea [extensiones de Microsoft RPC Binding-Handle](microsoft-rpc-binding-handle-extensions.md).

Para crear un identificador explícito, declare el identificador como un parámetro para las operaciones remotas en el archivo IDL. El [ejemplo Hello, World](tutorial.md) se puede redefinir para usar un identificador explícito, como se muestra a continuación:

``` syntax
/* IDL file for explicit handles */
 
[ 
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0) 
]
interface hello
{
  void HelloProc([in] handle_t h1,
                 [in, string] char *  pszString); 
}
```

Puede combinar controladores explícitos e implícitos en una sola interfaz. Si una función tiene un identificador explícito en su lista de parámetros, se usará dicho identificador. Si una función de una interfaz que usa identificadores implícitos no especifica un identificador explícito, se usará el identificador implícito predeterminado.

 

 




