---
title: Implementación de un proveedor de dispositivos
description: Para implementar un proveedor de dispositivos, cree un objeto que exponga la interfaz IUPnPDeviceProvider.
ms.assetid: 3ba1200d-68d4-4f03-805c-7fff2d76b16f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb8cd2bea433b884bf6ddf3828fb148c726cd867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487026"
---
# <a name="implementing-a-device-provider"></a>Implementación de un proveedor de dispositivos

Para implementar un proveedor de dispositivos, cree un objeto que exponga la interfaz [**IUPnPDeviceProvider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) . Este objeto se debe registrar con el host del dispositivo mediante el método [**IUPnPRegistrar:: RegisterDeviceProvider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) . Este método toma los parámetros siguientes:

-   Nombre del proveedor, que debe ser único en el equipo.
-   Identificador de programa (ProgID) de la clase que implementa el proveedor de dispositivos.
-   Una cadena de inicialización que se pasa al proveedor de dispositivos cuando se inicia.
-   IDENTIFICADOR del contenedor. Un identificador de contenedor es una cadena que identifica el grupo al que pertenece el dispositivo. Todos los dispositivos con el mismo identificador de contenedor se hospedan en el mismo proceso.

 

 




