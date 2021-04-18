---
description: El lenguaje de consulta de Microsoft Windows Search se basa en Lenguaje de consulta estructurado (SQL); sin embargo, no busca en una base de datos relacional con tablas o índices definidos por el usuario.
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: Características de SQL no disponibles en Microsoft Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cf0e082a10a7775ca2d880be6153b7d99b6bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715003"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a>Características de SQL no disponibles en Microsoft Search

El lenguaje de consulta de Microsoft Windows Search se basa en Lenguaje de consulta estructurado (SQL); sin embargo, no busca en una base de datos relacional con tablas o índices definidos por el usuario. Por este motivo, no se aplican muchas de las instrucciones SQL estándar y las características de sintaxis. A continuación se muestra una lista de las características de SQL más importantes que no se admiten en Windows Search.


-   Instrucciones por lotes
-   Coalesce ( \_ función de tabla)
-   CONVERT (función) (usar en su lugar las funciones de conversión)
-   CREATE VIEW, instrucción
-   Lenguaje de definición de datos
-   DATASOURCE (instrucción)
-   Formatos de fecha y hora distintos de la marca de fecha y hora ISO
-   Instrucción DELETE
-   GRANT, instrucción
-   Esquema de información
-   Instrucción INSERT
-   OLE DB tipos de datos
-   Expresiones regulares de SQL estándar (use Contains o LIKE en su lugar)
-   Parámetros para consultas SQL
-   Comparación de columnas relacionales
-   Encabezado de ID. de revisión
-   REVOKE, instrucción
-   Alias de ámbito o números de revisión
-   SELECCIONAR todo (quita los duplicados automáticamente)
-   Procedimientos almacenados
-   Expansión de documentos estructurados
-   UNION ALL
-   Palabra clave UNKNOWN
-   Instrucción UPDATE

Windows Search no admite palabras irrelevantes y de sinónimos.

 

 



