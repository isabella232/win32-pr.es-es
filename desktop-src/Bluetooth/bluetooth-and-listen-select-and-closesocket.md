---
title: Bluetooth y escuchar, seleccionar y closesocket
description: Bluetooth usa las funciones Listen, SELECT y closesocket sin ninguna modificación de la programación estándar de Windows Sockets.
ms.assetid: b64440de-bc63-4e3b-bfd9-5cf783f36c23
keywords:
- Bluetooth
- closesocket
- listen
- select
- Bluetooth y escuchar
- Bluetooth y escuchar, seleccione
- Bluetooth y escuchar, seleccionar y closesocket
- listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e442cfc0593ab5be297902487c7c3ccdf056b4e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487914"
---
# <a name="bluetooth-and-listen-select-and-closesocket"></a>Bluetooth y escuchar, seleccionar y closesocket

Bluetooth usa las funciones [**Listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**Select**](/windows/desktop/api/winsock2/nf-winsock2-select)y [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) sin ninguna modificación de la programación estándar de Windows Sockets.

Al igual que con Windows Sockets, la función [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) libera los recursos asociados al socket.

Cuando se llama a la función [**Listen**](/windows/desktop/api/winsock2/nf-winsock2-listen) , se recomienda encarecidamente que se use un valor bajo para el parámetro de *trabajo pendiente* (normalmente de 2 a 4), ya que solo se aceptan algunas conexiones de cliente. Esto reduce los recursos del sistema que se asignan para su uso por el socket de escucha.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[**escuchar**](/windows/desktop/api/winsock2/nf-winsock2-listen)
</dt> <dt>

[**no**](/windows/desktop/api/winsock2/nf-winsock2-select)
</dt> </dl>

 

 