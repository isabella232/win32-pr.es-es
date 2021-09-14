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
ms.openlocfilehash: 681e24c06334a9010287e2084d9d6a04428ca6a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266276"
---
# <a name="http-server-api-version-10-data-types"></a>Tipos de datos de LA API del servidor HTTP versión 1.0

La API del servidor HTTP usa varios tipos de identificadores de propósito especial declarados en el archivo de encabezado Http.h como enteros de 64 bits sin signo **(ULONGLONG):**

-   IDENTIFICADOR \_ DE CONEXIÓN \_ HTTP
-   IDENTIFICADOR \_ DE CONEXIÓN HTTP SIN \_ \_ PROCESAR
-   IDENTIFICADOR \_ DE SOLICITUD \_ HTTP
-   CONTEXTO \_ DE DIRECCIÓN URL \_ HTTP

Una aplicación no debe intentar generar ni modificar ningún identificador que pertenezca a uno de estos tipos.

 

 




