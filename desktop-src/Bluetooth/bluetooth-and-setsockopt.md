---
title: Bluetooth y-i
description: Bluetooth usa la función de la función-to para establecer diversos parámetros asociados con el canal de servidor o la conexión.
ms.assetid: ab78baed-5556-4d7b-88a6-e3ceb93afa8c
keywords:
- Bluetooth
- setsockopt
- Bluetooth y-i
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 943839a49788b76e597596aee9cba65fa4b8d30d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359043"
---
# <a name="bluetooth-and-setsockopt"></a>Bluetooth y-i

Bluetooth usa la [**función de**](/windows/desktop/api/winsock/nf-winsock-setsockopt) la función-to para establecer diversos parámetros asociados con el canal de servidor o la conexión. El uso **de las opciones de la** con Bluetooth tiene los siguientes requisitos:

-   El parámetro *s* de [**r**](/windows/desktop/api/winsock/nf-winsock-setsockopt) debe ser un Socket Bluetooth válido.
-   El parámetro *LEVEL* de [**la**](/windows/desktop/api/winsock/nf-winsock-setsockopt) de-to debe ser sol \_ RFCOMM.

Para obtener una lista de las opciones de Socket Bluetooth disponibles, consulte [Opciones de Bluetooth y socket](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 