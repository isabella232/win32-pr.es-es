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
# <a name="sql-log-file-schema"></a><span data-ttu-id="f1c60-103">Esquema del archivo de registro de SQL</span><span class="sxs-lookup"><span data-stu-id="f1c60-103">SQL Log File Schema</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f1c60-104">La compatibilidad de PDH con las bases de datos SQL de ODBC puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="f1c60-104">PDH support for ODBC SQL databases may be altered or unavailable in the future.</span></span>

<span data-ttu-id="f1c60-105">Las aplicaciones pueden usar los datos del contador de rendimiento de lectura y escritura de las API de PDH en bases de datos ODBC SQL compatibles y, a continuación, realizar un procesamiento posterior a través de consultas SQL.</span><span class="sxs-lookup"><span data-stu-id="f1c60-105">Applications can use PDH APIs read and write performance counter data in compatible ODBC SQL databases and then perform further processing through SQL queries.</span></span> <span data-ttu-id="f1c60-106">En esta sección se describe el esquema de SQL que se usa para almacenar los contadores de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f1c60-106">This section describes the SQL schema used to store performance counters.</span></span> <span data-ttu-id="f1c60-107">Puede usar esta información para crear vistas e informes personalizados.</span><span class="sxs-lookup"><span data-stu-id="f1c60-107">You can use this information to create custom views and reports.</span></span> <span data-ttu-id="f1c60-108">El esquema consta de las siguientes tres tablas:</span><span class="sxs-lookup"><span data-stu-id="f1c60-108">The schema consists of the following three tables:</span></span>

- [<span data-ttu-id="f1c60-109">**Datos**</span><span class="sxs-lookup"><span data-stu-id="f1c60-109">**CounterData**</span></span>](counterdata.md)
- [<span data-ttu-id="f1c60-110">**Detalles**</span><span class="sxs-lookup"><span data-stu-id="f1c60-110">**CounterDetails**</span></span>](counterdetails.md)
- [<span data-ttu-id="f1c60-111">**DisplayToID**</span><span class="sxs-lookup"><span data-stu-id="f1c60-111">**DisplayToID**</span></span>](displaytoid.md)

> [!NOTE]
> <span data-ttu-id="f1c60-112">La compatibilidad de PDH con las bases de datos SQL de ODBC solo funciona con los controladores ODBC SQL compatibles con [las extensiones de copia masiva (BCP)](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions).</span><span class="sxs-lookup"><span data-stu-id="f1c60-112">PDH support for ODBC SQL databases only works with ODBC SQL drivers that support [Bulk Copy (BCP) Extensions](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions).</span></span>
