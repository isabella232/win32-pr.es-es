---
description: La tabla MsiFileHash se usa para almacenar un hash de 128 bits de un archivo de código fuente proporcionado por el paquete Windows Installer. El hash se divide en valores de 4 32 bits y se almacena en columnas independientes de la tabla.
ms.assetid: 972a2784-418d-4cb3-b13c-df89b079e94c
title: Tabla MsiFileHash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86acb299e5d7f099a8d49affc64810d128e88369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666465"
---
# <a name="msifilehash-table"></a><span data-ttu-id="a9b70-104">Tabla MsiFileHash</span><span class="sxs-lookup"><span data-stu-id="a9b70-104">MsiFileHash Table</span></span>

<span data-ttu-id="a9b70-105">La tabla **MsiFileHash** se usa para almacenar un hash de 128 bits de un archivo de código fuente proporcionado por el paquete Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a9b70-105">The **MsiFileHash** table is used to store a 128-bit hash of a source file provided by the Windows Installer package.</span></span> <span data-ttu-id="a9b70-106">El hash se divide en valores de 4 32 bits y se almacena en columnas independientes de la tabla.</span><span class="sxs-lookup"><span data-stu-id="a9b70-106">The hash is split into four 32-bit values and stored in separate columns of the table.</span></span>

<span data-ttu-id="a9b70-107">Windows Installer puede utilizar el hash de archivo como medio para detectar y eliminar la copia de archivos innecesaria.</span><span class="sxs-lookup"><span data-stu-id="a9b70-107">Windows Installer can use file hashing as a means to detect and eliminate unnecessary file copying.</span></span> <span data-ttu-id="a9b70-108">Un hash de archivo almacenado en la tabla **MsiFileHash** se puede comparar con un hash de un archivo existente en el equipo del usuario obtenido mediante una llamada a [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span><span class="sxs-lookup"><span data-stu-id="a9b70-108">A file hash stored in the **MsiFileHash** table may be compared to a hash of an existing file on the user's computer obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span></span> <span data-ttu-id="a9b70-109">La tabla **MsiFileHash** solo se puede usar con archivos sin versión.</span><span class="sxs-lookup"><span data-stu-id="a9b70-109">The **MsiFileHash** table can only be used with unversioned files.</span></span>

<span data-ttu-id="a9b70-110">La tabla **MsiFileHash** tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="a9b70-110">The **MsiFileHash** table has the following columns.</span></span>



| <span data-ttu-id="a9b70-111">Columna</span><span class="sxs-lookup"><span data-stu-id="a9b70-111">Column</span></span>    | <span data-ttu-id="a9b70-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="a9b70-112">Type</span></span>                               | <span data-ttu-id="a9b70-113">Clave</span><span class="sxs-lookup"><span data-stu-id="a9b70-113">Key</span></span> | <span data-ttu-id="a9b70-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="a9b70-114">Nullable</span></span> |
|-----------|------------------------------------|-----|----------|
| <span data-ttu-id="a9b70-115">Archivo\_</span><span class="sxs-lookup"><span data-stu-id="a9b70-115">File\_</span></span>    | [<span data-ttu-id="a9b70-116">Identificador</span><span class="sxs-lookup"><span data-stu-id="a9b70-116">Identifier</span></span>](identifier.md)       | <span data-ttu-id="a9b70-117">Y</span><span class="sxs-lookup"><span data-stu-id="a9b70-117">Y</span></span>   | <span data-ttu-id="a9b70-118">N</span><span class="sxs-lookup"><span data-stu-id="a9b70-118">N</span></span>        |
| <span data-ttu-id="a9b70-119">Opciones</span><span class="sxs-lookup"><span data-stu-id="a9b70-119">Options</span></span>   | [<span data-ttu-id="a9b70-120">Entero</span><span class="sxs-lookup"><span data-stu-id="a9b70-120">Integer</span></span>](integer.md)             | <span data-ttu-id="a9b70-121">N</span><span class="sxs-lookup"><span data-stu-id="a9b70-121">N</span></span>   | <span data-ttu-id="a9b70-122">N</span><span class="sxs-lookup"><span data-stu-id="a9b70-122">N</span></span>        |
| <span data-ttu-id="a9b70-123">HashPart1</span><span class="sxs-lookup"><span data-stu-id="a9b70-123">HashPart1</span></span> | [<span data-ttu-id="a9b70-124">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="a9b70-124">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="a9b70-125">N</span><span class="sxs-lookup"><span data-stu-id="a9b70-125">N</span></span>   | <span data-ttu-id="a9b70-126">N</span><span class="sxs-lookup"><span data-stu-id="a9b70-126">N</span></span>        |
| <span data-ttu-id="a9b70-127">HashPart2</span><span class="sxs-lookup"><span data-stu-id="a9b70-127">HashPart2</span></span> | [<span data-ttu-id="a9b70-128">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="a9b70-128">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="a9b70-129">N</span><span class="sxs-lookup"><span data-stu-id="a9b70-129">N</span></span>   | <span data-ttu-id="a9b70-130">N</span><span class="sxs-lookup"><span data-stu-id="a9b70-130">N</span></span>        |
| <span data-ttu-id="a9b70-131">HashPart3</span><span class="sxs-lookup"><span data-stu-id="a9b70-131">HashPart3</span></span> | [<span data-ttu-id="a9b70-132">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="a9b70-132">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="a9b70-133">N</span><span class="sxs-lookup"><span data-stu-id="a9b70-133">N</span></span>   | <span data-ttu-id="a9b70-134">N</span><span class="sxs-lookup"><span data-stu-id="a9b70-134">N</span></span>        |
| <span data-ttu-id="a9b70-135">Hashpart4</span><span class="sxs-lookup"><span data-stu-id="a9b70-135">Hashpart4</span></span> | [<span data-ttu-id="a9b70-136">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="a9b70-136">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="a9b70-137">N</span><span class="sxs-lookup"><span data-stu-id="a9b70-137">N</span></span>   | <span data-ttu-id="a9b70-138">N</span><span class="sxs-lookup"><span data-stu-id="a9b70-138">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a9b70-139">Columnas</span><span class="sxs-lookup"><span data-stu-id="a9b70-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a9b70-140"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_</span><span class="sxs-lookup"><span data-stu-id="a9b70-140"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="a9b70-141">Clave externa para la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="a9b70-141">Foreign key to [File table](file-table.md).</span></span> <span data-ttu-id="a9b70-142">72 cadena de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a9b70-142">72 char string.</span></span>

</dd> <dt>

<span data-ttu-id="a9b70-143"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Opciones</span><span class="sxs-lookup"><span data-stu-id="a9b70-143"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Options</span></span>
</dt> <dd>

<span data-ttu-id="a9b70-144">Esta columna debe ser 0 y está reservada para un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="a9b70-144">This column must be 0 and is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="a9b70-145"><span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1</span><span class="sxs-lookup"><span data-stu-id="a9b70-145"><span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1</span></span>
</dt> <dd>

<span data-ttu-id="a9b70-146">Primeros 32 bits de hash.</span><span class="sxs-lookup"><span data-stu-id="a9b70-146">First 32 bits of hash.</span></span> <span data-ttu-id="a9b70-147">El hash de archivo especificado en este campo se debe obtener llamando a [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) o al [**método FileHash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="a9b70-147">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="a9b70-148">No utilice otros métodos.</span><span class="sxs-lookup"><span data-stu-id="a9b70-148">Do not use other methods.</span></span>

</dd> <dt>

<span data-ttu-id="a9b70-149"><span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2</span><span class="sxs-lookup"><span data-stu-id="a9b70-149"><span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2</span></span>
</dt> <dd>

<span data-ttu-id="a9b70-150">Segundos 32 bits de hash.</span><span class="sxs-lookup"><span data-stu-id="a9b70-150">Second 32 bits of hash.</span></span> <span data-ttu-id="a9b70-151">El hash de archivo especificado en este campo se debe obtener llamando a [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) o al [**método FileHash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="a9b70-151">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="a9b70-152">No utilice otros métodos hash.</span><span class="sxs-lookup"><span data-stu-id="a9b70-152">Do not use other hashing methods.</span></span>

</dd> <dt>

<span data-ttu-id="a9b70-153"><span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3</span><span class="sxs-lookup"><span data-stu-id="a9b70-153"><span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3</span></span>
</dt> <dd>

<span data-ttu-id="a9b70-154">Tercer 32 bits de hash.</span><span class="sxs-lookup"><span data-stu-id="a9b70-154">Third 32 bits of hash.</span></span> <span data-ttu-id="a9b70-155">El hash de archivo especificado en este campo se debe obtener llamando a [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) o al [**método FileHash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="a9b70-155">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="a9b70-156">No utilice otros métodos.</span><span class="sxs-lookup"><span data-stu-id="a9b70-156">Do not use other methods.</span></span>

</dd> <dt>

<span data-ttu-id="a9b70-157"><span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4</span><span class="sxs-lookup"><span data-stu-id="a9b70-157"><span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4</span></span>
</dt> <dd>

<span data-ttu-id="a9b70-158">Cuarto 32 bits de hash.</span><span class="sxs-lookup"><span data-stu-id="a9b70-158">Fourth 32 bits of hash.</span></span> <span data-ttu-id="a9b70-159">El hash de archivo especificado en este campo se debe obtener llamando a [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) o al [**método FileHash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="a9b70-159">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="a9b70-160">No utilice otros métodos.</span><span class="sxs-lookup"><span data-stu-id="a9b70-160">Do not use other methods.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="a9b70-161">Validación</span><span class="sxs-lookup"><span data-stu-id="a9b70-161">Validation</span></span>

<dl>

[<span data-ttu-id="a9b70-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="a9b70-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a9b70-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="a9b70-163">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="a9b70-164">ICE32</span><span class="sxs-lookup"><span data-stu-id="a9b70-164">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="a9b70-165">ICE60</span><span class="sxs-lookup"><span data-stu-id="a9b70-165">ICE60</span></span>](ice60.md)  
[<span data-ttu-id="a9b70-166">ICE66</span><span class="sxs-lookup"><span data-stu-id="a9b70-166">ICE66</span></span>](ice66.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="a9b70-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a9b70-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9b70-168">**MsiGetFileHash**</span><span class="sxs-lookup"><span data-stu-id="a9b70-168">**MsiGetFileHash**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> <dt>

[<span data-ttu-id="a9b70-169">Control de versiones de archivo predeterminado</span><span class="sxs-lookup"><span data-stu-id="a9b70-169">Default File Versioning</span></span>](default-file-versioning.md)
</dt> </dl>

 

 



