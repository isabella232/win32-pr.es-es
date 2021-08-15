---
description: El aislamiento es el objetivo principal de un entorno de ejecución de AppContainer.
ms.assetid: 13C579F9-7F9F-4602-9B03-08CD820C3BBA
title: Aislamiento de AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe42b12698983bc3a90af06be2bb45992013b52e16e6f7de37083d6c92b9422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784711"
---
# <a name="appcontainer-isolation"></a>Aislamiento de AppContainer

El aislamiento es el objetivo principal de un entorno de ejecución de AppContainer. Al aislar una aplicación de recursos innecesarios y otras aplicaciones, se minimizan las oportunidades de manipulación malintencionada. La concesión de acceso basada en privilegios mínimos impide que las aplicaciones y los usuarios accedan a recursos más allá de sus derechos. El control del acceso a los recursos protege el proceso, el dispositivo y la red.

La mayoría de las vulnerabilidades Windows comienzan con la aplicación. Algunos ejemplos comunes incluyen la salida de una aplicación de su explorador o el envío de un documento no Internet Explorer, así como la explotación de complementos, como flash. Entre más se puedan aislar estas aplicaciones en un AppContainer, más seguro serán el dispositivo y los recursos. Incluso si se aprovecha la vulnerabilidad de una aplicación, la aplicación no puede acceder a recursos más allá de lo que se concede a AppContainer. Las aplicaciones malintencionadas no pueden asumir el resto de la máquina.

## <a name="credential-isolation"></a>Aislamiento de credenciales

Al administrar la identidad y las credenciales, AppContainer impide el uso de credenciales de usuario para obtener acceso a los recursos o iniciar sesión en otros entornos. El entorno de AppContainer crea un identificador que usa las identidades combinadas del usuario y la aplicación, por lo que las credenciales son únicas para cada emparejamiento de usuario y aplicación, y la aplicación no puede suplantar al usuario.

## <a name="device-isolation"></a>Aislamiento de dispositivos

Aislar la aplicación de los recursos del dispositivo, como sensores pasivos (cámara, micrófono, GPS) y bombas de dinero (3G/4G, teléfono telefónico), el entorno de AppContainer impide que la aplicación aproveche de forma malintencionada el dispositivo. Estos recursos están bloqueados de forma predeterminada y se les puede conceder acceso según sea necesario. En algunos casos, estos recursos están aún más protegidos por "agentes". Algunos recursos, como el teclado y el mouse, siempre están disponibles para AppContainer y la aplicación residentes.

## <a name="file-isolation"></a>Aislamiento de archivos

Al controlar el acceso al registro y al archivo, el entorno AppContainer impide que la aplicación modifique los archivos que no debería. Se puede conceder acceso de lectura y escritura a archivos persistentes y claves del Registro específicos. El acceso de solo lectura está menos restringido. Una aplicación siempre tiene acceso a los archivos residentes en memoria creados específicamente para ese AppContainer.

## <a name="network-isolation"></a>Aislamiento de red

Al aislar la aplicación de los recursos de red más allá de los asignados específicamente, AppContainer impide que la aplicación "escape" su entorno y aproveche de forma malintencionada los recursos de red. Se puede conceder acceso granular para el acceso a Internet, el acceso a la intranet y actuar como servidor.

## <a name="process-isolation"></a>Aislamiento de procesos

Al espacio aislado de los objetos de kernel de la aplicación, el entorno AppContainer impide que la aplicación influye en otros procesos de aplicación o se ve afectado por ellos. Esto evita que una aplicación contenida correctamente daña otros procesos en caso de una excepción.

## <a name="window-isolation"></a>Aislamiento de ventana

Al aislar la aplicación de otras ventanas, el entorno AppContainer impide que la aplicación afecte a otras interfaces de aplicación.

 

 



