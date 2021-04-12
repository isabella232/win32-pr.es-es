---
description: Antes de trabajar con una base de datos, primero debe obtener un identificador.
ms.assetid: 53cf73bc-4d52-471c-8384-46d106a36e38
title: Obtener un identificador de base de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5f37f1abd329d0c51b00839d43ef85784fdad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155285"
---
# <a name="obtaining-a-database-handle"></a><span data-ttu-id="d96bc-103">Obtener un identificador de base de datos</span><span class="sxs-lookup"><span data-stu-id="d96bc-103">Obtaining a Database Handle</span></span>

<span data-ttu-id="d96bc-104">Antes de trabajar con una base de datos, primero debe obtener un identificador.</span><span class="sxs-lookup"><span data-stu-id="d96bc-104">Before working with a database you must first obtain a handle to it.</span></span>

<span data-ttu-id="d96bc-105">**Para obtener acceso a información sobre una base de datos del instalador**</span><span class="sxs-lookup"><span data-stu-id="d96bc-105">**To access information about an installer database**</span></span>

1.  <span data-ttu-id="d96bc-106">Obtenga un identificador de la base de datos de una de las dos maneras siguientes:</span><span class="sxs-lookup"><span data-stu-id="d96bc-106">Obtain a handle to the database in one of two ways:</span></span>
    -   <span data-ttu-id="d96bc-107">Si hay una instalación en curso, obtenga un identificador de la base de datos activa mediante una llamada a la función [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) .</span><span class="sxs-lookup"><span data-stu-id="d96bc-107">If an installation is in progress, get a handle to the active database by calling the [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) function.</span></span>
    -   <span data-ttu-id="d96bc-108">Si una instalación no está en curso, abra cualquier base de datos especificada llamando a la función [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) .</span><span class="sxs-lookup"><span data-stu-id="d96bc-108">If an installation is not in progress, open any specified database by calling the [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) function.</span></span>
2.  <span data-ttu-id="d96bc-109">Una vez abierta la base de datos, puede llamar a funciones para obtener información sobre la base de datos o para manipular la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d96bc-109">After the database has been opened, you can call functions to obtain information about the database or to manipulate the database.</span></span>
    -   <span data-ttu-id="d96bc-110">Cree un objeto de **vista** y especifique una consulta SQL de la base de datos abierta mediante una llamada a la función [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) .</span><span class="sxs-lookup"><span data-stu-id="d96bc-110">Create a **View** object and specify a SQL query of the open database by calling the [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) function.</span></span>
    -   <span data-ttu-id="d96bc-111">Obtener un registro que contenga todas las claves principales de una tabla especificada en la base de datos abierta mediante una llamada a la función [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) .</span><span class="sxs-lookup"><span data-stu-id="d96bc-111">Obtain a record that contains all primary keys of a specified table in the open database by calling the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function.</span></span>
    -   <span data-ttu-id="d96bc-112">Compruebe el estado actual de una base de datos abierta mediante una llamada a la función [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) .</span><span class="sxs-lookup"><span data-stu-id="d96bc-112">Check the current state of an open database by calling the [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) function.</span></span> <span data-ttu-id="d96bc-113">Con la función **MsiGetDatabaseState** , puede determinar el estado de lectura y escritura de una base de datos o si el identificador es válido.</span><span class="sxs-lookup"><span data-stu-id="d96bc-113">With the **MsiGetDatabaseState** function, you can determine the read/write status for a database or if the handle is valid.</span></span>

 

 



