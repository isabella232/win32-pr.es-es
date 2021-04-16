---
title: Tipos de datos de la API del servidor HTTP versión 1,0
description: La API del servidor HTTP usa varios tipos de identificador de propósito especial declarados en el archivo de encabezado HTTP. h como enteros de 64 bits sin signo.
ms.assetid: bec1d41e-0c80-49bc-84e1-b16c409cd0f3
keywords:
- HTTP_CONNECTION_ID tipo HTTP
- HTTP_RAW_CONNECTION_ID tipo HTTP
- HTTP_REQUEST_ID tipo HTTP
- HTTP_URL_CONTEXT tipo HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681e24c06334a9010287e2084d9d6a04428ca6a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685616"
---
# <a name="http-server-api-version-10-data-types"></a>Tipos de datos de la API del servidor HTTP versión 1,0

La API del servidor HTTP usa varios tipos de identificador de propósito especial declarados en el archivo de encabezado HTTP. h como enteros de 64 bits sin signo (**ULONGLONGs**):

-   \_identificador de conexión HTTP \_
-   \_identificador de conexión http sin formato \_ \_
-   \_identificador de solicitud HTTP \_
-   \_contexto de URL http \_

Una aplicación no debe intentar generar o modificar ningún identificador que pertenezca a uno de estos tipos.

 

 




