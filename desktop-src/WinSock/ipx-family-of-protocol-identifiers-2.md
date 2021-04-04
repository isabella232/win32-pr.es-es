---
description: El parámetro Protocol de socket y WSASocket es un identificador que establece un tipo de red y un método para identificar los distintos protocolos de transporte que se ejecutan en la red.
ms.assetid: cb4d99d5-3ae0-4bfc-b521-122dd9d4f1c2
title: Familia IPX de identificadores de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fc808a04f1cf10bb099cd7d923bf471e9bd8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154270"
---
# <a name="ipx-family-of-protocol-identifiers"></a>Familia IPX de identificadores de protocolo

El parámetro *Protocol* de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) y [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) es un identificador que establece un tipo de red y un método para identificar los distintos protocolos de transporte que se ejecutan en la red. A diferencia de IP, IPX no utiliza un único valor de protocolo para seleccionar una pila de transporte. Puesto que no hay ningún requisito de red para usar un valor específico para cada protocolo de transporte, podemos asignarlos de forma adecuada para las aplicaciones Winsock. Se evitan los valores 0 a 255 para evitar colisiones con los valores de \_ Protocolo PF inet correspondientes.



| Nombre         | Value       | Tipos de socket              | Descripción                                         |
|--------------|-------------|---------------------------|-----------------------------------------------------|
| Reservado     | 0-255       |                           | Reservado para \_ los valores del protocolo PF inet.              |
| NSPROTO \_ IPX | 1000-1255 | SOCK \_ DGRAM sock \_ raw     | Servicio de datagrama para IPX.                           |
| NSPROTO \_ SPX | 1256        | SOCK \_ Stream sock \_ SEQPKT | Intercambio de paquetes confiable con paquetes de tamaño fijo. |



 

> [!Note]  
> Cuando \_ se especifica NSPROTO SPX, el protocolo SPX II se emplea automáticamente si ambos puntos de conexión son capaces de hacerlo.

 

 

 



