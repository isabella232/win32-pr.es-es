---
description: Las aplicaciones pueden usar PDH para extraer contadores de rendimiento de los registros de SQL, o bien pueden extraer contadores con formato o sin formato directamente de la base de datos a través de consultas SQL.
ms.assetid: 89515dd9-2d65-4b19-bb7a-ef9e7d146caa
title: Esquema del archivo de registro de SQL
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 33b988194a8fda4a99f713e0026aeaddb65e9c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667242"
---
# <a name="sql-log-file-schema"></a>Esquema del archivo de registro de SQL

> [!IMPORTANT]
> La compatibilidad de PDH con las bases de datos SQL de ODBC puede modificarse o no estar disponible en el futuro.

Las aplicaciones pueden usar los datos del contador de rendimiento de lectura y escritura de las API de PDH en bases de datos ODBC SQL compatibles y, a continuación, realizar un procesamiento posterior a través de consultas SQL. En esta sección se describe el esquema de SQL que se usa para almacenar los contadores de rendimiento. Puede usar esta información para crear vistas e informes personalizados. El esquema consta de las siguientes tres tablas:

- [**Datos**](counterdata.md)
- [**Detalles**](counterdetails.md)
- [**DisplayToID**](displaytoid.md)

> [!NOTE]
> La compatibilidad de PDH con las bases de datos SQL de ODBC solo funciona con los controladores ODBC SQL compatibles con [las extensiones de copia masiva (BCP)](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions).
