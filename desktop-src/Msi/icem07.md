---
description: ICEM07 comprueba que el orden de los archivos de la tabla de secuencia coincide con el orden de los archivos en MergeModule.CABinet.
ms.assetid: 5778e0c5-2f8d-4562-9c93-d6f6890a74e9
title: ICEM07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 696d5c92671c3a8347cb43714d43e646a3e14f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910385"
---
# <a name="icem07"></a><span data-ttu-id="a9563-103">ICEM07</span><span class="sxs-lookup"><span data-stu-id="a9563-103">ICEM07</span></span>

<span data-ttu-id="a9563-104">ICEM07 comprueba que el orden de los archivos de la tabla de secuencia coincide con el orden de los archivos en [MergeModule.CABinet](mergemodule-cabinet.md).</span><span class="sxs-lookup"><span data-stu-id="a9563-104">ICEM07 verifies that the order of files in the sequence table matches the order of files in [MergeModule.CABinet](mergemodule-cabinet.md).</span></span>

<span data-ttu-id="a9563-105">El módulo de combinación ICEs se almacena en un archivo. Cub de módulo de combinación denominado Mergemod. Cub y no en el archivo. Cub que contiene el ICEs usado para la validación del paquete.</span><span class="sxs-lookup"><span data-stu-id="a9563-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="a9563-106">Resultado</span><span class="sxs-lookup"><span data-stu-id="a9563-106">Result</span></span>

<span data-ttu-id="a9563-107">ICEM07 publica un error si el orden de los archivos de la tabla de archivos no coincide con el orden del archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="a9563-107">ICEM07 posts an error if the order of files in the File table does not match the order in the cabinet file.</span></span>

## <a name="example"></a><span data-ttu-id="a9563-108">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a9563-108">Example</span></span>

<span data-ttu-id="a9563-109">IC0M07 publicaría el mensaje de error siguiente para el ejemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="a9563-109">IC0M07 would post the following error message for the example shown.</span></span>

``` syntax
The file 'FileB.GUID1' appears to be out of sequence. It has position 3 
in the CAB, but not when the file table is ordered by sequence number.
```

[<span data-ttu-id="a9563-110">Tabla de archivos</span><span class="sxs-lookup"><span data-stu-id="a9563-110">File Table</span></span>](file-table.md)



| <span data-ttu-id="a9563-111">Archivo</span><span class="sxs-lookup"><span data-stu-id="a9563-111">File</span></span>          | <span data-ttu-id="a9563-112">Secuencia</span><span class="sxs-lookup"><span data-stu-id="a9563-112">Sequence</span></span> |
|---------------|----------|
| <span data-ttu-id="a9563-113">Archivoa. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="a9563-113">FileA.*GUID1*</span></span> | <span data-ttu-id="a9563-114">1</span><span class="sxs-lookup"><span data-stu-id="a9563-114">1</span></span>        |
| <span data-ttu-id="a9563-115">FileB. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="a9563-115">FileB.*GUID1*</span></span> | <span data-ttu-id="a9563-116">8</span><span class="sxs-lookup"><span data-stu-id="a9563-116">8</span></span>        |
| <span data-ttu-id="a9563-117">FileC. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="a9563-117">FileC.*GUID1*</span></span> | <span data-ttu-id="a9563-118">52</span><span class="sxs-lookup"><span data-stu-id="a9563-118">52</span></span>       |



 

<span data-ttu-id="a9563-119">Embedded [MergeModule.CABinet](mergemodule-cabinet.md)</span><span class="sxs-lookup"><span data-stu-id="a9563-119">Embedded [MergeModule.CABinet](mergemodule-cabinet.md)</span></span>



| <span data-ttu-id="a9563-120">Archivo</span><span class="sxs-lookup"><span data-stu-id="a9563-120">File</span></span>          |
|---------------|
| <span data-ttu-id="a9563-121">Archivoa. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="a9563-121">FileA.*GUID1*</span></span> |
| <span data-ttu-id="a9563-122">FileC. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="a9563-122">FileC.*GUID1*</span></span> |
| <span data-ttu-id="a9563-123">Registrado. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="a9563-123">FileD.*GUID1*</span></span> |
| <span data-ttu-id="a9563-124">FileB. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="a9563-124">FileB.*GUID1*</span></span> |



 

<span data-ttu-id="a9563-125">Aunque los números de secuencia de archivos de la tabla de archivos no tienen que ser consecutivos, y los archivos adicionales pueden existir en el archivo. cab, la secuencia relativa de todos los archivos de la tabla de archivos debe coincidir con el orden en [MergeModule.CABinet](mergemodule-cabinet.md).</span><span class="sxs-lookup"><span data-stu-id="a9563-125">Although the file sequence numbers in the file table do not have to be consecutive, and extra files can exist in the cabinet file, the relative sequence of all files in the File table must match the order in [MergeModule.CABinet](mergemodule-cabinet.md).</span></span> <span data-ttu-id="a9563-126">Para corregir este error, cambie el número de secuencia de FileB para que aparezca después de FileC para que coincida con el orden de los archivos en el archivo. CAB o vuelva a generar el archivo. CAB con los archivos en el orden correcto.</span><span class="sxs-lookup"><span data-stu-id="a9563-126">To fix this error, change the sequence number of FileB to come after FileC to match the file order in the CAB, or rebuild the CAB with the files in the correct order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9563-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a9563-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9563-128">Referencia de módulo de combinación ICE</span><span class="sxs-lookup"><span data-stu-id="a9563-128">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



