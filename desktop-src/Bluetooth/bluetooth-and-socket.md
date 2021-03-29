---
title: Bluetooth y socket
description: Crea un socket para las conexiones entrantes o salientes.
ms.assetid: 21b9cf1f-1a85-4a4b-9557-faa4f32c3696
keywords:
- Bluetooth Bluetooth
- Bluetooth de socket
- Bluetooth y Socket Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2c2085ee0c61941bab93ed25dd86f5c102d0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791889"
---
# <a name="bluetooth-and-socket"></a>Bluetooth y socket

La función [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) crea un socket para las conexiones entrantes o salientes.

Para crear un socket mediante Bluetooth, utilice la siguiente configuración:

-   El parámetro *AF* de la función [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) siempre se establece en **AF \_ BTH** para los sockets Bluetooth.
-   El parámetro de *tipo* de la función de [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) siempre es **sock \_ Stream**; **Sock \_** Los sockets DGRAM no son compatibles con Bluetooth.
-   En el caso del parámetro *Protocol* , **BTHPROTO \_ RFCOMM** es el protocolo admitido.

Para obtener más información, consulte [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**tomacorriente**](/windows/desktop/api/winsock2/nf-winsock2-socket)
</dt> </dl>

 

 