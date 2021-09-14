---
description: Las aplicaciones pueden usar PDH para extraer contadores de rendimiento de SQL registros, o bien pueden extraer contadores con formato o sin formato directamente de la base de datos a través de SQL consultas.
ms.assetid: 89515dd9-2d65-4b19-bb7a-ef9e7d146caa
title: SQL Esquema de archivo de registro
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 33b988194a8fda4a99f713e0026aeaddb65e9c26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062875"
---
# <a name="sql-log-file-schema"></a>SQL Esquema de archivo de registro

> [!IMPORTANT]
> La compatibilidad de PDH con bases SQL odbc puede modificarse o no estar disponible en el futuro.

Las aplicaciones pueden usar las API de PDH para leer y escribir datos de contadores de rendimiento en bases de datos de SQL ODBC compatibles y, a continuación, realizar un procesamiento adicional a través de SQL consultas. En esta sección se describe el SQL que se usa para almacenar contadores de rendimiento. Puede usar esta información para crear vistas e informes personalizados. El esquema consta de las tres tablas siguientes:

- [**CounterData**](counterdata.md)
- [**CounterDetails**](counterdetails.md)
- [**DisplayToID**](displaytoid.md)

> [!NOTE]
> La compatibilidad de PDH con bases de SQL odbc solo funciona con controladores SQL ODBC que admiten extensiones de [copia masiva (BCP).](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions)
