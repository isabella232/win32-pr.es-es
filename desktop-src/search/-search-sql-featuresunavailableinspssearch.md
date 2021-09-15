---
description: El lenguaje de consulta de Microsoft Windows Search se basa en Lenguaje de consulta estructurado (SQL); sin embargo, no busca en una base de datos relacional con índices o tablas definidos por el usuario.
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: SQL Características no disponibles en Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cf0e082a10a7775ca2d880be6153b7d99b6bc7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572545"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a>SQL Características no disponibles en Microsoft Windows Search

El lenguaje de consulta de Microsoft Windows Search se basa en Lenguaje de consulta estructurado (SQL); sin embargo, no busca en una base de datos relacional con índices o tablas definidos por el usuario. Por este problema, no se SQL las instrucciones estándar y las características de sintaxis. A continuación se muestra una lista de las características de SQL más importantes que no se admiten en Windows Search.


-   Instrucciones BATCH
-   Función COALESCE \_ TABLE
-   Función CONVERT (use las funciones CAST en su lugar)
-   CREATE VIEW, instrucción
-   Lenguaje de definición de datos
-   Instrucción DATASOURCE
-   Formatos de fecha y hora distintos de marca de fecha y hora ISO
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

Windows La búsqueda no admite el diccionario de sinónimos ni las palabras ruidosas.

 

 



