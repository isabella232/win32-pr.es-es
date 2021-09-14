---
description: Un socket sin formato es un tipo de socket que permite el acceso al proveedor de transporte subyacente. No se recomienda el uso de sockets sin procesar al portear aplicaciones a Winsock por varias razones.
ms.assetid: b78c75b7-255c-4e85-9a88-0efb3b5f0e51
title: Sockets sin procesar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209c884e85327a7a8c1d21292d9342a0c032747a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241497"
---
# <a name="raw-sockets"></a>Sockets sin procesar

Un socket sin formato es un tipo de socket que permite el acceso al proveedor de transporte subyacente. No se recomienda el uso de sockets sin procesar al portear aplicaciones a Winsock por varias razones.

La Windows sockets no exige que un proveedor de servicios Winsock admita sockets sin procesar, es decir, sockets de tipo **SOCK \_ RAW**. Sin embargo, se recomienda a los proveedores de servicios que proporcionen compatibilidad con sockets sin procesar. Una aplicación compatible con Windows Sockets que desee usar sockets sin procesar debe intentar abrir el socket con la llamada [**de socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) y, si se produce un error, intente usar otro tipo de socket o indique el error al usuario.

En Windows 7, Windows Server 2008 R2, Windows Vista y Windows XP con Service Pack 2 (SP2), la capacidad de enviar tráfico a través de sockets sin procesar se ha restringido de varias maneras. Para obtener más información, [vea Sockets sin formato TCP/IP.](tcp-ip-raw-sockets-2.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Porte de aplicaciones de socket a Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**Zócalo**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[Sockets sin formato TCP/IP](tcp-ip-raw-sockets-2.md)
</dt> <dt>

[Consideraciones de programación de Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



