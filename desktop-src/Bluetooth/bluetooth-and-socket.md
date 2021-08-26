---
title: Bluetooth y socket
description: Crea un socket para las conexiones entrantes o salientes.
ms.assetid: 21b9cf1f-1a85-4a4b-9557-faa4f32c3696
keywords:
- Bluetooth Bluetooth
- socket Bluetooth
- Bluetooth y socket Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afaf61e307ce8d5001c2ba5402607b63b1ad6d19317aee044d7a2cac31259b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004305"
---
# <a name="bluetooth-and-socket"></a>Bluetooth y socket

La [**función de**](/windows/desktop/api/winsock2/nf-winsock2-socket) socket crea un socket para las conexiones entrantes o salientes:

Para crear un socket mediante Bluetooth, use la siguiente configuración:

-   El *parámetro af* de la función de [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) siempre se establece en AF **\_ BTH** para Bluetooth sockets.
-   El *parámetro de* tipo de la función de [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) es siempre **SOCK \_ STREAM**; **SOCK \_ Los sockets DGRAM** no son compatibles con Bluetooth.
-   Para el *parámetro protocol,* **BTHPROTO \_ RFCOMM** es el protocolo admitido.

Para obtener más información, [vea Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Zócalo**](/windows/desktop/api/winsock2/nf-winsock2-socket)
</dt> </dl>

 

 