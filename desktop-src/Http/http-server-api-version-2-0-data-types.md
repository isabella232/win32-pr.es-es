---
title: Tipos de datos de LA API del servidor HTTP versión 2.0
description: Tipos de datos de LA API del servidor HTTP versión 2.0
ms.assetid: 13a0cac9-9e75-4350-a523-5ad9a57caad7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a347b58a97ad89e499136c07f85e18ee2ce1bddc31b5c6d67b8f14a2348a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950774"
---
# <a name="http-server-api-version-20-data-types"></a>Tipos de datos de LA API del servidor HTTP versión 2.0

La API del servidor HTTP usa varios tipos de identificadores de propósito especial declarados en el encabezado Http.h como se muestra a continuación:

-   **USHORT** HTTP \_ SERVICE \_ CONFIG \_ TIMEOUT \_ PARAM, \* PHTTP \_ SERVICE \_ CONFIG \_ TIMEOUT \_ PARAM
-   **ULONGLONG** HTTP \_ OPAQUE \_ ID, \* PHTTP \_ OPAQUE \_ ID
-   **HTTP \_ OPAQUE \_ ID** HTTP \_ REQUEST \_ ID, \* PHTTP \_ REQUEST \_ ID
-   **HTTP \_ OPAQUE \_ ID** HTTP \_ CONNECTION \_ ID, \* PHTTP \_ CONNECTION \_ ID
-   **HTTP \_ OPAQUE \_ ID** HTTP \_ RAW \_ CONNECTION \_ ID, \* PHTTP \_ RAW \_ CONNECTION \_ ID
-   **USHORT** HTTP \_ SERVICE \_ CONFIG \_ TIMEOUT \_ PARAM, \* PHTTP \_ SERVICE \_ CONFIG \_ TIMEOUT \_ PARAM

Una aplicación no debe intentar generar ni modificar ningún identificador que pertenezca a uno de estos tipos.

 

 




