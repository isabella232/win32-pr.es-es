---
description: Las aplicaciones pueden usar PDH para extraer contadores de rendimiento de SQL o pueden extraer contadores con formato o sin formato directamente de la base de datos a través de SQL consultas.
ms.assetid: 89515dd9-2d65-4b19-bb7a-ef9e7d146caa
title: SQL Esquema de archivo de registro
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: a95026c478094d8e71a44c2c57e65c2fa7044b00e982ea43187244838beed2ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143818"
---
# <a name="sql-log-file-schema"></a>SQL Esquema de archivo de registro

> [!IMPORTANT]
> La compatibilidad de PDH con bases SQL odbc puede modificarse o no estar disponible en el futuro.

Las aplicaciones pueden usar las API de PDH para leer y escribir datos de contadores de rendimiento en bases de datos odbc SQL compatibles y, a continuación, realizar un procesamiento adicional a través de SQL consultas. En esta sección se describe el SQL que se usa para almacenar contadores de rendimiento. Puede usar esta información para crear vistas e informes personalizados. El esquema consta de las tres tablas siguientes:

- [**CounterData**](counterdata.md)
- [**CounterDetails**](counterdetails.md)
- [**DisplayToID**](displaytoid.md)

> [!NOTE]
> La compatibilidad de PDH con bases de SQL odbc solo funciona con controladores odbc SQL que admiten extensiones de [copia masiva (BCP).](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions)
