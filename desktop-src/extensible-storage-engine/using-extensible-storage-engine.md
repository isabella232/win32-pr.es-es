---
description: Más información acerca de cómo usar el motor de almacenamiento extensible
title: Usar el motor de almacenamiento extensible
TOCTitle: Using Extensible Storage Engine
ms:assetid: d0249519-4c7c-49c1-9c80-b3cae2537d61
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294096(v=EXCHG.10)
ms:contentKeyID: 32765711
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 636c3fa96692b8c48f9a175b5fa7d34c53314e1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715672"
---
# <a name="using-extensible-storage-engine"></a><span data-ttu-id="8f875-103">Usar el motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="8f875-103">Using Extensible Storage Engine</span></span>


<span data-ttu-id="8f875-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8f875-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="using-extensible-storage-engine"></a><span data-ttu-id="8f875-105">Usar el motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="8f875-105">Using Extensible Storage Engine</span></span>

<span data-ttu-id="8f875-106">Esta sección contiene información general sobre cómo usar las siguientes partes de la API de ESE.</span><span class="sxs-lookup"><span data-stu-id="8f875-106">This section contains general information about how to use the following parts of the ESE API.</span></span>

  - [<span data-ttu-id="8f875-107">Columnas</span><span class="sxs-lookup"><span data-stu-id="8f875-107">Columns</span></span>](./columns.md)

  - [<span data-ttu-id="8f875-108">Indexación en la tabla</span><span class="sxs-lookup"><span data-stu-id="8f875-108">Indexing in the Table</span></span>](./indexing-in-the-table.md)

  - [<span data-ttu-id="8f875-109">Crear bases de datos</span><span class="sxs-lookup"><span data-stu-id="8f875-109">Creating Databases</span></span>](./creating-databases.md)

  - [<span data-ttu-id="8f875-110">Transactions</span><span class="sxs-lookup"><span data-stu-id="8f875-110">Transactions</span></span>](./transactions.md)

  - [<span data-ttu-id="8f875-111">Errores de ESE</span><span class="sxs-lookup"><span data-stu-id="8f875-111">ESE Errors</span></span>](./extensible-storage-engine-errors.md)

  - [<span data-ttu-id="8f875-112">Archivos de ESE</span><span class="sxs-lookup"><span data-stu-id="8f875-112">ESE Files</span></span>](./extensible-storage-engine-files.md)

<span data-ttu-id="8f875-113">Los archivos de código fuente del programa deben incluir el archivo de encabezado esent. h para tener acceso a los prototipos de función y las definiciones de estructura de la API del motor de almacenamiento extensible.</span><span class="sxs-lookup"><span data-stu-id="8f875-113">Your program source files should include the esent.h header file to access function prototypes and structure definitions for the Extensible Storage Engine API.</span></span> <span data-ttu-id="8f875-114">Los desarrolladores pueden utilizar el archivo de biblioteca esent. lib para compilar aplicaciones que usan la API del motor de almacenamiento extensible.</span><span class="sxs-lookup"><span data-stu-id="8f875-114">Developers can use the esent.lib library file to build applications that use the Extensible Storage Engine API.</span></span> <span data-ttu-id="8f875-115">En tiempo de ejecución, las aplicaciones se vinculan a la esent.dll.</span><span class="sxs-lookup"><span data-stu-id="8f875-115">At runtime, applications link to the esent.dll.</span></span>
