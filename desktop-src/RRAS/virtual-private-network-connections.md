---
title: Conexiones de red privada virtual
description: El servicio de acceso remoto (RAS) admite conexiones de red privada virtual (VPN) además de conexiones de acceso remoto convencionales que utilizan Protocolo punto a punto (PPP).
ms.assetid: c1195ebb-3107-4429-bc67-b64577d66268
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f5fc0b80a6eb00e7587e941eea39c056a11d14
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077866"
---
# <a name="virtual-private-network-connections"></a>Conexiones de red privada virtual

El servicio de acceso remoto (RAS) admite conexiones de red privada virtual (VPN) además de conexiones de acceso remoto convencionales que utilizan Protocolo punto a punto (PPP). En una conexión VPN, los paquetes VPN se encapsulan en paquetes IP y se envían a través de una red IP como Internet. Por lo tanto, el acceso a una red IP es un requisito para establecer una conexión VPN. Si el equipo cliente tiene una conexión siempre activada a una red IP, por ejemplo, una conexión a una LAN IP, el cliente puede establecer la conexión VPN mediante una única llamada a la función [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) .

Si el equipo cliente no tiene una conexión siempre activada a una red IP, se necesitan dos llamadas a [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para establecer la conexión VPN. La primera llamada establece una conexión de acceso telefónico a la red IP; la segunda llamada establece la conexión VPN.

El miembro **szLocalPhoneNumber** de la estructura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) para la conexión VPN debe contener el nombre DNS o la dirección IP del servidor VPN de destino.

Cada conexión requiere una entrada [de libreta de teléfonos](ras-phone-books.md) independiente. La primera llamada a [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) especifica la entrada del libro de teléfono para la red IP. La segunda llamada especifica la entrada de la libreta de teléfonos de la VPN.

La función [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) toma un puntero a una estructura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) como parámetro. Esta estructura especifica las credenciales de autenticación que se usarán para la red especificada por la entrada del libro de teléfono. Las credenciales necesarias para tener acceso a la red IP suelen ser diferentes de las de la VPN. La primera llamada a **rasdial** debe especificar las credenciales de la red IP. La segunda llamada debe especificar las credenciales de la VPN.

Si la función [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) se realiza correctamente, devuelve un identificador para la conexión. Use este identificador en una llamada a [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) para finalizar la conexión.

En el escenario anterior, las dos llamadas a [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) devuelven controladores de conexión independientes para la red IP y la VPN. La llamada a [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) con el identificador de la conexión VPN termina la conexión VPN, pero deja intacta la conexión a la red IP.

 

 