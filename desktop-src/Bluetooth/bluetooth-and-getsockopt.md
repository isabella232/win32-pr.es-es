---
title: Bluetooth y getsockopt
description: Bluetooth usa la función getsockopt para consultar varios parámetros asociados con el canal de servidor o la conexión.
ms.assetid: 9593fd6c-b55d-45d8-a9d9-87ebcd09d1bd
keywords:
- Bluetooth
- getsockopt
- Bluetooth y getsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dede19b27eea39b7d1e778b3e92312a5e148c0ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792423"
---
# <a name="bluetooth-and-getsockopt"></a>Bluetooth y getsockopt

Bluetooth usa la función [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para consultar varios parámetros asociados con el canal de servidor o la conexión. El uso de **getsockopt** con Bluetooth tiene los siguientes requisitos:

-   El parámetro *s* de [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) debe ser un Socket Bluetooth válido.
-   El parámetro *LEVEL* de [**GETSOCKOPT**](/windows/desktop/api/winsock/nf-winsock-getsockopt) debe ser sol \_ RFCOMM.

Para obtener una lista de las opciones de Socket Bluetooth disponibles, consulte [Opciones de Bluetooth y socket](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> </dl>

 

 