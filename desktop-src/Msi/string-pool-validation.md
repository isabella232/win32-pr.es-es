---
description: El Windows Installer almacena todas las cadenas de base de datos en un único grupo de cadenas compartidas para reducir el tamaño de la base de datos y mejorar el rendimiento.
ms.assetid: b627f3da-3545-4c1a-85b0-d8845fdac621
title: Validación de String-Pool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb544b5c76026846f7e8b8f6f331195426ab55c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155124"
---
# <a name="string-pool-validation"></a><span data-ttu-id="1c432-103">Validación de String-Pool</span><span class="sxs-lookup"><span data-stu-id="1c432-103">String-Pool Validation</span></span>

<span data-ttu-id="1c432-104">El Windows Installer almacena todas las cadenas de base de datos en un único grupo de cadenas compartidas para reducir el tamaño de la base de datos y mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="1c432-104">The Windows Installer stores all database strings in a single shared string pool to reduce the size of the database and to improve performance.</span></span> <span data-ttu-id="1c432-105">El único medio para validar el grupo de cadenas es usar la herramienta MsiInfo que se encuentra en el SDK de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1c432-105">The only means of validating the string pool is to use the MsiInfo tool found in the Windows Installer SDK.</span></span>

<span data-ttu-id="1c432-106">La comprobación del grupo de cadenas consta de dos comprobaciones principales:</span><span class="sxs-lookup"><span data-stu-id="1c432-106">String pool verification consists of two main checks:</span></span>

-   [<span data-ttu-id="1c432-107">Pruebas de cadenas DBCS</span><span class="sxs-lookup"><span data-stu-id="1c432-107">DBCS string tests</span></span>](#dbcs-string-tests)
-   [<span data-ttu-id="1c432-108">Comprobación del recuento de referencias</span><span class="sxs-lookup"><span data-stu-id="1c432-108">Reference count verification</span></span>](#reference-count-verification)

## <a name="dbcs-string-tests"></a><span data-ttu-id="1c432-109">Pruebas de cadenas DBCS</span><span class="sxs-lookup"><span data-stu-id="1c432-109">DBCS String Tests</span></span>

<span data-ttu-id="1c432-110">Las pruebas de cadenas DBCS examinan cada cadena de la base de datos para ver si hay dos criterios: en el caso de los paquetes con una página de códigos neutra marcada, si alguno de los caracteres es un carácter extendido (mayor que 127), la cadena se marca y se muestra un mensaje que indica que la página de códigos de la base de datos no es válida, ya que estos caracteres requieren</span><span class="sxs-lookup"><span data-stu-id="1c432-110">The DBCS string tests scan each string in the database for two criteria: For packages with a neutral code page marked, if any character is an extended character (greater than 127), the string is flagged and a message is displayed saying that the code page of the database is invalid because these characters require a specific code page to be rendered consistently on all systems.</span></span>

<span data-ttu-id="1c432-111">Si la base de datos tiene una página de códigos, se examina cada cadena para detectar un indicador DBCS no válido.</span><span class="sxs-lookup"><span data-stu-id="1c432-111">If the database has a code page, each string is scanned for an invalid DBCS indicator.</span></span> <span data-ttu-id="1c432-112">Si una cadena no neutra se ha marcado incorrectamente, los caracteres no se representarán correctamente.</span><span class="sxs-lookup"><span data-stu-id="1c432-112">If a non-neutral string has been improperly marked, the characters will not render correctly.</span></span> <span data-ttu-id="1c432-113">(Esto se debe normalmente al forzar la página de códigos a un valor determinado mediante el \_ Tabla ForceCodepage con cadenas no neutras que ya están en la base de datos.) Tenga en cuenta que esta comprobación requiere que la página de códigos de la base de datos esté instalada en el sistema.</span><span class="sxs-lookup"><span data-stu-id="1c432-113">(This is most commonly caused by forcing the code page to a particular value using the \_ForceCodepage table with non-neutral strings already in the database.) Note that this check requires that the code page of the database be installed on the system.</span></span>

<span data-ttu-id="1c432-114">Si hay un problema de página de códigos, el usuario puede corregir el error mediante la \_ tabla ForceCodepage para forzar a la página de códigos de la base de datos al valor adecuado.</span><span class="sxs-lookup"><span data-stu-id="1c432-114">If there is a code page problem, the user may fix the error by using the \_ForceCodepage table to force the code page of the database to the appropriate value.</span></span> <span data-ttu-id="1c432-115">Para obtener más información, vea [control de páginas de códigos](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="1c432-115">For more information, see [Code Page Handling](code-page-handling-windows-installer-.md).</span></span>

## <a name="reference-count-verification"></a><span data-ttu-id="1c432-116">Comprobación del recuento de referencias</span><span class="sxs-lookup"><span data-stu-id="1c432-116">Reference Count Verification</span></span>

<span data-ttu-id="1c432-117">Para comprobar los recuentos de referencias de todas las cadenas, se examinan los valores de cadena de cada tabla, se mantiene un recuento de cada cadena distinta y el resultado se compara con el recuento de referencias almacenado en el grupo de cadenas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="1c432-117">To verify the reference counts of all strings, every table is scanned for string values, a count of each distinct string is kept, and the result is compared to the stored reference count in the database string pool.</span></span>

<span data-ttu-id="1c432-118">Si hay un problema de recuento de referencias de cadena, el usuario debe exportar inmediatamente cada tabla de la base de datos mediante [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), crear una nueva base de datos e importar las tablas en la nueva base de datos mediante [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="1c432-118">If there is a string reference count problem, the user should immediately export each table of the database using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), create a new database, and import the tables into the new database using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="1c432-119">La nueva base de datos tiene el mismo contenido que la antigua, pero los recuentos de referencias de cadena son correctos.</span><span class="sxs-lookup"><span data-stu-id="1c432-119">The new database then has the same content as the old database, but the string reference counts are correct.</span></span> <span data-ttu-id="1c432-120">Agregar o eliminar datos de una base de datos con un grupo de cadenas dañado puede aumentar el daño de la base de datos y la pérdida de datos, por lo que realizar estos pasos rápidamente es importante para evitar la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="1c432-120">Adding or deleting data from a database with a corrupt string pool can increase corruption of the database and loss of data, so taking these steps quickly is important to prevent further data loss.</span></span>

<span data-ttu-id="1c432-121">Al volver a generar las bases de datos, recuerde insertar los flujos y almacenamientos necesarios en la nueva base de datos (consulte [ \_ tabla](-storages-table.md)de [ \_ transmisiones](-streams-table.md) y tablas de almacenamiento) y tener en cuenta los problemas de las páginas de códigos.</span><span class="sxs-lookup"><span data-stu-id="1c432-121">When rebuilding databases, remember to embed any necessary storages and streams in the new database (see [\_Streams Table](-streams-table.md) and [\_Storages Table](-storages-table.md)) and be aware of code page issues.</span></span> <span data-ttu-id="1c432-122">Recuerde también establecer cada una de las propiedades de [flujo de información de Resumen](summary-information-stream.md) necesarias.</span><span class="sxs-lookup"><span data-stu-id="1c432-122">Also remember to set each of the necessary [Summary Information Stream](summary-information-stream.md) properties.</span></span>

 

 



