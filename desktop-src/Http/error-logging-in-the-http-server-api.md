---
title: Error Logging in the HTTP Server API
description: La API del servidor HTTP controla algunos tipos de errores en lugar de devolverlos a una aplicación para controlarlos, ya que la frecuencia de estos errores podría inundar un registro de eventos o un controlador de aplicación.
ms.assetid: b919a718-e20b-4f34-a02e-bc028f8c32c7
keywords:
- API del servidor HTTP, registro de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d988d87a65c914625623c3f55d33a7f8cc9a4f94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685484"
---
# <a name="error-logging-in-the-http-server-api"></a>Error Logging in the HTTP Server API

La API del servidor HTTP controla algunos tipos de errores en lugar de devolverlos a una aplicación para controlarlos, ya que la frecuencia de estos errores podría inundar un registro de eventos o un controlador de aplicación.

En los siguientes tres temas se describen los distintos aspectos del registro de errores de la API del servidor HTTP:

-   [Configuración](configuring-http-server-api-error-logging.md) de Los valores del registro controlan si la API del servidor HTTP registra errores, el tamaño máximo permitido de los archivos de registro y dónde se guardan los archivos de registro.
-   [Formato del archivo de registro](format-of-the-http-server-api-error-logs.md) La API del servidor HTTP crea archivos de registro que cumplen las convenciones del archivo de registro del World Wide Web Consortium (W3C) y se pueden analizar mediante herramientas estándar. Sin embargo, a diferencia de los archivos de registro del W3C, los archivos de registro de la API del servidor HTTP no contienen los nombres de las columnas.
-   [Tipos de errores registrados](types-of-errors-logged-by-the-http-server-api.md) La API del servidor HTTP registra diversos errores comunes.

 

 




