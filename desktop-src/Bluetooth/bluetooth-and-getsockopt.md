---
title: Bluetooth y getsockopt
description: Bluetooth utiliza la función getsockopt para consultar varios parámetros asociados con el canal del servidor o la conexión.
ms.assetid: 9593fd6c-b55d-45d8-a9d9-87ebcd09d1bd
keywords:
- Bluetooth
- getsockopt
- Bluetooth y getsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee63d8dc1665868023967dd88c5ba223cce538c1fa1d41dd151329f6bf52f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081089"
---
# <a name="bluetooth-and-getsockopt"></a>Bluetooth y getsockopt

Bluetooth utiliza la [**función getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para consultar varios parámetros asociados con el canal del servidor o la conexión. El uso **de getsockopt** con Bluetooth tiene los siguientes requisitos:

-   El *parámetro s* de [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) debe ser un socket Bluetooth válido.
-   El *parámetro level* de [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) debe ser SOL \_ RFCOMM.

Para obtener una lista de las opciones Bluetooth sockets disponibles, [vea Bluetooth y Opciones de socket](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> </dl>

 

 