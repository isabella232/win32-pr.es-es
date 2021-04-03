---
description: Interfaces de conexión de MTP/Bluetooth
ms.assetid: 7bbd5fe3-85f1-4f0a-9d3e-22746bd23aae
title: Interfaces de conexión de MTP/Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e5194b8a6ababc05c36590ef30ae19ab185efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083305"
---
# <a name="mtpbluetooth-connection-interfaces"></a>Interfaces de conexión de MTP/Bluetooth

Las siguientes interfaces permiten a las aplicaciones enumerar y conectarse solo a los dispositivos que admiten el protocolo de transferencia multimedia (MTP) a través de Bluetooth (MTP/Bluetooth). El controlador de WPD, la colección y las interfaces de cliente no están restringidos al protocolo MTP/Bluetooth.



| Interfaz                                                              | Descripción                                                                                                         |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**IConnectionRequestCallback**](iconnectionrequestcallback.md)       | Define un método de devolución de llamada único que las aplicaciones usan para recibir la notificación de las solicitudes completadas y canceladas. |
| [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) | Enumera las interfaces de **IPortableDeviceConnector** .                                                                 |
| [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)           | Admite métodos que las aplicaciones llaman para establecer conexiones con dispositivos Bluetooth MTP.                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 



