---
title: Configuración del proveedor de servicios de nombres del localizador de Microsoft
description: Puede cambiar el proveedor de servicio de nombres especificado editando el archivo de configuración Rpcreg. dat, que contiene los parámetros NSP y la configuración del protocolo RPC. Use un editor de texto para cambiar las entradas NSP.
ms.assetid: b499e40e-d38f-4e51-bbce-41af3ff12a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a5334436ce307030048a862f1375a91000b41e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357291"
---
# <a name="configuring-the-microsoft-locator-name-service-provider"></a>Configuración del proveedor de servicios de nombres del localizador de Microsoft

Puede cambiar el proveedor de servicio de nombres especificado editando el archivo de configuración Rpcreg. dat, que contiene los parámetros NSP y la configuración del protocolo RPC. Use un editor de texto para cambiar las entradas NSP.

**Para volver a configurar el proveedor de servicios de nombres del localizador de Microsoft**

1.  Abra el archivo Rpcreg. dat con un editor de texto.

    Rpcreg. dat está en el directorio raíz a menos que haya especificado una ruta de acceso diferente durante la instalación.

2.  Establezca los siguientes valores para las entradas del registro. 

    | Entrada del Registro                                         | Value                                                                                                                                                 |
    |--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
    | \\Protocolo Microsoft \\ RPC \\ NameService \\       | La secuencia de protocolos para el protocolo que está usando. El valor predeterminado es **ncacn \_ NP**.                                                                   |
    | Software \\ Microsoft \\ RPC \\ NameService \\ NetworkAddress | Nombre del equipo que ejecuta el localizador que usan los clientes durante las operaciones de búsqueda de servicio de nombres. El valor predeterminado es el controlador de dominio principal. |
    | \\Punto de conexión de Microsoft \\ RPC \\ NameService \\ de software       | Nombre del punto de conexión utilizado por el servicio de nombres. El valor predeterminado es el \\ localizador de canalización \\ .                                                                    |

    

     

3.  Guarde y cierre el archivo.

 

 




