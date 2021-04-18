---
description: 'La API del proveedor de espacio de nombres PNRP utiliza las siguientes estructuras:'
ms.assetid: 697fb99a-259f-429c-8818-0d725255bc86
title: Estructuras PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e2ee85f3673395ade31417c79c010354f16b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667386"
---
# <a name="pnrp-structures"></a>Estructuras PNRP

La API del proveedor de espacio de nombres PNRP utiliza las siguientes estructuras:



| Estructura                                                             | Descripción                                                                                                                                                         |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_información del \_ punto de conexión PNRP del mismo nivel \_**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_endpoint_info)         | Contiene las direcciones IP y los datos asociados a un punto de conexión del mismo nivel.                                                                                                 |
| [**\_información de \_ la nube PNRP del mismo nivel \_**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_cloud_info)               | Contiene información sobre una nube de protocolo de resolución de nombres de mismo nivel (PNRP).                                                                                            |
| [**\_información de \_ registro de PNRP del mismo nivel \_**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_registration_info) | Contiene la información proporcionada por una identidad del mismo nivel cuando se registra con una nube PNRP.                                                                           |
| [PNRP y BLOB](pnrp-and-blob.md)                                    | Pasa datos a la estructura [**WSAQUERYSET**](winsock-nsp-reference-links.md) durante las llamadas a varias funciones.                                                  |
| [PNRP y WSAQUERYSET](pnrp-and-wsaqueryset.md)                      | Facilita la resolución de nombres y la enumeración de nombres y nubes.                                                                                         |
| [**\_identificador de nube PNRP \_**](/windows/desktop/api/Pnrpdef/ns-pnrpdef-pnrp_cloud_id)                              | Contiene los valores que definen una nube de red.                                                                                                                    |
| [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)                                | Apuntado por el miembro **lpBlob** de la estructura [**WSAQUERYSET**](winsock-nsp-reference-links.md) .                                                            |
| [**PNRPINFO \_ v1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)                                      | Apuntado por el miembro **lpBlob** de la estructura [**WSAQUERYSET**](winsock-nsp-reference-links.md)                                                             |
| [**PNRPINFO \_ V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))                                   | Apuntado por el miembro **lpBlob** de la estructura [**WSAQUERYSET**](winsock-nsp-reference-links.md) y proporciona compatibilidad con datos opacos específicos de la aplicación. |



 

 

 
