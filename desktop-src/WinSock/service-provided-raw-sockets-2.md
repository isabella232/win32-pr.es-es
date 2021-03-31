---
description: Un socket sin formato es un tipo de socket que permite el acceso al proveedor de transporte subyacente. El uso de sockets sin formato al migrar aplicaciones a Winsock no se recomienda por varias razones.
ms.assetid: b78c75b7-255c-4e85-9a88-0efb3b5f0e51
title: Sockets sin formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209c884e85327a7a8c1d21292d9342a0c032747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155869"
---
# <a name="raw-sockets"></a>Sockets sin formato

Un socket sin formato es un tipo de socket que permite el acceso al proveedor de transporte subyacente. El uso de sockets sin formato al migrar aplicaciones a Winsock no se recomienda por varias razones.

La especificación de Windows Sockets no exige que un proveedor de servicios Winsock admita Sockets sin formato, es decir, sockets de tipo **sock \_ raw**. Sin embargo, se recomienda que los proveedores de servicios proporcionen compatibilidad con sockets sin formato. Una aplicación compatible con Windows Sockets que desee usar sockets sin formato debe intentar abrir el socket con la llamada de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) , y si se produce un error al intentar usar otro tipo de socket o indicar el error al usuario.

En Windows 7, Windows Server 2008 R2, Windows Vista y Windows XP con Service Pack 2 (SP2), la capacidad de enviar tráfico a través de sockets sin formato se ha restringido de varias maneras. Para obtener más información, consulte [Sockets sin formato de TCP/IP](tcp-ip-raw-sockets-2.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trasladar aplicaciones de socket a Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**tomacorriente**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[Sockets sin formato de TCP/IP](tcp-ip-raw-sockets-2.md)
</dt> <dt>

[Consideraciones sobre la programación de Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



