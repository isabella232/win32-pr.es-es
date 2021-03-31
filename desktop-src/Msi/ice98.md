---
description: ICE98 comprueba el campo de descripción de la tabla ODBCDataSource para un origen de datos ODBC. Usa la función SQLValidDSN para comprobar que solo se usan caracteres válidos y que la descripción no supera la longitud máxima permitida.
ms.assetid: ed78db96-10a1-4e42-9147-2309c9ca9c6e
title: ICE98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf06e97341bd8f15502b1ea1fe43a975dc9cde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277374"
---
# <a name="ice98"></a><span data-ttu-id="fe4f7-104">ICE98</span><span class="sxs-lookup"><span data-stu-id="fe4f7-104">ICE98</span></span>

<span data-ttu-id="fe4f7-105">ICE98 comprueba el campo de descripción de la [tabla ODBCDataSource](odbcdatasource-table.md) para un origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="fe4f7-105">ICE98 verifies the description field of the [ODBCDataSource Table](odbcdatasource-table.md) for an ODBC data source.</span></span> <span data-ttu-id="fe4f7-106">Usa la función **SQLValidDSN** para comprobar que solo se usan caracteres válidos y que la descripción no supera la longitud máxima permitida.</span><span class="sxs-lookup"><span data-stu-id="fe4f7-106">It uses the **SQLValidDSN** function to check that only valid characters are used, and that the description does not exceed the maximum allowed length.</span></span>

## <a name="result"></a><span data-ttu-id="fe4f7-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="fe4f7-107">Result</span></span>

<span data-ttu-id="fe4f7-108">ICE98 expone las siguientes advertencias.</span><span class="sxs-lookup"><span data-stu-id="fe4f7-108">ICE98 posts the following warnings.</span></span>



| <span data-ttu-id="fe4f7-109">ADVERTENCIA de ICE98</span><span class="sxs-lookup"><span data-stu-id="fe4f7-109">ICE98 warning</span></span>                    | <span data-ttu-id="fe4f7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe4f7-110">Description</span></span>                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe4f7-111">El nombre del origen de datos no es válido.</span><span class="sxs-lookup"><span data-stu-id="fe4f7-111">The data source name is invalid.</span></span> | <span data-ttu-id="fe4f7-112">El valor de la columna Descripción de la [tabla ODBCDataSource](odbcdatasource-table.md) contiene caracteres no válidos o es demasiado largo, lo que significa que supera la \_ \_ \_ longitud de DSN de SQL Max de 32.</span><span class="sxs-lookup"><span data-stu-id="fe4f7-112">The value in the Description column of the [ODBCDataSource Table](odbcdatasource-table.md) either contains invalid characters or is too long, which means that it exceeds the SQL\_MAX\_DSN\_LENGTH of 32.</span></span> |



 

## <a name="example"></a><span data-ttu-id="fe4f7-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fe4f7-113">Example</span></span>

<span data-ttu-id="fe4f7-114">ICE98 notifica las siguientes advertencias para el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="fe4f7-114">ICE98 reports the following warnings for the example:</span></span>

``` syntax
The data source name is invalid: !
The data source name is invalid: <String of length > 32>
```

<span data-ttu-id="fe4f7-115">[Tabla ODBCDataSource](odbcdatasource-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="fe4f7-115">[ODBCDataSource Table](odbcdatasource-table.md) (partial)</span></span>



| <span data-ttu-id="fe4f7-116">DataSource</span><span class="sxs-lookup"><span data-stu-id="fe4f7-116">DataSource</span></span> | <span data-ttu-id="fe4f7-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe4f7-117">Description</span></span>                      |
|------------|----------------------------------|
| <span data-ttu-id="fe4f7-118">BadChar</span><span class="sxs-lookup"><span data-stu-id="fe4f7-118">BadChar</span></span>    | <span data-ttu-id="fe4f7-119">!</span><span class="sxs-lookup"><span data-stu-id="fe4f7-119">!</span></span>                                |
| <span data-ttu-id="fe4f7-120">TooLong</span><span class="sxs-lookup"><span data-stu-id="fe4f7-120">TooLong</span></span>    | <span data-ttu-id="fe4f7-121"><String of length > 32></span><span class="sxs-lookup"><span data-stu-id="fe4f7-121"><String of length > 32></span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fe4f7-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fe4f7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe4f7-123">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="fe4f7-123">ICE Reference</span></span>](ice-reference.md)
</dt> <dt>

[<span data-ttu-id="fe4f7-124">Tabla ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="fe4f7-124">ODBCDataSource Table</span></span>](odbcdatasource-table.md)
</dt> </dl>

 

 



