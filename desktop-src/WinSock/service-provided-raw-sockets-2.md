---
description: Un socket sin formato es un tipo de socket que permite el acceso al proveedor de transporte subyacente. No se recomienda el uso de sockets sin procesar al portear aplicaciones a Winsock por varias razones.
ms.assetid: b78c75b7-255c-4e85-9a88-0efb3b5f0e51
title: Sockets sin procesar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c1522c2b8499e2ba8f1bb693513105804ec936fc2224fccaa55dd90a1b0dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740539"
---
# <a name="raw-sockets"></a>Sockets sin procesar

Un socket sin formato es un tipo de socket que permite el acceso al proveedor de transporte subyacente. No se recomienda el uso de sockets sin procesar al portear aplicaciones a Winsock por varias razones.

La Windows sockets no exige que un proveedor de servicios Winsock admita sockets sin procesar, es decir, sockets de tipo **SOCK \_ RAW.** Sin embargo, se recomienda a los proveedores de servicios que proporcionen compatibilidad con sockets sin procesar. Una aplicación compatible con Windows Sockets que desee usar sockets sin procesar debe intentar abrir el socket con la llamada [**de socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) y, si se produce un error, intente usar otro tipo de socket o indique el error al usuario.

En Windows 7, Windows Server 2008 R2, Windows Vista y Windows XP con Service Pack 2 (SP2), la capacidad de enviar tráfico a través de sockets sin procesar se ha restringido de varias maneras. Para obtener más información, [vea Sockets sin formato TCP/IP.](tcp-ip-raw-sockets-2.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Porting Socket Applications to Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**Zócalo**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[Sockets sin formato TCP/IP](tcp-ip-raw-sockets-2.md)
</dt> <dt>

[Consideraciones de programación de Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



