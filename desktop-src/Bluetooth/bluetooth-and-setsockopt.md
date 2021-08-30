---
title: Bluetooth y setsockopt
description: Bluetooth usa la función setsockopt para establecer varios parámetros asociados con el canal del servidor o la conexión.
ms.assetid: ab78baed-5556-4d7b-88a6-e3ceb93afa8c
keywords:
- Bluetooth
- setsockopt
- Bluetooth y setsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70aef0914e13888f3bcb48bed5c7c90cd2585a5d22d60c27a35af605657f20c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004445"
---
# <a name="bluetooth-and-setsockopt"></a>Bluetooth y setsockopt

Bluetooth usa la [**función setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para establecer varios parámetros asociados al canal del servidor o a la conexión. El uso **de setsockopt** con Bluetooth tiene los siguientes requisitos:

-   El *parámetro s* de [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) debe ser un socket Bluetooth válido.
-   El *parámetro level* de [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) debe ser SOL \_ RFCOMM.

Para obtener una lista de las opciones Bluetooth sockets disponibles, [vea Bluetooth y Opciones de socket](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 