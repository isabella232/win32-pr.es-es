---
description: ICE66 usa las tablas de la base de datos para determinar qué esquema debe usar la base de datos.
ms.assetid: 7cf929a0-2c4c-40ca-a902-dfd9dcd203b8
title: ICE66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea1436ad791941c96c0484a02f40a60fc9939e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810910"
---
# <a name="ice66"></a><span data-ttu-id="8ea82-103">ICE66</span><span class="sxs-lookup"><span data-stu-id="8ea82-103">ICE66</span></span>

<span data-ttu-id="8ea82-104">ICE66 usa las tablas de la base de datos para determinar qué esquema debe usar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="8ea82-104">ICE66 uses the tables in the database to determine which schema your database should use.</span></span>

<span data-ttu-id="8ea82-105">Es posible que algunas funciones solo estén disponibles si el paquete está instalado en un sistema con una versión de Windows Installer actual.</span><span class="sxs-lookup"><span data-stu-id="8ea82-105">Some functionality may only be available if the package is installed on a system with a current Windows Installer version.</span></span>

## <a name="result"></a><span data-ttu-id="8ea82-106">Resultado</span><span class="sxs-lookup"><span data-stu-id="8ea82-106">Result</span></span>

<span data-ttu-id="8ea82-107">ICE66 publica una advertencia si la base de datos usa un esquema incorrecto.</span><span class="sxs-lookup"><span data-stu-id="8ea82-107">ICE66 posts a warning if your database is using the wrong schema.</span></span>

## <a name="example"></a><span data-ttu-id="8ea82-108">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8ea82-108">Example</span></span>

<span data-ttu-id="8ea82-109">ICE66 notifica la siguiente advertencia para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="8ea82-109">ICE66 reports the following warning for the example shown.</span></span>

``` syntax
WARNING: Complete functionality of the IsolatedComponents table is only available with Windows Installer versions 1.1 or greater. Your schema is 100.
```

<span data-ttu-id="8ea82-110">Esta advertencia se puede omitir si desea que el paquete se instale con una versión de Windows Installer actual.</span><span class="sxs-lookup"><span data-stu-id="8ea82-110">This warning can be ignored if you want your package to be installed using a current Windows Installer version.</span></span> <span data-ttu-id="8ea82-111">Por ejemplo, si desea que el paquete se pueda instalar solo en la versión 2,0 o posterior, cambie el esquema del paquete (PID \_ PAGECOUNT) a 200.</span><span class="sxs-lookup"><span data-stu-id="8ea82-111">For example, if you want your package to be installable only on version 2.0 or later, change your package schema (PID\_PAGECOUNT) to 200.</span></span>

[<span data-ttu-id="8ea82-112">Tabla IsolatedComponent</span><span class="sxs-lookup"><span data-stu-id="8ea82-112">IsolatedComponent Table</span></span>](isolatedcomponent-table.md)



| <span data-ttu-id="8ea82-113">Componente \_ compartido</span><span class="sxs-lookup"><span data-stu-id="8ea82-113">Component\_Shared</span></span> | <span data-ttu-id="8ea82-114">Aplicación de componentes \_</span><span class="sxs-lookup"><span data-stu-id="8ea82-114">Component\_Application</span></span> |
|-------------------|------------------------|
| <span data-ttu-id="8ea82-115">Component1</span><span class="sxs-lookup"><span data-stu-id="8ea82-115">Component1</span></span>        | <span data-ttu-id="8ea82-116">Component2</span><span class="sxs-lookup"><span data-stu-id="8ea82-116">Component2</span></span>             |



 

[<span data-ttu-id="8ea82-117">Flujo de información de Resumen</span><span class="sxs-lookup"><span data-stu-id="8ea82-117">Summary Information Stream</span></span>](summary-information-stream.md)



| <span data-ttu-id="8ea82-118">PIDt</span><span class="sxs-lookup"><span data-stu-id="8ea82-118">PIDt</span></span>           | <span data-ttu-id="8ea82-119">Value</span><span class="sxs-lookup"><span data-stu-id="8ea82-119">Value</span></span> |
|----------------|-------|
| <span data-ttu-id="8ea82-120">PID \_ PAGECOUNT</span><span class="sxs-lookup"><span data-stu-id="8ea82-120">PID\_PAGECOUNT</span></span> | <span data-ttu-id="8ea82-121">100</span><span class="sxs-lookup"><span data-stu-id="8ea82-121">100</span></span>   |



 

## <a name="table-used-during-execution"></a><span data-ttu-id="8ea82-122">Tabla utilizada durante la ejecución:</span><span class="sxs-lookup"><span data-stu-id="8ea82-122">Table used during execution:</span></span>

[<span data-ttu-id="8ea82-123">\_Tabla de columnas</span><span class="sxs-lookup"><span data-stu-id="8ea82-123">\_Columns table</span></span>](-columns-table.md)

## <a name="related-topics"></a><span data-ttu-id="8ea82-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8ea82-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ea82-125">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="8ea82-125">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



