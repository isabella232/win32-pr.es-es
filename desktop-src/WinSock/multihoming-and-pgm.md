---
description: Se debe tener en cuenta una consideración especial para los receptores o los remitentes de PGM de host múltiple. En esta página se describen las consideraciones y se proporcionan instrucciones para las mejores prácticas de programación.
ms.assetid: 10fb56dd-3c96-4944-9b53-aee76c269528
title: Host múltiple y PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142527c7fdf3e5d34d80c51e4002bc21ad47691c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659803"
---
# <a name="multihoming-and-pgm"></a>Host múltiple y PGM

Se debe tener en cuenta una consideración especial para los receptores o los remitentes de PGM de host múltiple. En esta página se describen las consideraciones y se proporcionan instrucciones para las mejores prácticas de programación.

## <a name="multihomed-pgm-sender"></a>Remitente PGM de host múltiple

Cuando una aplicación no puede especificar una interfaz al llamar a la función [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , se usa la primera interfaz disponible. Si no hay ninguna interfaz disponible, se produce un error de **conexión** .

Cuando una aplicación especifica una interfaz mediante la opción [RM \_ set \_ send \_ If](socket-options.md) socket, se realiza un intento de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) implícitamente a esa interfaz mediante TCP/IP y se produce un error si TCP/IP produce un error en la solicitud de enlace. Si la interfaz se establece mediante RM \_ set \_ send \_ si varias veces, solo se aplica la última interfaz establecida correctamente.

Windows Sockets mantiene la interfaz que se establece y, si esa interfaz desaparece, la sesión se desconecta.

## <a name="multihomed-pgm-receiver"></a>Receptor PGM de host múltiple

Cuando una aplicación no puede especificar una interfaz al llamar a la función [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , se usa la interfaz predeterminada. Si no hay ninguna interfaz disponible, se produce un error de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) .

Cuando una aplicación especifica una o más interfaces en las que se va a realizar la escucha, mediante el uso de [RM \_ Add \_ Receive \_ si](socket-options.md), Windows Sockets intenta enlazar a la interfaz o interfaces solicitadas mediante TCP/IP. Cualquier error de TCP/IP hace que esta solicitud produzca un error. A diferencia del caso del remitente PGM, la adición de una interfaz de recepción varias veces da lugar a que se publiquen las escuchas en todas las interfaces agregadas correctamente. Use la \_ opción de \_ socket de recepción IF de RM \_ para detener la escucha en una interfaz.

Windows Sockets no mantiene el estado de varias interfaces de escucha especificadas y, en su lugar, se basa en TCP/IP para hacerlo. Sin embargo, una vez que una sesión está en curso, Windows Sockets realiza un seguimiento de la interfaz entrante de esa sesión y, si esa interfaz desaparece, Windows Sockets desconecta la sesión.

 

 



