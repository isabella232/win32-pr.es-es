---
title: Error Logging in the HTTP Server API
description: La API de servidor HTTP controla algunos tipos de errores en lugar de pasarse a una aplicación para su control, ya que la frecuencia de estos errores podría desbordar un registro de eventos o un controlador de aplicaciones.
ms.assetid: b919a718-e20b-4f34-a02e-bc028f8c32c7
keywords:
- API de servidor HTTP, registro de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c92c071929b61020b456d8ecabc81ebc0f05503c2f385b235afc323cf8dea33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130685"
---
# <a name="error-logging-in-the-http-server-api"></a>Error Logging in the HTTP Server API

La API de servidor HTTP controla algunos tipos de errores en lugar de pasarse a una aplicación para su control, ya que la frecuencia de estos errores podría desbordar un registro de eventos o un controlador de aplicaciones.

En los tres temas siguientes se describen los distintos aspectos del registro de errores de la API del servidor HTTP:

-   [Configuración](configuring-http-server-api-error-logging.md) La configuración del Registro controla si la API del servidor HTTP registra errores, el tamaño máximo permitido de los archivos de registro y dónde se guardan los archivos de registro.
-   [Formato de archivo de registro](format-of-the-http-server-api-error-logs.md) La API del servidor HTTP crea archivos de registro que cumplen las convenciones de archivo de registro de World Wide Web Consortium (W3C) y se pueden analizar mediante herramientas estándar. Sin embargo, a diferencia de los archivos de registro W3C, los archivos de registro de LA API del servidor HTTP no contienen nombres de las columnas.
-   [Tipos de errores registrados](types-of-errors-logged-by-the-http-server-api.md) La API del servidor HTTP registra una variedad de errores comunes.

 

 




