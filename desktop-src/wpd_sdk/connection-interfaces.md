---
description: MTP/Bluetooth interfaces de conexión
ms.assetid: 7bbd5fe3-85f1-4f0a-9d3e-22746bd23aae
title: MTP/Bluetooth interfaces de conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e5194b8a6ababc05c36590ef30ae19ab185efe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572121"
---
# <a name="mtpbluetooth-connection-interfaces"></a>MTP/Bluetooth interfaces de conexión

Las interfaces siguientes permiten a las aplicaciones enumerar y conectarse solo a dispositivos que admiten el Protocolo de transferencia multimedia (MTP) a través de Bluetooth (MTP/Bluetooth). Las interfaces de controlador, colección e cliente de WPD no están restringidas al protocolo MTP/Bluetooth.



| Interfaz                                                              | Descripción                                                                                                         |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**IConnectionRequestCallback**](iconnectionrequestcallback.md)       | Define un único método de devolución de llamada que las aplicaciones usan para recibir notificaciones de solicitudes completadas y canceladas. |
| [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) | Enumera las **interfaces IPortableDeviceConnector.**                                                                 |
| [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)           | Admite métodos a los que las aplicaciones llaman para establecer conexiones a MTP Bluetooth dispositivos.                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 



