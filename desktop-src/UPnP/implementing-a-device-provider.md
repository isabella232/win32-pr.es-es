---
title: Implementación de un proveedor de dispositivos
description: Para implementar un proveedor de dispositivos, cree un objeto que exponga la interfaz IUPnPDeviceProvider.
ms.assetid: 3ba1200d-68d4-4f03-805c-7fff2d76b16f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19823357389a513a095081ce6ca79176af79897273274cc1f0e59a56e29b339f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999655"
---
# <a name="implementing-a-device-provider"></a>Implementación de un proveedor de dispositivos

Para implementar un proveedor de dispositivos, cree un objeto que exponga la [**interfaz IUPnPDeviceProvider.**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) Este objeto debe registrarse con el host del dispositivo mediante el [**método IUPnPRegistrar::RegisterDeviceProvider.**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) Este método toma los parámetros siguientes:

-   Nombre del proveedor, que debe ser único en el equipo.
-   ProgID de la clase que implementa el proveedor de dispositivos.
-   Cadena de inicialización que se pasa al proveedor de dispositivos cuando se inicia.
-   Un identificador de contenedor. Un identificador de contenedor es una cadena que identifica el grupo al que pertenece el dispositivo. Todos los dispositivos con el mismo identificador de contenedor se hospedan en el mismo proceso.

 

 




