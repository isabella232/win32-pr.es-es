---
description: La cláusula ORDER IN GROUP se utiliza junto con la instrucción GROUP ON, que devuelve conjuntos de resultados en grupos.
ms.assetid: edfa2037-3360-411d-8a12-cdb9680222f2
title: ORDER IN GROUP (cláusula)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b4a3a39ffeb2704a099389a6668a075fb4a24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360189"
---
# <a name="order-in-group-clause"></a><span data-ttu-id="ad25e-103">ORDER IN GROUP (cláusula)</span><span class="sxs-lookup"><span data-stu-id="ad25e-103">ORDER IN GROUP Clause</span></span>

<span data-ttu-id="ad25e-104">La cláusula ORDER IN GROUP se utiliza junto con la instrucción [Group on](-search-sql-group-on-over.md) , que devuelve conjuntos de resultados en grupos.</span><span class="sxs-lookup"><span data-stu-id="ad25e-104">The ORDER IN GROUP clause is used in conjunction with the [GROUP ON](-search-sql-group-on-over.md) statement, which returns result sets in groups.</span></span> <span data-ttu-id="ad25e-105">La cláusula ORDER IN GROUP permite ordenar cada grupo devuelto de manera diferente.</span><span class="sxs-lookup"><span data-stu-id="ad25e-105">The ORDER IN GROUP clause enables you to sort each returned group in a different way.</span></span> <span data-ttu-id="ad25e-106">Si agrupa en System. Kind, por ejemplo, puede ordenar todos los documentos por System.Document. LastAuthor, todos los archivos de música por System. Music. AlbumArtist y todos los mensajes de correo electrónico por System. Message. FromName.</span><span class="sxs-lookup"><span data-stu-id="ad25e-106">If you group on System.Kind, for example, you can then sort all documents by System.Document.LastAuthor, all music files by System.Music.AlbumArtist, and all emails by System.Message.FromName.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad25e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad25e-107">Syntax</span></span>

<span data-ttu-id="ad25e-108">La siguiente es la sintaxis de la cláusula ORDER en GROUP:</span><span class="sxs-lookup"><span data-stu-id="ad25e-108">The following is the syntax of the ORDER IN GROUP clause:</span></span>


```
GROUP ON <group column and optional ranges>
OVER (SELECT ... FROM SystemIndex
    ORDER 
        IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]]
        [IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]] ]
        [BY <column> [<direction>] [,<column> [<direction>]] ])
```



<span data-ttu-id="ad25e-109">El especificador de nombre de grupo es un intervalo o un valor conocido de la columna Group, tal como se especifica en la instrucción GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="ad25e-109">The group name specifier is a range or known value from the group column, as specified in the GROUP ON statement.</span></span> <span data-ttu-id="ad25e-110">Por ejemplo, los valores conocidos de System. Photo. isospeed incluirían ' ISO-100 ', ' ISO-200 ', etc.</span><span class="sxs-lookup"><span data-stu-id="ad25e-110">For example, known values for System.Photo.ISOSpeed would include 'ISO-100', 'ISO-200', and so on.</span></span> <span data-ttu-id="ad25e-111">Un intervalo para System. Photo. DateTaken incluiría ' 2006-1-1 ' y ' 2007-1-1 ' para una instrucción como GROUP ON System. ItemDate \[ ' 2006-1-1 ', ' 2007-1-1 ' \] .</span><span class="sxs-lookup"><span data-stu-id="ad25e-111">A range for System.Photo.DateTaken would include '2006-1-1' and '2007-1-1' for a statement like GROUP ON System.ItemDate \['2006-1-1', '2007-1-1'\].</span></span>

<span data-ttu-id="ad25e-112">El especificador de columna debe ser una columna válida especificada en el grupo en o en la instrucción SELECT.</span><span class="sxs-lookup"><span data-stu-id="ad25e-112">The column specifier must be a valid column specified in either the GROUP ON or the SELECT statement.</span></span> <span data-ttu-id="ad25e-113">Puede incluir más de una columna, separadas por comas.</span><span class="sxs-lookup"><span data-stu-id="ad25e-113">You can include more than one column, separated by commas.</span></span> <span data-ttu-id="ad25e-114">Por ejemplo, si agrupa en System. Photo. isospeed, puede ordenar todas las fotos de ISO-100, primero por System. Photo. ShutterSpeed y, a continuación, por System. Photo. abertura.</span><span class="sxs-lookup"><span data-stu-id="ad25e-114">For example, if you group on System.Photo.ISOSpeed, you can sort all ISO-100 photos, first by System.Photo.ShutterSpeed, and then by System.Photo.Aperture.</span></span>

<span data-ttu-id="ad25e-115">El especificador de dirección opcional puede ser ASC para ascendente (de menor a mayor) o DESC para descendente (de alto a bajo).</span><span class="sxs-lookup"><span data-stu-id="ad25e-115">The optional direction specifier can be either ASC for ascending (low to high) or DESC for descending (high to low).</span></span> <span data-ttu-id="ad25e-116">Si no se proporciona un especificador de dirección, se utiliza el valor predeterminado, ascendente.</span><span class="sxs-lookup"><span data-stu-id="ad25e-116">If you do not provide a direction specifier, the default, ascending, is used.</span></span> <span data-ttu-id="ad25e-117">Si especifica más de una columna, pero no especifica todas las direcciones, la dirección que especifique en último lugar se aplicará a cada columna sucesiva hasta que cambie explícitamente la dirección.</span><span class="sxs-lookup"><span data-stu-id="ad25e-117">If you specify more than one column, but do not specify all directions, the direction you specify last is applied to each successive column until you explicitly change the direction.</span></span>

<span data-ttu-id="ad25e-118">Los intervalos o valores que no se especifican explícitamente en una cláusula ORDER GROUP IN se ordenan en orden ascendente por los valores de la columna GROUP ON.</span><span class="sxs-lookup"><span data-stu-id="ad25e-118">Ranges or values that are not explicitly specified in an ORDER GROUP IN clause are sorted in ascending order by the values in the GROUP ON column.</span></span>

## <a name="examples"></a><span data-ttu-id="ad25e-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ad25e-119">Examples</span></span>

<span data-ttu-id="ad25e-120">En el ejemplo siguiente se agrupan los resultados por la propiedad System. Kind.</span><span class="sxs-lookup"><span data-stu-id="ad25e-120">The following example groups results by the System.Kind property.</span></span> <span data-ttu-id="ad25e-121">La consulta ordenaría el grupo ' Program ' por el nombre de la aplicación y el grupo ' Music ' por el título del álbum y el número de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="ad25e-121">The query would order the 'program' group by the application name and the 'music' group by album title and track number.</span></span> <span data-ttu-id="ad25e-122">El grupo **null** se ordenará por el nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="ad25e-122">The **NULL** group would be ordered by the item name.</span></span> <span data-ttu-id="ad25e-123">Todos los demás grupos ordenarían por la fecha del elemento.</span><span class="sxs-lookup"><span data-stu-id="ad25e-123">All other groups would by ordered by the item date.</span></span>


```
GROUP ON System.Kind 
OVER (SELECT System.ItemUrl, System.Music.AlbumTitle, System.Music.TrackNumber, System.ItemName, System.ItemDate, System.Kind FROM SystemIndex
    ORDER 
        IN GROUP 'program' BY System.ApplicationName ASC
        IN GROUP 'music' BY System.Music.AlbumTitle ASC, System.Music.TrackNumber ASC
        IN GROUP NULL BY System.ItemName
        BY System.ItemDate DESC)
```



<span data-ttu-id="ad25e-124">En el ejemplo siguiente se agrupan los resultados por la propiedad System. ItemDate y, a continuación, se ordenan cada grupo por dirección URL, tipo o nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="ad25e-124">The following example groups results by the System.ItemDate property, and then sorts each group by item URL, kind, or name.</span></span>


```
GROUP ON System.ItemDate ['2006-1-1', '2007-1-1', '2008-1-1'] 
OVER (SELECT System.ItemUrl, System.ItemName, System.ItemDate System.Kind FROM SystemIndex
    ORDER 
        IN GROUP MINVALUE BY System.ItemUrl ASC
        IN GROUP '2007-1-1' BY System.Kind
        IN GROUP NULL BY System.ItemName)
```



<span data-ttu-id="ad25e-125">Los resultados de la consulta anterior se devolverían en cinco grupos y se ordenarían según se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ad25e-125">The results of the preceding query would be returned in five groups and sorted as described in the following table.</span></span>



| <span data-ttu-id="ad25e-126">Grupo</span><span class="sxs-lookup"><span data-stu-id="ad25e-126">Group</span></span>    | <span data-ttu-id="ad25e-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad25e-127">Description</span></span>                                               | <span data-ttu-id="ad25e-128">Ordenado por</span><span class="sxs-lookup"><span data-stu-id="ad25e-128">Sorted by</span></span>                                    |
|----------|-----------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="ad25e-129">MINVALUE</span><span class="sxs-lookup"><span data-stu-id="ad25e-129">MINVALUE</span></span> | <span data-ttu-id="ad25e-130">Elementos con fechas anteriores a 2006-1-1</span><span class="sxs-lookup"><span data-stu-id="ad25e-130">Items with dates before 2006-1-1</span></span>                          | <span data-ttu-id="ad25e-131">Ordenados por dirección URL del elemento, en orden ascendente</span><span class="sxs-lookup"><span data-stu-id="ad25e-131">Sorted by the item's URL, in ascending order</span></span> |
| <span data-ttu-id="ad25e-132">2006-1-1</span><span class="sxs-lookup"><span data-stu-id="ad25e-132">2006-1-1</span></span> | <span data-ttu-id="ad25e-133">Elementos con fechas de la 2006-1-1, pero anteriores a 2007-1-1</span><span class="sxs-lookup"><span data-stu-id="ad25e-133">Items with dates on or after 2006-1-1 but before 2007-1-1</span></span> | <span data-ttu-id="ad25e-134">Ordenados por fecha de elemento, en orden ascendente</span><span class="sxs-lookup"><span data-stu-id="ad25e-134">Sorted by item date, in ascending order</span></span>      |
| <span data-ttu-id="ad25e-135">2007-1-1</span><span class="sxs-lookup"><span data-stu-id="ad25e-135">2007-1-1</span></span> | <span data-ttu-id="ad25e-136">Elementos con fechas de la 2007-1-1, pero anteriores a 2008-1-1</span><span class="sxs-lookup"><span data-stu-id="ad25e-136">Items with dates on or after 2007-1-1 but before 2008-1-1</span></span> | <span data-ttu-id="ad25e-137">Ordenado por valor de tipo, en orden ascendente</span><span class="sxs-lookup"><span data-stu-id="ad25e-137">Sorted by kind value, in ascending order</span></span>     |
| <span data-ttu-id="ad25e-138">2008-1-1</span><span class="sxs-lookup"><span data-stu-id="ad25e-138">2008-1-1</span></span> | <span data-ttu-id="ad25e-139">Elementos con fechas en o después de 2008-1-1</span><span class="sxs-lookup"><span data-stu-id="ad25e-139">Items with dates on or after 2008-1-1</span></span>                     | <span data-ttu-id="ad25e-140">Ordenados por fecha de elemento, en orden ascendente</span><span class="sxs-lookup"><span data-stu-id="ad25e-140">Sorted by item date, in ascending order</span></span>      |
| <span data-ttu-id="ad25e-141">**NULL**</span><span class="sxs-lookup"><span data-stu-id="ad25e-141">**NULL**</span></span> | <span data-ttu-id="ad25e-142">Elementos sin valor en la columna System. ItemDate</span><span class="sxs-lookup"><span data-stu-id="ad25e-142">Items with no value in the System.ItemDate column</span></span>         | <span data-ttu-id="ad25e-143">Ordenado por nombre de elemento, en orden ascendente</span><span class="sxs-lookup"><span data-stu-id="ad25e-143">Sorted by item name, in ascending order</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="ad25e-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ad25e-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ad25e-145">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ad25e-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ad25e-146">AGRUPAR POR... MÁS de... Privacidad</span><span class="sxs-lookup"><span data-stu-id="ad25e-146">GROUP ON ... OVER... Statement</span></span>](-search-sql-group-on-over.md)
</dt> <dt>

[<span data-ttu-id="ad25e-147">Cláusula ORDER BY</span><span class="sxs-lookup"><span data-stu-id="ad25e-147">ORDER BY Clause</span></span>](-search-sql-orderby.md)
</dt> </dl>

 

 



