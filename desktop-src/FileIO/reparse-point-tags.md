---
description: Cada punto de reanálisis tiene una etiqueta de identificador para que pueda diferenciar de forma eficaz entre los distintos tipos de puntos de reanálisis, sin tener que examinar los datos definidos por el usuario en el punto de análisis.
ms.assetid: d02a2f50-d374-4149-bc04-49b7db052f62
title: Etiquetas de punto de reanálisis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a53b65034347e2a2c07afcd6c1f03e31f73cef7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668141"
---
# <a name="reparse-point-tags"></a><span data-ttu-id="25f51-103">Etiquetas de punto de reanálisis</span><span class="sxs-lookup"><span data-stu-id="25f51-103">Reparse Point Tags</span></span>

<span data-ttu-id="25f51-104">Cada punto de reanálisis tiene una etiqueta de identificador para que pueda diferenciar de forma eficaz entre los distintos tipos de puntos de reanálisis, sin tener que examinar los datos definidos por el usuario en el punto de análisis.</span><span class="sxs-lookup"><span data-stu-id="25f51-104">Each reparse point has an identifier tag so that you can efficiently differentiate between the different types of reparse points, without having to examine the user-defined data in the reparse point.</span></span> <span data-ttu-id="25f51-105">El sistema utiliza un conjunto de etiquetas predefinidas y un intervalo de etiquetas reservadas para Microsoft.</span><span class="sxs-lookup"><span data-stu-id="25f51-105">The system uses a set of predefined tags and a range of tags reserved for Microsoft.</span></span> <span data-ttu-id="25f51-106">Si usa cualquiera de las etiquetas reservadas al establecer un punto de reanálisis, se produce un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="25f51-106">If you use any of the reserved tags when setting a reparse point, the operation fails.</span></span> <span data-ttu-id="25f51-107">Las etiquetas no incluidas en estos intervalos no están reservadas y están disponibles para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="25f51-107">Tags not included in these ranges are not reserved and are available for your application.</span></span>

<span data-ttu-id="25f51-108">Al establecer un punto de análisis, debe etiquetar los datos que se van a colocar en el punto de análisis.</span><span class="sxs-lookup"><span data-stu-id="25f51-108">When you set a reparse point, you must tag the data to be placed in the reparse point.</span></span> <span data-ttu-id="25f51-109">Una vez establecido el punto de reanálisis, se produce un error en una nueva operación de establecimiento si la etiqueta de los datos nuevos no coincide con la etiqueta de los datos existentes.</span><span class="sxs-lookup"><span data-stu-id="25f51-109">After the reparse point has been established, a new set operation fails if the tag for the new data does not match the tag for the existing data.</span></span> <span data-ttu-id="25f51-110">Si las etiquetas coinciden, la operación de establecimiento sobrescribe el punto de reanálisis existente.</span><span class="sxs-lookup"><span data-stu-id="25f51-110">If the tags match, the set operation overwrites the existing reparse point.</span></span>

<span data-ttu-id="25f51-111">Para recuperar la etiqueta de punto de reanálisis, utilice la función [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) .</span><span class="sxs-lookup"><span data-stu-id="25f51-111">To retrieve the reparse point tag, use the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) function.</span></span> <span data-ttu-id="25f51-112">Si el miembro **dwFileAttributes** incluye el atributo de **archivo de \_ \_ \_ punto de reanálisis de atributo** , el miembro **dwReserved0** especifica el punto de reanálisis.</span><span class="sxs-lookup"><span data-stu-id="25f51-112">If the **dwFileAttributes** member includes the **FILE\_ATTRIBUTE\_REPARSE\_POINT** attribute, then the **dwReserved0** member specifies the reparse point.</span></span>

## <a name="tag-contents"></a><span data-ttu-id="25f51-113">Contenido de etiqueta</span><span class="sxs-lookup"><span data-stu-id="25f51-113">Tag Contents</span></span>

<span data-ttu-id="25f51-114">Las etiquetas de repetición de análisis se almacenan como valores **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="25f51-114">Reparse tags are stored as **DWORD** values.</span></span> <span data-ttu-id="25f51-115">Los bits definen ciertos atributos, tal y como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="25f51-115">The bits define certain attributes, as shown in the following diagram.</span></span>

``` syntax
   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
  +-+-+-+-+-----------------------+-------------------------------+
  |M|R|N|R|     Reserved bits     |      Reparse tag value        |
  +-+-+-+-+-----------------------+-------------------------------+
```

<span data-ttu-id="25f51-116">Los 16 bits inferiores determinan el tipo de punto de reanálisis.</span><span class="sxs-lookup"><span data-stu-id="25f51-116">The low 16 bits determine the kind of reparse point.</span></span> <span data-ttu-id="25f51-117">Los 16 bits superiores tienen 12 bits reservados para uso futuro y 4 bits que denotan atributos específicos de las etiquetas y los datos representados por el punto de análisis.</span><span class="sxs-lookup"><span data-stu-id="25f51-117">The high 16 bits have 12 bits reserved for future use and 4 bits that denote specific attributes of the tags and the data represented by the reparse point.</span></span> <span data-ttu-id="25f51-118">En la tabla siguiente se describen estos bits.</span><span class="sxs-lookup"><span data-stu-id="25f51-118">The following table describes these bits.</span></span>



| <span data-ttu-id="25f51-119">bit</span><span class="sxs-lookup"><span data-stu-id="25f51-119">Bit</span></span> | <span data-ttu-id="25f51-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="25f51-120">Description</span></span>                                                                                                  |
|-----|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25f51-121">M</span><span class="sxs-lookup"><span data-stu-id="25f51-121">M</span></span>   | <span data-ttu-id="25f51-122">Bit de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="25f51-122">Microsoft bit.</span></span> <span data-ttu-id="25f51-123">Si se establece este bit, la etiqueta es propiedad de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="25f51-123">If this bit is set, the tag is owned by Microsoft.</span></span> <span data-ttu-id="25f51-124">Todas las demás etiquetas deben usar cero para este bit.</span><span class="sxs-lookup"><span data-stu-id="25f51-124">All other tags must use zero for this bit.</span></span> |
| <span data-ttu-id="25f51-125">R</span><span class="sxs-lookup"><span data-stu-id="25f51-125">R</span></span>   | <span data-ttu-id="25f51-126">Sector debe ser cero para todas las etiquetas que no sean de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="25f51-126">Reserved; must be zero for all non-Microsoft tags.</span></span>                                                           |
| <span data-ttu-id="25f51-127">N</span><span class="sxs-lookup"><span data-stu-id="25f51-127">N</span></span>   | <span data-ttu-id="25f51-128">Bit suplente de nombre.</span><span class="sxs-lookup"><span data-stu-id="25f51-128">Name surrogate bit.</span></span> <span data-ttu-id="25f51-129">Si se establece este bit, el archivo o el directorio representa otra entidad con nombre en el sistema.</span><span class="sxs-lookup"><span data-stu-id="25f51-129">If this bit is set, the file or directory represents another named entity in the system.</span></span> |



 

<span data-ttu-id="25f51-130">Las siguientes macros existen para ayudar en las etiquetas de prueba:</span><span class="sxs-lookup"><span data-stu-id="25f51-130">The following macros exist to assist in testing tags:</span></span>

-   [<span data-ttu-id="25f51-131">**IsReparseTagMicrosoft**</span><span class="sxs-lookup"><span data-stu-id="25f51-131">**IsReparseTagMicrosoft**</span></span>](/windows/desktop/api/Winnt/nf-winnt-isreparsetagmicrosoft)
-   [<span data-ttu-id="25f51-132">**IsReparseTagNameSurrogate**</span><span class="sxs-lookup"><span data-stu-id="25f51-132">**IsReparseTagNameSurrogate**</span></span>](/windows/desktop/api/Winnt/nf-winnt-isreparsetagnamesurrogate)

<span data-ttu-id="25f51-133">Cada macro devuelve un valor distinto de cero si se establece el bit asociado.</span><span class="sxs-lookup"><span data-stu-id="25f51-133">Each macro returns a nonzero value if the associated bit is set.</span></span>

<span data-ttu-id="25f51-134">A continuación se indican los valores predefinidos de la etiqueta de reanálisis de Microsoft; se definen en Winnt. h:</span><span class="sxs-lookup"><span data-stu-id="25f51-134">The following are Microsoft's predefined reparse tag values; they are defined in WinNT.h:</span></span>

-   <span data-ttu-id="25f51-135">**IO_REPARSE_TAG_AF_UNIX**</span><span class="sxs-lookup"><span data-stu-id="25f51-135">**IO_REPARSE_TAG_AF_UNIX**</span></span>
-   <span data-ttu-id="25f51-136">**IO_REPARSE_TAG_APPEXECLINK**</span><span class="sxs-lookup"><span data-stu-id="25f51-136">**IO_REPARSE_TAG_APPEXECLINK**</span></span>
-   <span data-ttu-id="25f51-137">**IO_REPARSE_TAG_CLOUD**</span><span class="sxs-lookup"><span data-stu-id="25f51-137">**IO_REPARSE_TAG_CLOUD**</span></span>
-   <span data-ttu-id="25f51-138">**IO_REPARSE_TAG_CLOUD_1**</span><span class="sxs-lookup"><span data-stu-id="25f51-138">**IO_REPARSE_TAG_CLOUD_1**</span></span>
-   <span data-ttu-id="25f51-139">**IO_REPARSE_TAG_CLOUD_2**</span><span class="sxs-lookup"><span data-stu-id="25f51-139">**IO_REPARSE_TAG_CLOUD_2**</span></span>
-   <span data-ttu-id="25f51-140">**IO_REPARSE_TAG_CLOUD_3**</span><span class="sxs-lookup"><span data-stu-id="25f51-140">**IO_REPARSE_TAG_CLOUD_3**</span></span>
-   <span data-ttu-id="25f51-141">**IO_REPARSE_TAG_CLOUD_4**</span><span class="sxs-lookup"><span data-stu-id="25f51-141">**IO_REPARSE_TAG_CLOUD_4**</span></span>
-   <span data-ttu-id="25f51-142">**IO_REPARSE_TAG_CLOUD_5**</span><span class="sxs-lookup"><span data-stu-id="25f51-142">**IO_REPARSE_TAG_CLOUD_5**</span></span>
-   <span data-ttu-id="25f51-143">**IO_REPARSE_TAG_CLOUD_6**</span><span class="sxs-lookup"><span data-stu-id="25f51-143">**IO_REPARSE_TAG_CLOUD_6**</span></span>
-   <span data-ttu-id="25f51-144">**IO_REPARSE_TAG_CLOUD_7**</span><span class="sxs-lookup"><span data-stu-id="25f51-144">**IO_REPARSE_TAG_CLOUD_7**</span></span>
-   <span data-ttu-id="25f51-145">**IO_REPARSE_TAG_CLOUD_8**</span><span class="sxs-lookup"><span data-stu-id="25f51-145">**IO_REPARSE_TAG_CLOUD_8**</span></span>
-   <span data-ttu-id="25f51-146">**IO_REPARSE_TAG_CLOUD_9**</span><span class="sxs-lookup"><span data-stu-id="25f51-146">**IO_REPARSE_TAG_CLOUD_9**</span></span>
-   <span data-ttu-id="25f51-147">**IO_REPARSE_TAG_CLOUD_A**</span><span class="sxs-lookup"><span data-stu-id="25f51-147">**IO_REPARSE_TAG_CLOUD_A**</span></span>
-   <span data-ttu-id="25f51-148">**IO_REPARSE_TAG_CLOUD_B**</span><span class="sxs-lookup"><span data-stu-id="25f51-148">**IO_REPARSE_TAG_CLOUD_B**</span></span>
-   <span data-ttu-id="25f51-149">**IO_REPARSE_TAG_CLOUD_C**</span><span class="sxs-lookup"><span data-stu-id="25f51-149">**IO_REPARSE_TAG_CLOUD_C**</span></span>
-   <span data-ttu-id="25f51-150">**IO_REPARSE_TAG_CLOUD_D**</span><span class="sxs-lookup"><span data-stu-id="25f51-150">**IO_REPARSE_TAG_CLOUD_D**</span></span>
-   <span data-ttu-id="25f51-151">**IO_REPARSE_TAG_CLOUD_E**</span><span class="sxs-lookup"><span data-stu-id="25f51-151">**IO_REPARSE_TAG_CLOUD_E**</span></span>
-   <span data-ttu-id="25f51-152">**IO_REPARSE_TAG_CLOUD_F**</span><span class="sxs-lookup"><span data-stu-id="25f51-152">**IO_REPARSE_TAG_CLOUD_F**</span></span>
-   <span data-ttu-id="25f51-153">**IO_REPARSE_TAG_CLOUD_MASK**</span><span class="sxs-lookup"><span data-stu-id="25f51-153">**IO_REPARSE_TAG_CLOUD_MASK**</span></span>
-   <span data-ttu-id="25f51-154">**IO_REPARSE_TAG_CSV**</span><span class="sxs-lookup"><span data-stu-id="25f51-154">**IO_REPARSE_TAG_CSV**</span></span>
-   <span data-ttu-id="25f51-155">**IO_REPARSE_TAG_DEDUP**</span><span class="sxs-lookup"><span data-stu-id="25f51-155">**IO_REPARSE_TAG_DEDUP**</span></span>
-   <span data-ttu-id="25f51-156">**IO_REPARSE_TAG_DFS**</span><span class="sxs-lookup"><span data-stu-id="25f51-156">**IO_REPARSE_TAG_DFS**</span></span>
-   <span data-ttu-id="25f51-157">**IO_REPARSE_TAG_DFSR**</span><span class="sxs-lookup"><span data-stu-id="25f51-157">**IO_REPARSE_TAG_DFSR**</span></span>
-   <span data-ttu-id="25f51-158">**IO_REPARSE_TAG_FILE_PLACEHOLDER**</span><span class="sxs-lookup"><span data-stu-id="25f51-158">**IO_REPARSE_TAG_FILE_PLACEHOLDER**</span></span>
-   <span data-ttu-id="25f51-159">**IO_REPARSE_TAG_GLOBAL_REPARSE**</span><span class="sxs-lookup"><span data-stu-id="25f51-159">**IO_REPARSE_TAG_GLOBAL_REPARSE**</span></span>
-   <span data-ttu-id="25f51-160">**IO_REPARSE_TAG_HSM**</span><span class="sxs-lookup"><span data-stu-id="25f51-160">**IO_REPARSE_TAG_HSM**</span></span>
-   <span data-ttu-id="25f51-161">**IO_REPARSE_TAG_HSM2**</span><span class="sxs-lookup"><span data-stu-id="25f51-161">**IO_REPARSE_TAG_HSM2**</span></span>
-   <span data-ttu-id="25f51-162">**IO_REPARSE_TAG_MOUNT_POINT**</span><span class="sxs-lookup"><span data-stu-id="25f51-162">**IO_REPARSE_TAG_MOUNT_POINT**</span></span>
-   <span data-ttu-id="25f51-163">**IO_REPARSE_TAG_NFS**</span><span class="sxs-lookup"><span data-stu-id="25f51-163">**IO_REPARSE_TAG_NFS**</span></span>
-   <span data-ttu-id="25f51-164">**IO_REPARSE_TAG_ONEDRIVE**</span><span class="sxs-lookup"><span data-stu-id="25f51-164">**IO_REPARSE_TAG_ONEDRIVE**</span></span>
-   <span data-ttu-id="25f51-165">**IO_REPARSE_TAG_PROJFS**</span><span class="sxs-lookup"><span data-stu-id="25f51-165">**IO_REPARSE_TAG_PROJFS**</span></span>
-   <span data-ttu-id="25f51-166">**IO_REPARSE_TAG_PROJFS_TOMBSTONE**</span><span class="sxs-lookup"><span data-stu-id="25f51-166">**IO_REPARSE_TAG_PROJFS_TOMBSTONE**</span></span>
-   <span data-ttu-id="25f51-167">**IO_REPARSE_TAG_SIS**</span><span class="sxs-lookup"><span data-stu-id="25f51-167">**IO_REPARSE_TAG_SIS**</span></span>
-   <span data-ttu-id="25f51-168">**IO_REPARSE_TAG_STORAGE_SYNC**</span><span class="sxs-lookup"><span data-stu-id="25f51-168">**IO_REPARSE_TAG_STORAGE_SYNC**</span></span>
-   <span data-ttu-id="25f51-169">**IO_REPARSE_TAG_SYMLINK**</span><span class="sxs-lookup"><span data-stu-id="25f51-169">**IO_REPARSE_TAG_SYMLINK**</span></span>
-   <span data-ttu-id="25f51-170">**IO_REPARSE_TAG_UNHANDLED**</span><span class="sxs-lookup"><span data-stu-id="25f51-170">**IO_REPARSE_TAG_UNHANDLED**</span></span>
-   <span data-ttu-id="25f51-171">**IO_REPARSE_TAG_WCI**</span><span class="sxs-lookup"><span data-stu-id="25f51-171">**IO_REPARSE_TAG_WCI**</span></span>
-   <span data-ttu-id="25f51-172">**IO_REPARSE_TAG_WCI_1**</span><span class="sxs-lookup"><span data-stu-id="25f51-172">**IO_REPARSE_TAG_WCI_1**</span></span>
-   <span data-ttu-id="25f51-173">**IO_REPARSE_TAG_WCI_LINK**</span><span class="sxs-lookup"><span data-stu-id="25f51-173">**IO_REPARSE_TAG_WCI_LINK**</span></span>
-   <span data-ttu-id="25f51-174">**IO_REPARSE_TAG_WCI_LINK_1**</span><span class="sxs-lookup"><span data-stu-id="25f51-174">**IO_REPARSE_TAG_WCI_LINK_1**</span></span>
-   <span data-ttu-id="25f51-175">**IO_REPARSE_TAG_WCI_TOMBSTONE**</span><span class="sxs-lookup"><span data-stu-id="25f51-175">**IO_REPARSE_TAG_WCI_TOMBSTONE**</span></span>
-   <span data-ttu-id="25f51-176">**IO_REPARSE_TAG_WIM**</span><span class="sxs-lookup"><span data-stu-id="25f51-176">**IO_REPARSE_TAG_WIM**</span></span>
-   <span data-ttu-id="25f51-177">**IO_REPARSE_TAG_WOF**</span><span class="sxs-lookup"><span data-stu-id="25f51-177">**IO_REPARSE_TAG_WOF**</span></span>

<span data-ttu-id="25f51-178">Para garantizar la exclusividad de las etiquetas, Microsoft proporciona un mecanismo para distribuir nuevas etiquetas.</span><span class="sxs-lookup"><span data-stu-id="25f51-178">To ensure uniqueness of tags, Microsoft provides a mechanism to distribute new tags.</span></span> <span data-ttu-id="25f51-179">Para obtener más información, consulte el [Kit del sistema de archivos instalables (IFS)](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).</span><span class="sxs-lookup"><span data-stu-id="25f51-179">For more information, see the [Installable File System (IFS) Kit](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).</span></span>

 

 



