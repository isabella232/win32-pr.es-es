---
title: Tipos de datos de la API del servidor HTTP versión 2,0
description: Tipos de datos de la API del servidor HTTP versión 2,0
ms.assetid: 13a0cac9-9e75-4350-a523-5ad9a57caad7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670099f3303682f52fdc78397dc7f229577b94d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665707"
---
# <a name="http-server-api-version-20-data-types"></a>Tipos de datos de la API del servidor HTTP versión 2,0

La API del servidor HTTP usa varios tipos de identificador de propósito especial declarados en el encabezado HTTP. h como se indica a continuación:

-   **USHORT** \_ \_ \_ \_ parámetro de tiempo de espera de configuración de servicio http, \* PHTTP de tiempo de espera de \_ configuración de servicio \_ \_ \_
-   **ULONGLONG** \_identificador opaco \_ de http \* , \_ \_ ID. de PHTTP opaco
-   **Http \_ identificador \_** de solicitud HTTP de ID. opaco \_ \_ , \* \_ \_ ID. de solicitud de PHTTP
-   **Http \_ identificador \_** \_ de conexión HTTP \_ de identificador opaco, \* \_ ID. de conexión de PHTTP \_
-   **Http \_ identificador \_ opaco** identificador \_ de conexión http sin formato, ID. \_ \_ de \* \_ conexión sin formato de PHTTP \_ \_
-   **USHORT** \_ \_ \_ \_ parámetro de tiempo de espera de configuración de servicio http, \* PHTTP de tiempo de espera de \_ configuración de servicio \_ \_ \_

Una aplicación no debe intentar generar o modificar ningún identificador que pertenezca a uno de estos tipos.

 

 




