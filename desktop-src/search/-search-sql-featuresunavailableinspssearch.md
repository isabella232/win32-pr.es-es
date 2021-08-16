---
description: El lenguaje de consulta de Microsoft Windows Search se basa en Lenguaje de consulta estructurado (SQL); sin embargo, no busca en una base de datos relacional con tablas o índices definidos por el usuario.
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: SQL Características no disponibles en Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66adb175aa7fae799e0ad9b69916415f12c94ee984d276b5a2238ebb19ec2f06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716125"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a>SQL Características no disponibles en Microsoft Windows Search

El lenguaje de consulta de Microsoft Windows Search se basa en Lenguaje de consulta estructurado (SQL); sin embargo, no busca en una base de datos relacional con tablas o índices definidos por el usuario. Por este problema, no se aplican muchas instrucciones SQL estándar y características de sintaxis. A continuación se muestra una lista de las características SQL más importantes que no se admiten en Windows Search.


-   Instrucciones BATCH
-   Función COALESCE \_ TABLE
-   Función CONVERT (use en su lugar las funciones CAST)
-   CREATE VIEW, instrucción
-   Lenguaje de definición de datos
-   Instrucción DATASOURCE
-   Formatos de fecha y hora distintos de la marca de fecha y hora ISO
-   Instrucción DELETE
-   GRANT, instrucción
-   Esquema de información
-   Instrucción INSERT
-   OLE DB tipos de datos
-   SQL expresiones regulares estándar (use CONTAINS o LIKE en su lugar)
-   Parámetros para SQL consultas
-   Comparación de columnas relacionales
-   Encabezado de identificador de revisión
-   REVOKE, instrucción
-   Alias scope o números de revisión
-   SELECT ALL (quita los duplicados automáticamente)
-   Procedimientos almacenados
-   Expansión de documentos estructurados
-   UNION ALL
-   Palabra clave UNKNOWN
-   Instrucción UPDATE

Windows La búsqueda no admite el diccionario de sinónimos ni las palabras ruido.

 

 



