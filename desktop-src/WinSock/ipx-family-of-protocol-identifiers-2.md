---
description: El parámetro protocol en socket y WSASocket es un identificador que establece un tipo de red y un método para identificar los distintos protocolos de transporte que se ejecutan en la red.
ms.assetid: cb4d99d5-3ae0-4bfc-b521-122dd9d4f1c2
title: Familia IPX de identificadores de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 549e1dbdb9d379e87ed8e22871188b0b7762e924a695721f1c860fce14f2a2e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733655"
---
# <a name="ipx-family-of-protocol-identifiers"></a>Familia IPX de identificadores de protocolo

El *parámetro protocol* en [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) y [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) es un identificador que establece un tipo de red y un método para identificar los distintos protocolos de transporte que se ejecutan en la red. A diferencia de IP, IPX no usa un único valor de protocolo para seleccionar una pila de transporte. Puesto que no hay ningún requisito de red para usar un valor específico para cada protocolo de transporte, podemos asignarlos de una manera adecuada para las aplicaciones Winsock. Se evitan los valores de 0 a 255 para evitar colisiones con los valores de \_ protocolo PF INET correspondientes.



| Nombre         | Value       | Tipos de socket              | Descripción                                         |
|--------------|-------------|---------------------------|-----------------------------------------------------|
| Reservada     | 0-255       |                           | Reservado para valores \_ de protocolo PF INET.              |
| IPX de NSPROTO \_ | 1000 - 1255 | SOCK \_ DGRAM SOCK \_ RAW     | Servicio de datagramas para IPX.                           |
| NSPROTO \_ SPX | 1256        | SOCK \_ STREAM SOCK \_ SEQPKT | Intercambio de paquetes confiable mediante paquetes de tamaño fijo. |



 

> [!Note]  
> Cuando se especifica NSPROTO SPX, el protocolo SPX II se usa automáticamente si ambos puntos de conexión son capaces \_ de hacerlo.

 

 

 



