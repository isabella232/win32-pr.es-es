---
description: ICE04 valida que el número de secuencia de todos los archivos de la tabla de archivos sea menor o igual que el número de secuencia más grande de la columna LastSequence de la tabla de medios.
ms.assetid: ecde1389-50ea-479e-bbc1-a36ce3aceccd
title: ICE04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da25a23a26f8a2c49e224ad334791a6081b697b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002259"
---
# <a name="ice04"></a><span data-ttu-id="fa516-103">ICE04</span><span class="sxs-lookup"><span data-stu-id="fa516-103">ICE04</span></span>

<span data-ttu-id="fa516-104">ICE04 valida que el número de secuencia de todos los archivos de la [tabla de archivos](file-table.md) sea menor o igual que el número de secuencia más grande de la columna LastSequence de la tabla de [medios](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="fa516-104">ICE04 validates that the sequence number of every file in the [File table](file-table.md) is less than or equal to the largest sequence number in the LastSequence column of the [Media table](media-table.md).</span></span>

<span data-ttu-id="fa516-105">Cada registro de la tabla de medios representa un disco en el medio de origen que contiene todos los archivos con un número de secuencia menor o igual que el valor de la columna LastSequence y mayor que el valor de LastSequence en el registro del disco anterior.</span><span class="sxs-lookup"><span data-stu-id="fa516-105">Each record in the Media table represents a disk on the source media containing all the files with a sequence number less than or equal to the value in the LastSequence column and greater than the LastSequence value in the record of the preceding disk.</span></span>

## <a name="result"></a><span data-ttu-id="fa516-106">Resultado</span><span class="sxs-lookup"><span data-stu-id="fa516-106">Result</span></span>

<span data-ttu-id="fa516-107">ICE04 envía un mensaje de error si hay un archivo con un número de secuencia mayor que el número de LastSequence mayor de los medios de origen.</span><span class="sxs-lookup"><span data-stu-id="fa516-107">ICE04 posts an error message if there is a file with a sequence number greater than the largest LastSequence number for the source media.</span></span>

## <a name="example"></a><span data-ttu-id="fa516-108">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fa516-108">Example</span></span>

<span data-ttu-id="fa516-109">ICE04 notificaría el siguiente error para el ejemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="fa516-109">ICE04 would report the following error for the example shown:</span></span>

``` syntax
File: MyFile, Sequence: 210 Greater Than Max Allowed by Media Table.
```

<span data-ttu-id="fa516-110">[Tabla de archivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="fa516-110">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="fa516-111">Archivo</span><span class="sxs-lookup"><span data-stu-id="fa516-111">File</span></span>   | <span data-ttu-id="fa516-112">Secuencia</span><span class="sxs-lookup"><span data-stu-id="fa516-112">Sequence</span></span> |
|--------|----------|
| <span data-ttu-id="fa516-113">MyFile</span><span class="sxs-lookup"><span data-stu-id="fa516-113">MyFile</span></span> | <span data-ttu-id="fa516-114">210</span><span class="sxs-lookup"><span data-stu-id="fa516-114">210</span></span>      |



 

<span data-ttu-id="fa516-115">[Tabla de medios](media-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="fa516-115">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="fa516-116">Detectaron</span><span class="sxs-lookup"><span data-stu-id="fa516-116">DiskId</span></span> | <span data-ttu-id="fa516-117">LastSequence</span><span class="sxs-lookup"><span data-stu-id="fa516-117">LastSequence</span></span> |
|--------|--------------|
| <span data-ttu-id="fa516-118">1</span><span class="sxs-lookup"><span data-stu-id="fa516-118">1</span></span>      | <span data-ttu-id="fa516-119">100</span><span class="sxs-lookup"><span data-stu-id="fa516-119">100</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="fa516-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fa516-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa516-121">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="fa516-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



