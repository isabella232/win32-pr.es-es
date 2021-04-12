---
description: Las tablas del grupo tablas del sistema realizan un seguimiento de las tablas y columnas de la base de datos de instalación.
ms.assetid: d20be8b6-f456-4f90-aa9e-dc122c20d20c
title: Grupo tablas del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482333ec3f6f483d431aced9a984c7db1ae5cef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155116"
---
# <a name="system-tables-group"></a><span data-ttu-id="ebe7b-103">Grupo tablas del sistema</span><span class="sxs-lookup"><span data-stu-id="ebe7b-103">System Tables Group</span></span>

<span data-ttu-id="ebe7b-104">Las tablas del grupo tablas del sistema realizan un seguimiento de las tablas y columnas de la base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="ebe7b-104">The tables of the system tables group track the tables and columns of the installation database.</span></span>

-   <span data-ttu-id="ebe7b-105">La [ \_ tabla tablas](-tables-table.md) realiza un seguimiento de todas las tablas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="ebe7b-105">The [\_Tables table](-tables-table.md) tracks all the tables in the database.</span></span> <span data-ttu-id="ebe7b-106">Esto incluye las tablas que puede haber creado para sus propias acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="ebe7b-106">This includes tables that you may have created for your own custom actions.</span></span> <span data-ttu-id="ebe7b-107">Consulte esta tabla para averiguar si existe una tabla.</span><span class="sxs-lookup"><span data-stu-id="ebe7b-107">Query this table to find out if a table exists.</span></span>
-   <span data-ttu-id="ebe7b-108">La [ \_ tabla de columnas](-columns-table.md) realiza un seguimiento de las columnas de la base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="ebe7b-108">The [\_Columns table](-columns-table.md) tracks columns in the installation database.</span></span> <span data-ttu-id="ebe7b-109">Actualmente no se realiza el seguimiento de las columnas temporales en esta tabla.</span><span class="sxs-lookup"><span data-stu-id="ebe7b-109">Temporary columns are currently not tracked by this table.</span></span> <span data-ttu-id="ebe7b-110">Consulte esta tabla para averiguar si existe una columna determinada.</span><span class="sxs-lookup"><span data-stu-id="ebe7b-110">Query this table to find out if a given column exists.</span></span>
-   <span data-ttu-id="ebe7b-111">En la [ \_ tabla streams](-streams-table.md) se enumeran los flujos de datos OLE incrustados.</span><span class="sxs-lookup"><span data-stu-id="ebe7b-111">The [\_Streams table](-streams-table.md) lists embedded OLE data streams.</span></span>
-   <span data-ttu-id="ebe7b-112">La [ \_ tabla Storages](-storages-table.md) enumera los almacenamientos de datos OLE incrustados.</span><span class="sxs-lookup"><span data-stu-id="ebe7b-112">The [\_Storages table](-storages-table.md) lists embedded OLE data storages.</span></span>
-   <span data-ttu-id="ebe7b-113">[ \_ Tabla de validación](-validation-table.md).</span><span class="sxs-lookup"><span data-stu-id="ebe7b-113">The [\_Validation table](-validation-table.md).</span></span> <span data-ttu-id="ebe7b-114">La \_ tabla de validación realiza un seguimiento de los tipos y los intervalos permitidos de cada columna de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="ebe7b-114">The \_Validation table tracks the types and allowed ranges of every column in the database.</span></span> <span data-ttu-id="ebe7b-115">La \_ tabla de validación se utiliza durante el proceso de validación de la base de datos para asegurarse de que todas las columnas se han contabilizado y tienen los valores correctos.</span><span class="sxs-lookup"><span data-stu-id="ebe7b-115">The \_Validation table is used during the database validation process to ensure that all columns are accounted for and have the correct values.</span></span> <span data-ttu-id="ebe7b-116">Esta tabla no se incluye con la base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="ebe7b-116">This table is not shipped with the installer database.</span></span>

 

 



