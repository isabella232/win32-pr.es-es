---
title: Identificadores de enlace explícitos
description: Para obtener el máximo control sobre el proceso de enlace, las aplicaciones cliente/servidor pueden usar identificadores de enlace explícitos.
ms.assetid: e711ce37-92f0-4e60-a126-148c27662c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a6e723d8559dc5e72783412eb6250f69431f31d08a92c4984fb2e2a19b761d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930024"
---
# <a name="explicit-binding-handles"></a>Identificadores de enlace explícitos

Para obtener el máximo control sobre el proceso de enlace, las aplicaciones cliente/servidor pueden usar identificadores de enlace explícitos. Al igual que los identificadores implícitos, los identificadores de enlace explícitos permiten a la aplicación cliente seleccionar un servidor para ejecutar sus llamadas. Además, los identificadores de enlace explícitos permiten a la aplicación cliente/servidor crear una sesión de comunicación RPC autenticada. Con identificadores explícitos, el cliente puede conectarse a más de un servidor y ejecutar procedimientos remotos en varios servidores. Las aplicaciones cliente multiproceso y asincrónicas incluso pueden conectarse a varios servidores y ejecutar varios procedimientos remotos al mismo tiempo.

La aplicación cliente debe pasar el identificador explícito como parámetro a cada llamada a procedimiento remoto. Para cumplir con el estándar de OSF, el identificador debe especificarse como el primer parámetro en cada procedimiento remoto. Sin embargo, las extensiones de Microsoft para RPC permiten especificar el identificador de enlace en otras posiciones. Para obtener más información, vea [Microsoft RPC Binding-Handle Extensions](microsoft-rpc-binding-handle-extensions.md).

Para crear un identificador explícito, declare el identificador como un parámetro para las operaciones remotas en el archivo IDL. El [ejemplo Hello, World](tutorial.md) se puede volver a definir para usar un identificador explícito como se muestra a continuación:

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

Puede combinar identificadores explícitos e implícitos en una sola interfaz. Si una función tiene un identificador explícito en su lista de parámetros, se usará ese identificador. Si una función de una interfaz que usa identificadores implícitos no especifica un identificador explícito, se usará el identificador implícito predeterminado.

 

 




