---
description: El aislamiento es el objetivo principal de un entorno de ejecución de AppContainer.
ms.assetid: 13C579F9-7F9F-4602-9B03-08CD820C3BBA
title: Aislamiento de AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82fec44fd3d6eb9495370c42e52726ceb0f63806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278119"
---
# <a name="appcontainer-isolation"></a>Aislamiento de AppContainer

El aislamiento es el objetivo principal de un entorno de ejecución de AppContainer. Al aislar una aplicación de recursos innecesarios y otras aplicaciones, se minimizan las oportunidades de manipulación malintencionada. Conceder acceso basado en privilegios mínimos evita que las aplicaciones y los usuarios tengan acceso a recursos más allá de sus derechos. Controlar el acceso a los recursos protege el proceso, el dispositivo y la red.

La mayoría de las vulnerabilidades en Windows se inician con la aplicación. Algunos ejemplos comunes incluyen la interrupción de la aplicación del explorador o el envío de un documento incorrecto a Internet Explorer, así como la explotación de complementos, como Flash. Cuanto más se puedan aislar estas aplicaciones en un AppContainer, más seguros serán el dispositivo y los recursos. Incluso si se aprovecha una vulnerabilidad en una aplicación, la aplicación no puede acceder a los recursos más allá de lo que se le concede a AppContainer. Las aplicaciones malintencionadas no pueden asumir el resto del equipo.

## <a name="credential-isolation"></a>Aislamiento de credenciales

Administrar la identidad y las credenciales, el AppContainer impide el uso de las credenciales de usuario para obtener acceso a los recursos o iniciar sesión en otros entornos. El entorno de AppContainer crea un identificador que usa las identidades combinadas del usuario y la aplicación, por lo que las credenciales son únicas para cada emparejamiento de usuario y aplicación, y la aplicación no puede suplantar al usuario.

## <a name="device-isolation"></a>Aislamiento de dispositivos

Aislar la aplicación de recursos de dispositivo, como sensores pasivos (cámara, micrófono, GPS) y bombas de dinero (3G/4G, dial Phone) el entorno de AppContainer impide que la aplicación aproveche de forma malintencionada el dispositivo. Estos recursos están bloqueados de forma predeterminada y se puede conceder acceso según sea necesario. En algunos casos, estos recursos están más protegidos por ' agentes '. Algunos recursos, como el teclado y el mouse, siempre están disponibles para el AppContainer y la aplicación residente.

## <a name="file-isolation"></a>Aislamiento de archivos

Al controlar el acceso al archivo y al registro, el entorno AppContainer evita que la aplicación modifique los archivos que no debería. El acceso de lectura y escritura se puede conceder a archivos persistentes específicos y claves del registro. El acceso de solo lectura es menos restringido. Una aplicación siempre tiene acceso a los archivos residentes en memoria creados específicamente para ese AppContainer.

## <a name="network-isolation"></a>Aislamiento de red

Al aislar la aplicación de los recursos de red más allá de los asignados específicamente, AppContainer evita que la aplicación ' escape ' a su entorno y aproveche de forma malintencionada los recursos de red. Se puede conceder acceso granular para el acceso a Internet, el acceso a la intranet y la actuación como servidor.

## <a name="process-isolation"></a>Aislamiento de procesos

Espacio aislado de los objetos de kernel de la aplicación, el entorno de AppContainer evita que la aplicación pueda influir en otros procesos de la aplicación, o influir en ellos. Esto evita que una aplicación contenida correctamente dañe otros procesos en caso de que se produzca una excepción.

## <a name="window-isolation"></a>Aislamiento de ventanas

Aislar la aplicación de otras ventanas, el entorno de AppContainer evita que la aplicación afecte a otras interfaces de aplicación.

 

 



