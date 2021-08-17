---
title: Tipos de datos de LA API del servidor HTTP versión 1.0
description: La API del servidor HTTP usa varios tipos de identificadores de propósito especial declarados en el archivo de encabezado Http.h como enteros de 64 bits sin signo.
ms.assetid: bec1d41e-0c80-49bc-84e1-b16c409cd0f3
keywords:
- HTTP_CONNECTION_ID tipo HTTP
- HTTP_RAW_CONNECTION_ID tipo HTTP
- HTTP_REQUEST_ID tipo HTTP
- HTTP_URL_CONTEXT tipo HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151ef975470ca21c6e82e5bc7bd7bd8b99a70573385375e8552b6660ce78f631
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950804"
---
# <a name="http-server-api-version-10-data-types"></a>Tipos de datos de LA API del servidor HTTP versión 1.0

La API del servidor HTTP usa varios tipos de identificadores de propósito especial declarados en el archivo de encabezado Http.h como enteros de 64 bits sin signo **(ULONGLONG**):

-   IDENTIFICADOR \_ DE CONEXIÓN \_ HTTP
-   IDENTIFICADOR \_ DE CONEXIÓN HTTP SIN \_ \_ PROCESAR
-   IDENTIFICADOR \_ DE SOLICITUD \_ HTTP
-   CONTEXTO \_ DE DIRECCIÓN URL \_ HTTP

Una aplicación no debe intentar generar ni modificar ningún identificador que pertenezca a uno de estos tipos.

 

 




