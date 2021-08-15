---
description: 'La API del proveedor de espacios de nombres PNRP usa las estructuras siguientes:'
ms.assetid: 697fb99a-259f-429c-8818-0d725255bc86
title: Estructuras PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2e275dff1b0c0986cfa998ed64cfb1ffad5b19af400f8719715d2106af353d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011533"
---
# <a name="pnrp-structures"></a>Estructuras PNRP

La API del proveedor de espacios de nombres PNRP usa las estructuras siguientes:



| Estructura                                                             | Descripción                                                                                                                                                         |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INFORMACIÓN DEL \_ PUNTO DE CONEXIÓN PNRP DEL MISMO \_ \_ NIVEL**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_endpoint_info)         | Contiene las direcciones IP y los datos asociados a un punto de conexión del mismo nivel.                                                                                                 |
| [**INFORMACIÓN \_ DE NUBE DE PNRP DEL MISMO \_ \_ NIVEL**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_cloud_info)               | Contiene información sobre una nube del Protocolo de resolución de nombres del mismo nivel (PNRP).                                                                                            |
| [**INFORMACIÓN \_ DE REGISTRO DE PNRP DEL MISMO \_ \_ NIVEL**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_registration_info) | Contiene la información proporcionada por una identidad del mismo nivel cuando se registra con una nube PNRP.                                                                           |
| [PNRP y BLOB](pnrp-and-blob.md)                                    | Pasa datos a la estructura [**WSAQUERYSET**](winsock-nsp-reference-links.md) durante las llamadas a varias funciones.                                                  |
| [PNRP y WSAQUERYSET](pnrp-and-wsaqueryset.md)                      | Facilita la resolución de nombres y la enumeración de nombres y nubes.                                                                                         |
| [**PNRP \_ CLOUD \_ ID**](/windows/desktop/api/Pnrpdef/ns-pnrpdef-pnrp_cloud_id)                              | Contiene los valores que definen una nube de red.                                                                                                                    |
| [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)                                | Señalado por el **miembro lpBlob** de la [**estructura WSAQUERYSET.**](winsock-nsp-reference-links.md)                                                            |
| [**PNRPINFO \_ V1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)                                      | Señalado por el **miembro lpBlob** de la [**estructura WSAQUERYSET**](winsock-nsp-reference-links.md)                                                             |
| [**PNRPINFO \_ V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))                                   | Señalado por el miembro **lpBlob** de la [**estructura WSAQUERYSET**](winsock-nsp-reference-links.md) y proporciona compatibilidad con datos opacos específicos de la aplicación. |



 

 

 
