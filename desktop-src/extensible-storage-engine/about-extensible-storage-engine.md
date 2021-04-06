---
description: 'Más información acerca de: acerca del motor de almacenamiento extensible'
title: Acerca del motor de almacenamiento extensible
TOCTitle: About Extensible Storage Engine
ms:assetid: 06d1526e-169d-4677-b409-2ed415287de6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269181(v=EXCHG.10)
ms:contentKeyID: 32765484
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 17e2277deaef54c04bf6a53a8464479fd67295a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000880"
---
# <a name="about-extensible-storage-engine"></a><span data-ttu-id="4477c-103">Acerca del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="4477c-103">About Extensible Storage Engine</span></span>


<span data-ttu-id="4477c-104">_**Se aplica a:** Exchange Server 2013 | Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4477c-104">_**Applies to:** Exchange Server 2013 | Windows | Windows Server_</span></span>

## <a name="about-extensible-storage-engine"></a><span data-ttu-id="4477c-105">Acerca del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="4477c-105">About Extensible Storage Engine</span></span>

<span data-ttu-id="4477c-106">El motor de almacenamiento extensible (ESE) es un motor de base de datos que almacena información en una secuencia lógica.</span><span class="sxs-lookup"><span data-stu-id="4477c-106">The extensible storage engine (ESE) is a database engine that stores information in a logical sequence.</span></span> <span data-ttu-id="4477c-107">La información se puede recuperar de forma secuencial o mediante el acceso a índices definidos.</span><span class="sxs-lookup"><span data-stu-id="4477c-107">Information can be retrieved either sequentially or by accessing defined indices.</span></span> <span data-ttu-id="4477c-108">Las actualizaciones de la base de datos se implementan con una transacción con el fin de garantizar operaciones seguras.</span><span class="sxs-lookup"><span data-stu-id="4477c-108">Updates to the database are implemented with a transaction in order to ensure secure operations.</span></span> <span data-ttu-id="4477c-109">ESE permite el acceso simultáneo a varias bases de datos, incluidas las bases de datos de archivos de registro de transacciones que se pueden utilizar para la recuperación del sistema.</span><span class="sxs-lookup"><span data-stu-id="4477c-109">ESE enables simultaneous access to multiple databases, including transaction-log file databases that can be used for system recovery.</span></span> <span data-ttu-id="4477c-110">ESE es escalable a aplicaciones grandes o pequeñas.</span><span class="sxs-lookup"><span data-stu-id="4477c-110">ESE is scalable to large or small applications.</span></span> <span data-ttu-id="4477c-111">Las siguientes características están disponibles con la interfaz de programación de aplicaciones (API) de ESE:</span><span class="sxs-lookup"><span data-stu-id="4477c-111">The following features are available with the ESE application programming interface (API):</span></span>

  - <span data-ttu-id="4477c-112">Copias de seguridad y restauración: una aplicación puede hacer copias coherentes del estado de los datos mientras está en línea y modificando activamente el estado de los datos.</span><span class="sxs-lookup"><span data-stu-id="4477c-112">Backup and restore: An application can make consistent copies of the data state while it is on-line and actively modifying data state.</span></span>

  - <span data-ttu-id="4477c-113">Navegación por el cursor: la aplicación puede navegar con el cursor para tener acceso a los datos de forma secuencial o mediante índices.</span><span class="sxs-lookup"><span data-stu-id="4477c-113">Cursor Navigation: The application can navigate with the cursor to access data either sequentially or by using indices.</span></span>

  - <span data-ttu-id="4477c-114">Base de datos: colección de tablas de las que se realiza una copia de seguridad y se restaura como una sola unidad.</span><span class="sxs-lookup"><span data-stu-id="4477c-114">Database: A collection of tables that are backed up and restored as a single unit.</span></span>

  - <span data-ttu-id="4477c-115">Registro y recuperación de bloqueos: la API de ESE garantiza que la coherencia de los datos definidos por la aplicación se respeta incluso en caso de que se produzca un bloqueo del sistema.</span><span class="sxs-lookup"><span data-stu-id="4477c-115">Logging and crash recovery: The ESE API ensures that application-defined data consistency is honored even in the event of a system crash.</span></span>

  - <span data-ttu-id="4477c-116">Tablas: estructura fundamental de la base de datos de ESE que se utiliza para almacenar los datos.</span><span class="sxs-lookup"><span data-stu-id="4477c-116">Tables: The fundamental structure of the ESE database that is used to store data.</span></span>

  - <span data-ttu-id="4477c-117">Transacción: el motor de base de datos ESE proporciona transacciones duraderas aisladas atómicas (ACID) que permiten a las aplicaciones recuperar datos únicamente de los Estados de datos confiables y mantiene la coherencia de los datos en caso de que se produzca una terminación de proceso inesperada o un cierre del sistema.</span><span class="sxs-lookup"><span data-stu-id="4477c-117">Transaction: The ESE database engine provides Atomic Consistent Isolated Durable (ACID) transactions that allow applications to retrieve data only from reliable data states and maintains data consistency in the event of an unexpected process termination or system shutdown.</span></span>

  - <span data-ttu-id="4477c-118">Escalable: la aplicación puede crear bases de datos de hasta 100 GB o tan pequeñas como 1 MB.</span><span class="sxs-lookup"><span data-stu-id="4477c-118">Scalable: The application can create databases as large as 100 GB or as small as 1MB.</span></span>

