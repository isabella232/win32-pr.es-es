---
title: Conexiones de red privada virtual
description: El servicio de acceso remoto (RAS) admite conexiones de red privada virtual (VPN), además de conexiones de acceso remoto convencionales que usan Protocolo punto a punto (PPP).
ms.assetid: c1195ebb-3107-4429-bc67-b64577d66268
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc532d0873a5c3cb4a50552ca267a8a88b305ad855a1588338786881b3af04e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024785"
---
# <a name="virtual-private-network-connections"></a>Conexiones de red privada virtual

El servicio de acceso remoto (RAS) admite conexiones de red privada virtual (VPN), además de conexiones de acceso remoto convencionales que usan Protocolo punto a punto (PPP). En una conexión VPN, los paquetes VPN se encapsulan en paquetes IP y se envían a través de una red IP como Internet. Por lo tanto, el acceso a una red IP es un requisito para establecer una conexión VPN. Si el equipo cliente tiene una conexión siempre activa a una red IP, por ejemplo, una conexión a una LAN IP, el cliente puede establecer la conexión VPN mediante una única llamada a la función [**RasDial.**](/windows/desktop/api/Ras/nf-ras-rasdiala)

Si el equipo cliente no tiene una conexión siempre activa a una red IP, se requieren dos llamadas a [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para establecer la conexión VPN. La primera llamada establece una conexión de acceso telefónico a la red IP; la segunda llamada establece la conexión VPN.

El **miembro szLocalPhoneNumber** de la estructura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) de la conexión VPN debe contener el nombre DNS o la dirección IP del servidor VPN de destino.

Cada conexión requiere una entrada [de libreta de teléfonos](ras-phone-books.md) independiente. La primera llamada a [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) especifica la entrada de la libreta de teléfonos de la red IP. La segunda llamada especifica la entrada de la libreta de teléfonos para la VPN.

La [**función RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) toma un puntero a una [**estructura RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) como parámetro. Esta estructura especifica las credenciales de autenticación que se usarán para la red especificada por la entrada de la libreta de teléfonos. Las credenciales necesarias para acceder a la red IP suelen ser diferentes de las de la VPN. La primera llamada a **RasDial** debe especificar las credenciales de la red IP. La segunda llamada debe especificar las credenciales de la VPN.

Si la [**función RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) se realiza correctamente, devuelve un identificador para la conexión. Use este identificador en una llamada a [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) para finalizar la conexión.

En el escenario anterior, las dos llamadas a [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) devuelven identificadores de conexión independientes para la red IP y la VPN. Al [**llamar a RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) con el identificador de la conexión VPN, se finaliza la conexión VPN, pero se deja intacta la conexión a la red IP.

 

 