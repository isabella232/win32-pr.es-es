---
description: ICE06 comprueba cada tabla para comprobar que todas las columnas enumeradas en la \_ tabla de validación están presentes en la tabla. Si no existe una tabla, \_ se omiten las entradas de validación de esa tabla.
ms.assetid: 0c3f21ae-49ea-4cfe-b465-6fdc2b19cbb9
title: ICE06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9442d9b2c4089b88299106de875074bd7b0625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002258"
---
# <a name="ice06"></a><span data-ttu-id="0d7d5-104">ICE06</span><span class="sxs-lookup"><span data-stu-id="0d7d5-104">ICE06</span></span>

<span data-ttu-id="0d7d5-105">ICE06 comprueba cada tabla para comprobar que todas las columnas enumeradas en la [ \_ tabla de validación](-validation-table.md) están presentes en la tabla.</span><span class="sxs-lookup"><span data-stu-id="0d7d5-105">ICE06 checks every table to validate that all the columns listed in the [\_Validation table](-validation-table.md) are present in the table.</span></span> <span data-ttu-id="0d7d5-106">Si no existe una tabla, \_ se omiten las entradas de validación de esa tabla.</span><span class="sxs-lookup"><span data-stu-id="0d7d5-106">If a table does not exist, any \_Validation entries for that table are ignored.</span></span>

<span data-ttu-id="0d7d5-107">El propósito de ICE06 es detectar las instancias en las que un autor intenta usar una nueva \_ tabla de validación que refleja un cambio de esquema con una base de datos antigua que no se ha actualizado.</span><span class="sxs-lookup"><span data-stu-id="0d7d5-107">The purpose of ICE06 is to detect instances in which an author tries to use a new \_Validation table that reflects a schema change with an old database that has not been updated.</span></span> <span data-ttu-id="0d7d5-108">ICE06 también detecta el caso inverso de una \_ tabla de validación anterior que se utiliza con una base de datos modificada.</span><span class="sxs-lookup"><span data-stu-id="0d7d5-108">ICE06 also detects the reverse case of an old \_Validation table being used with an altered database.</span></span>

<span data-ttu-id="0d7d5-109">Tenga en cuenta que la validación interna realizada por [ICE03](ice03.md) detecta la instancia de una columna de tabla no definida en la \_ tabla de validación que aparece en el catálogo de columnas.</span><span class="sxs-lookup"><span data-stu-id="0d7d5-109">Note that the internal validation performed by [ICE03](ice03.md) catches the instance of a table column not defined in the \_Validation table being listed in the columns catalog.</span></span> <span data-ttu-id="0d7d5-110">Por lo tanto, el uso de ICE03 y ICE06 garantiza que se prueban todas las columnas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="0d7d5-110">The use of both ICE03 and ICE06 therefore ensures every column in the database is tested.</span></span>

## <a name="result"></a><span data-ttu-id="0d7d5-111">Resultado</span><span class="sxs-lookup"><span data-stu-id="0d7d5-111">Result</span></span>

<span data-ttu-id="0d7d5-112">ICE06 expone un error cuando hay una columna de tabla definida en la \_ tabla de validación que no aparece en la \_ tabla de columnas.</span><span class="sxs-lookup"><span data-stu-id="0d7d5-112">ICE06 posts an error when there is a table column defined in the \_Validation table that is not listed in the \_Columns table.</span></span>

## <a name="example"></a><span data-ttu-id="0d7d5-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0d7d5-113">Example</span></span>

<span data-ttu-id="0d7d5-114">En el ejemplo siguiente, ICE06 envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="0d7d5-114">For the following example ICE06 posts the message</span></span>

<span data-ttu-id="0d7d5-115">Columna: versión de la tabla: ModuleSignature no está definido en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="0d7d5-115">Column: Version of Table: ModuleSignature is not defined in database.</span></span>

<span data-ttu-id="0d7d5-116">[ \_ Tabla de validación](-validation-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="0d7d5-116">[\_Validation Table](-validation-table.md) (partial)</span></span>



| <span data-ttu-id="0d7d5-117">Tabla</span><span class="sxs-lookup"><span data-stu-id="0d7d5-117">Table</span></span>           | <span data-ttu-id="0d7d5-118">Columna</span><span class="sxs-lookup"><span data-stu-id="0d7d5-118">Column</span></span>   |
|-----------------|----------|
| <span data-ttu-id="0d7d5-119">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="0d7d5-119">ModuleSignature</span></span> | <span data-ttu-id="0d7d5-120">ModuleID</span><span class="sxs-lookup"><span data-stu-id="0d7d5-120">ModuleID</span></span> |
| <span data-ttu-id="0d7d5-121">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="0d7d5-121">ModuleSignature</span></span> | <span data-ttu-id="0d7d5-122">Versión</span><span class="sxs-lookup"><span data-stu-id="0d7d5-122">Version</span></span>  |



 

<span data-ttu-id="0d7d5-123">[ \_ Tabla de columnas](-columns-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="0d7d5-123">[\_Columns Table](-columns-table.md) (partial)</span></span>



| <span data-ttu-id="0d7d5-124">Tabla</span><span class="sxs-lookup"><span data-stu-id="0d7d5-124">Table</span></span>           | <span data-ttu-id="0d7d5-125">número</span><span class="sxs-lookup"><span data-stu-id="0d7d5-125">Number</span></span> | <span data-ttu-id="0d7d5-126">NOMBRE</span><span class="sxs-lookup"><span data-stu-id="0d7d5-126">Name</span></span>     |
|-----------------|--------|----------|
| <span data-ttu-id="0d7d5-127">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="0d7d5-127">ModuleSignature</span></span> | <span data-ttu-id="0d7d5-128">1</span><span class="sxs-lookup"><span data-stu-id="0d7d5-128">1</span></span>      | <span data-ttu-id="0d7d5-129">ModuleID</span><span class="sxs-lookup"><span data-stu-id="0d7d5-129">ModuleID</span></span> |



 

<span data-ttu-id="0d7d5-130">La columna version de la tabla ModuleSignature no está en la base de datos ni se muestra en la \_ tabla columnas.</span><span class="sxs-lookup"><span data-stu-id="0d7d5-130">The Version column of the ModuleSignature table is not in the database or listed in the \_Columns table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d7d5-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0d7d5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d7d5-132">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="0d7d5-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



