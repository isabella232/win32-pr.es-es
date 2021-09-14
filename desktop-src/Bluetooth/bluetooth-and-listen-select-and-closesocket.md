---
title: Bluetooth, escuchar, seleccionar y cerrarsocket
description: Bluetooth las funciones listen, select y closesocket sin ninguna modificación de la programación estándar Windows Sockets.
ms.assetid: b64440de-bc63-4e3b-bfd9-5cf783f36c23
keywords:
- Bluetooth
- closesocket
- listen
- select
- Bluetooth y escucha
- Bluetooth y escucha, seleccione
- Bluetooth, escuchar, seleccionar y cerrarsocket
- listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e442cfc0593ab5be297902487c7c3ccdf056b4e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361477"
---
# <a name="bluetooth-and-listen-select-and-closesocket"></a>Bluetooth, escuchar, seleccionar y cerrarsocket

Bluetooth las funciones [**listen,**](/windows/desktop/api/winsock2/nf-winsock2-listen) [**select**](/windows/desktop/api/winsock2/nf-winsock2-select)y [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) sin ninguna modificación de la programación estándar Windows Sockets.

Al igual que Windows sockets, la [**función closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) libera los recursos asociados al socket.

Al llamar a la función [**de**](/windows/desktop/api/winsock2/nf-winsock2-listen) escucha, se recomienda encarecidamente que se utilice un valor bajo para el parámetro *de* trabajo pendiente (normalmente de 2 a 4), ya que solo se aceptan algunas conexiones de cliente. Esto reduce los recursos del sistema asignados para su uso por el socket de escucha.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen)
</dt> <dt>

[**Seleccione**](/windows/desktop/api/winsock2/nf-winsock2-select)
</dt> </dl>

 

 