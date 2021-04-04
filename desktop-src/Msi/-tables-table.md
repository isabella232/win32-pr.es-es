---
description: La \_ tabla tablas es una tabla del sistema de solo lectura que enumera todas las tablas de la base de datos. Consulte esta tabla para averiguar si existe una tabla.
ms.assetid: d064855b-8c10-476e-9570-cc3ab48ae998
title: _Tables tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2dc3ebafd969a07676f64f674f76c3e16ebe059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909162"
---
# <a name="_tables-table"></a><span data-ttu-id="4410c-104">\_Tabla tablas</span><span class="sxs-lookup"><span data-stu-id="4410c-104">\_Tables Table</span></span>

<span data-ttu-id="4410c-105">La \_ tabla tablas es una tabla del sistema de solo lectura que enumera todas las tablas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="4410c-105">The \_Tables table is a read-only system table that lists all the tables in the database.</span></span> <span data-ttu-id="4410c-106">Consulte esta tabla para averiguar si existe una tabla.</span><span class="sxs-lookup"><span data-stu-id="4410c-106">Query this table to find out if a table exists.</span></span>

<span data-ttu-id="4410c-107">La \_ tabla tablas tiene la siguiente columna.</span><span class="sxs-lookup"><span data-stu-id="4410c-107">The \_Tables Table has the following column.</span></span>



| <span data-ttu-id="4410c-108">Columna</span><span class="sxs-lookup"><span data-stu-id="4410c-108">Column</span></span> | <span data-ttu-id="4410c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4410c-109">Type</span></span>             | <span data-ttu-id="4410c-110">Clave</span><span class="sxs-lookup"><span data-stu-id="4410c-110">Key</span></span> | <span data-ttu-id="4410c-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="4410c-111">Nullable</span></span> |
|--------|------------------|-----|----------|
| <span data-ttu-id="4410c-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="4410c-112">Name</span></span>   | [<span data-ttu-id="4410c-113">Texto</span><span class="sxs-lookup"><span data-stu-id="4410c-113">Text</span></span>](text.md) | <span data-ttu-id="4410c-114">Y</span><span class="sxs-lookup"><span data-stu-id="4410c-114">Y</span></span>   | <span data-ttu-id="4410c-115">N</span><span class="sxs-lookup"><span data-stu-id="4410c-115">N</span></span>        |



 

## <a name="column"></a><span data-ttu-id="4410c-116">Columna</span><span class="sxs-lookup"><span data-stu-id="4410c-116">Column</span></span>

<dl> <dt>

<span data-ttu-id="4410c-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span><span class="sxs-lookup"><span data-stu-id="4410c-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="4410c-118">Nombre de una de las tablas.</span><span class="sxs-lookup"><span data-stu-id="4410c-118">Name of one of the tables.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4410c-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4410c-119">Remarks</span></span>

<span data-ttu-id="4410c-120">Dado que la tabla tables \_ es una tabla del sistema que no se puede modificar mediante consultas SQL, no puede obtener las claves principales con la función [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) o la [**propiedad PrimaryKeys**](database-primarykeys.md).</span><span class="sxs-lookup"><span data-stu-id="4410c-120">Because the \_Tables table is a system table that cannot be modified through SQL queries, you cannot obtain the primary keys with the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function or the [**PrimaryKeys property**](database-primarykeys.md).</span></span>

 

 



