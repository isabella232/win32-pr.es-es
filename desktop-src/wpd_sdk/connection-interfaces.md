---
description: Interfaces de conexión MTP/Bluetooth
ms.assetid: 7bbd5fe3-85f1-4f0a-9d3e-22746bd23aae
title: Interfaces de conexión MTP/Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c0f32717afe14be05cae6e43d097e67fc9790729e5be4ce9c2dfa6f901a126a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843372"
---
# <a name="mtpbluetooth-connection-interfaces"></a>Interfaces de conexión MTP/Bluetooth

Las interfaces siguientes permiten a las aplicaciones enumerar y conectarse solo a dispositivos que admiten el Protocolo de transferencia multimedia (MTP) a través de Bluetooth (MTP/Bluetooth). Las interfaces de controlador, colección y cliente de WPD no están restringidas al protocolo MTP/Bluetooth cliente.



| Interfaz                                                              | Descripción                                                                                                         |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**IConnectionRequestCallback**](iconnectionrequestcallback.md)       | Define un único método de devolución de llamada que las aplicaciones usan para recibir notificaciones de solicitudes completadas y canceladas. |
| [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) | Enumera las **interfaces IPortableDeviceConnector.**                                                                 |
| [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)           | Admite métodos a los que las aplicaciones llaman para establecer conexiones a MTP Bluetooth dispositivos.                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 



