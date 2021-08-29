---
title: Configuración del proveedor de servicios de nombres de localizador de Microsoft
description: Puede cambiar el proveedor de servicios de nombre que especificó editando el archivo de configuración Rpcreg.dat, que contiene los parámetros NSP y la configuración del protocolo RPC. Use un editor de texto para cambiar las entradas de NSP.
ms.assetid: b499e40e-d38f-4e51-bbce-41af3ff12a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 413d7654096b2a7eda74d28b019cac73afe1d0eb182d48d9c0eda601dd2c87c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931610"
---
# <a name="configuring-the-microsoft-locator-name-service-provider"></a>Configuración del proveedor de servicios de nombres de localizador de Microsoft

Puede cambiar el proveedor de servicios de nombre que especificó editando el archivo de configuración Rpcreg.dat, que contiene los parámetros NSP y la configuración del protocolo RPC. Use un editor de texto para cambiar las entradas de NSP.

**Para volver a configurar el proveedor de servicios de nombre de localizador de Microsoft**

1.  Abra el archivo Rpcreg.dat mediante un editor de texto.

    Rpcreg.dat se encuentra en el directorio raíz a menos que haya especificado una ruta de acceso diferente durante la instalación.

2.  Establezca los siguientes valores para las entradas del Registro. 

    | Entrada del Registro                                         | Value                                                                                                                                                 |
    |--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Software \\ Microsoft \\ RPC \\ NameService \\ Protocol       | Secuencia de protocolo para el protocolo que está usando. El valor predeterminado **es ncacn \_ np**.                                                                   |
    | Software \\ Microsoft \\ RPC \\ NameService \\ NetworkAddress | Nombre del equipo que ejecuta locator que usan los clientes durante las operaciones de búsqueda del servicio de nombres. El valor predeterminado es el controlador de dominio principal. |
    | Punto \\ de conexión de servicio de nombre RPC de Microsoft de \\ \\ \\ software       | Nombre del punto de conexión utilizado por el servicio de nombres. El valor predeterminado es \\ el localizador de \\ canalización.                                                                    |

    

     

3.  Guarde y cierre el archivo.

 

 




