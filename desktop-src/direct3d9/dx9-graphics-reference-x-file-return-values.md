---
description: Los métodos que se usan para trabajar con archivos de DirectX. x pueden devolver los siguientes valores además de los valores devueltos de COM estándar. En desuso.
ms.assetid: a91168bc-966a-47b5-ba83-fc480593228d
title: Valores devueltos (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Return
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 7d465b9759d958cba06bf0b950bc67772fbb84a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821199"
---
# <a name="return-values-dxfileh"></a><span data-ttu-id="0d62f-104">Valores devueltos (DXFile. h)</span><span class="sxs-lookup"><span data-stu-id="0d62f-104">Return Values (DXFile.h)</span></span>

<span data-ttu-id="0d62f-105">Los métodos que se usan para trabajar con archivos de DirectX. x pueden devolver los siguientes valores además de los valores devueltos de COM estándar.</span><span class="sxs-lookup"><span data-stu-id="0d62f-105">The methods used to work with DirectX .x files can return the following values in addition to the standard COM return values.</span></span> <span data-ttu-id="0d62f-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="0d62f-106">Deprecated.</span></span>

<dl> <dt>

<span data-ttu-id="0d62f-107"><span id="DXFILE_OK"></span><span id="dxfile_ok"></span>**DXFILE \_ Aceptar**</span><span class="sxs-lookup"><span data-stu-id="0d62f-107"><span id="DXFILE_OK"></span><span id="dxfile_ok"></span>**DXFILE\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-108">El comando se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0d62f-108">Command completed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-109"><span id="DXFILEERR_BADALLOC"></span><span id="dxfileerr_badalloc"></span>**DXFILEERR \_ BADALLOC**</span><span class="sxs-lookup"><span data-stu-id="0d62f-109"><span id="DXFILEERR_BADALLOC"></span><span id="dxfileerr_badalloc"></span>**DXFILEERR\_BADALLOC**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-110">Se produjo un error de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="0d62f-110">Memory allocation failed.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-111"><span id="DXFILEERR_BADARRAYSIZE"></span><span id="dxfileerr_badarraysize"></span>**DXFILEERR \_ BADARRAYSIZE**</span><span class="sxs-lookup"><span data-stu-id="0d62f-111"><span id="DXFILEERR_BADARRAYSIZE"></span><span id="dxfileerr_badarraysize"></span>**DXFILEERR\_BADARRAYSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-112">El tamaño de la matriz no es válido.</span><span class="sxs-lookup"><span data-stu-id="0d62f-112">Array size is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-113"><span id="DXFILEERR_BADCACHEFILE"></span><span id="dxfileerr_badcachefile"></span>**DXFILEERR \_ BADCACHEFILE**</span><span class="sxs-lookup"><span data-stu-id="0d62f-113"><span id="DXFILEERR_BADCACHEFILE"></span><span id="dxfileerr_badcachefile"></span>**DXFILEERR\_BADCACHEFILE**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-114">El archivo de caché que contiene la fecha del archivo. x no es válido.</span><span class="sxs-lookup"><span data-stu-id="0d62f-114">The cache file containing the .x file date is invalid.</span></span> <span data-ttu-id="0d62f-115">Un archivo caché contiene datos recuperados de la red, almacenados en memoria caché en el disco duro y recuperados en solicitudes posteriores.</span><span class="sxs-lookup"><span data-stu-id="0d62f-115">A cache file contains data retrieved from the network, cached on the hard disk, and retrieved in subsequent requests.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-116"><span id="DXFILEERR_BADDataReference"></span><span id="dxfileerr_baddatareference"></span><span id="DXFILEERR_BADDATAREFERENCE"></span>**DXFILEERR \_ BADDataReference**</span><span class="sxs-lookup"><span data-stu-id="0d62f-116"><span id="DXFILEERR_BADDataReference"></span><span id="dxfileerr_baddatareference"></span><span id="DXFILEERR_BADDATAREFERENCE"></span>**DXFILEERR\_BADDataReference**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-117">La referencia de datos no es válida.</span><span class="sxs-lookup"><span data-stu-id="0d62f-117">Data reference is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-118"><span id="DXFILEERR_BADFILE"></span><span id="dxfileerr_badfile"></span>**DXFILEERR \_ BADFILE**</span><span class="sxs-lookup"><span data-stu-id="0d62f-118"><span id="DXFILEERR_BADFILE"></span><span id="dxfileerr_badfile"></span>**DXFILEERR\_BADFILE**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-119">El archivo no es válido.</span><span class="sxs-lookup"><span data-stu-id="0d62f-119">File is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-120"><span id="DXFILEERR_BADFILECOMPRESSIONTYPE"></span><span id="dxfileerr_badfilecompressiontype"></span>**DXFILEERR \_ BADFILECOMPRESSIONTYPE**</span><span class="sxs-lookup"><span data-stu-id="0d62f-120"><span id="DXFILEERR_BADFILECOMPRESSIONTYPE"></span><span id="dxfileerr_badfilecompressiontype"></span>**DXFILEERR\_BADFILECOMPRESSIONTYPE**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-121">El tipo de compresión de archivo no es válido.</span><span class="sxs-lookup"><span data-stu-id="0d62f-121">File compression type is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-122"><span id="DXFILEERR_BADFILEFLOATSIZE"></span><span id="dxfileerr_badfilefloatsize"></span>**DXFILEERR \_ BADFILEFLOATSIZE**</span><span class="sxs-lookup"><span data-stu-id="0d62f-122"><span id="DXFILEERR_BADFILEFLOATSIZE"></span><span id="dxfileerr_badfilefloatsize"></span>**DXFILEERR\_BADFILEFLOATSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-123">El tamaño de punto flotante no es válido.</span><span class="sxs-lookup"><span data-stu-id="0d62f-123">Floating-point size is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-124"><span id="DXFILEERR_BADFILETYPE"></span><span id="dxfileerr_badfiletype"></span>**DXFILEERR \_ BADFILETYPE**</span><span class="sxs-lookup"><span data-stu-id="0d62f-124"><span id="DXFILEERR_BADFILETYPE"></span><span id="dxfileerr_badfiletype"></span>**DXFILEERR\_BADFILETYPE**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-125">El archivo no es un archivo de DirectX. x.</span><span class="sxs-lookup"><span data-stu-id="0d62f-125">File is not a DirectX .x file.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-126"><span id="DXFILEERR_BADFILEVERSION"></span><span id="dxfileerr_badfileversion"></span>**DXFILEERR \_ BADFILEVERSION**</span><span class="sxs-lookup"><span data-stu-id="0d62f-126"><span id="DXFILEERR_BADFILEVERSION"></span><span id="dxfileerr_badfileversion"></span>**DXFILEERR\_BADFILEVERSION**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-127">La versión del archivo no es válida.</span><span class="sxs-lookup"><span data-stu-id="0d62f-127">File version is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-128"><span id="DXFILEERR_BADINTRINSICS"></span><span id="dxfileerr_badintrinsics"></span>**DXFILEERR \_ BADINTRINSICS**</span><span class="sxs-lookup"><span data-stu-id="0d62f-128"><span id="DXFILEERR_BADINTRINSICS"></span><span id="dxfileerr_badintrinsics"></span>**DXFILEERR\_BADINTRINSICS**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-129">Los intrínsecos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="0d62f-129">Intrinsics are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-130"><span id="DXFILEERR_BADOBJECT"></span><span id="dxfileerr_badobject"></span>**DXFILEERR \_ BADOBJECT**</span><span class="sxs-lookup"><span data-stu-id="0d62f-130"><span id="DXFILEERR_BADOBJECT"></span><span id="dxfileerr_badobject"></span>**DXFILEERR\_BADOBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-131">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="0d62f-131">Object is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-132"><span id="DXFILEERR_BADRESOURCE"></span><span id="dxfileerr_badresource"></span>**DXFILEERR \_ BADRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="0d62f-132"><span id="DXFILEERR_BADRESOURCE"></span><span id="dxfileerr_badresource"></span>**DXFILEERR\_BADRESOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-133">El recurso no es válido.</span><span class="sxs-lookup"><span data-stu-id="0d62f-133">Resource is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-134"><span id="DXFILEERR_BADSTREAMHANDLE"></span><span id="dxfileerr_badstreamhandle"></span>**DXFILEERR \_ BADSTREAMHANDLE**</span><span class="sxs-lookup"><span data-stu-id="0d62f-134"><span id="DXFILEERR_BADSTREAMHANDLE"></span><span id="dxfileerr_badstreamhandle"></span>**DXFILEERR\_BADSTREAMHANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-135">El identificador de secuencia no es válido.</span><span class="sxs-lookup"><span data-stu-id="0d62f-135">Stream handle is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-136"><span id="DXFILEERR_BADTYPE"></span><span id="dxfileerr_badtype"></span>**DXFILEERR \_ BADTYPE**</span><span class="sxs-lookup"><span data-stu-id="0d62f-136"><span id="DXFILEERR_BADTYPE"></span><span id="dxfileerr_badtype"></span>**DXFILEERR\_BADTYPE**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-137">El tipo de objeto no es válido.</span><span class="sxs-lookup"><span data-stu-id="0d62f-137">Object type is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-138"><span id="DXFILEERR_BADVALUE"></span><span id="dxfileerr_badvalue"></span>**DXFILEERR \_ BADVALUE**</span><span class="sxs-lookup"><span data-stu-id="0d62f-138"><span id="DXFILEERR_BADVALUE"></span><span id="dxfileerr_badvalue"></span>**DXFILEERR\_BADVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-139">El parámetro no es válido.</span><span class="sxs-lookup"><span data-stu-id="0d62f-139">Parameter is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-140"><span id="DXFILEERR_FILENOTFOUND"></span><span id="dxfileerr_filenotfound"></span>**DXFILEERR \_ FILENOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="0d62f-140"><span id="DXFILEERR_FILENOTFOUND"></span><span id="dxfileerr_filenotfound"></span>**DXFILEERR\_FILENOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-141">No se encontró el archivo.</span><span class="sxs-lookup"><span data-stu-id="0d62f-141">File could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-142"><span id="DXFILEERR_INTERNALERROR"></span><span id="dxfileerr_internalerror"></span>**DXFILEERR \_ INTERNALERROR**</span><span class="sxs-lookup"><span data-stu-id="0d62f-142"><span id="DXFILEERR_INTERNALERROR"></span><span id="dxfileerr_internalerror"></span>**DXFILEERR\_INTERNALERROR**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-143">Se produjo un error interno.</span><span class="sxs-lookup"><span data-stu-id="0d62f-143">Internal error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-144"><span id="DXFILEERR_NOINTERNET"></span><span id="dxfileerr_nointernet"></span>**DXFILEERR \_ NOinternet**</span><span class="sxs-lookup"><span data-stu-id="0d62f-144"><span id="DXFILEERR_NOINTERNET"></span><span id="dxfileerr_nointernet"></span>**DXFILEERR\_NOINTERNET**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-145">No se encontró la conexión a Internet.</span><span class="sxs-lookup"><span data-stu-id="0d62f-145">Internet connection not found.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-146"><span id="DXFILEERR_NOMOREDATA"></span><span id="dxfileerr_nomoredata"></span>**DXFILEERR \_ NOMOREDATA**</span><span class="sxs-lookup"><span data-stu-id="0d62f-146"><span id="DXFILEERR_NOMOREDATA"></span><span id="dxfileerr_nomoredata"></span>**DXFILEERR\_NOMOREDATA**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-147">No hay más datos disponibles.</span><span class="sxs-lookup"><span data-stu-id="0d62f-147">No further data is available.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-148"><span id="DXFILEERR_NOMOREOBJECTS"></span><span id="dxfileerr_nomoreobjects"></span>**DXFILEERR \_ NOMOREOBJECTS**</span><span class="sxs-lookup"><span data-stu-id="0d62f-148"><span id="DXFILEERR_NOMOREOBJECTS"></span><span id="dxfileerr_nomoreobjects"></span>**DXFILEERR\_NOMOREOBJECTS**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-149">Se han enumerado todos los objetos.</span><span class="sxs-lookup"><span data-stu-id="0d62f-149">All objects have been enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-150"><span id="DXFILEERR_NOMORESTREAMHANDLES"></span><span id="dxfileerr_nomorestreamhandles"></span>**DXFILEERR \_ NOMORESTREAMHANDLES**</span><span class="sxs-lookup"><span data-stu-id="0d62f-150"><span id="DXFILEERR_NOMORESTREAMHANDLES"></span><span id="dxfileerr_nomorestreamhandles"></span>**DXFILEERR\_NOMORESTREAMHANDLES**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-151">No hay identificadores de flujo disponibles.</span><span class="sxs-lookup"><span data-stu-id="0d62f-151">No stream handles are available.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-152"><span id="DXFILEERR_NOTDONEYET"></span><span id="dxfileerr_notdoneyet"></span>**DXFILEERR \_ NOTDONEYET**</span><span class="sxs-lookup"><span data-stu-id="0d62f-152"><span id="DXFILEERR_NOTDONEYET"></span><span id="dxfileerr_notdoneyet"></span>**DXFILEERR\_NOTDONEYET**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-153">La operación no ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="0d62f-153">Operation has not completed.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-154"><span id="DXFILEERR_NOTFOUND"></span><span id="dxfileerr_notfound"></span>**DXFILEERR \_ NOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="0d62f-154"><span id="DXFILEERR_NOTFOUND"></span><span id="dxfileerr_notfound"></span>**DXFILEERR\_NOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-155">No se pudo encontrar el objeto.</span><span class="sxs-lookup"><span data-stu-id="0d62f-155">Object could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-156"><span id="DXFILEERR_PARSEERROR"></span><span id="dxfileerr_parseerror"></span>**DXFILEERR \_ Nº**</span><span class="sxs-lookup"><span data-stu-id="0d62f-156"><span id="DXFILEERR_PARSEERROR"></span><span id="dxfileerr_parseerror"></span>**DXFILEERR\_PARSEERROR**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-157">No se pudo analizar el archivo.</span><span class="sxs-lookup"><span data-stu-id="0d62f-157">File could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-158"><span id="DXFILEERR_RESOURCENOTFOUND"></span><span id="dxfileerr_resourcenotfound"></span>**DXFILEERR \_ RESOURCENOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="0d62f-158"><span id="DXFILEERR_RESOURCENOTFOUND"></span><span id="dxfileerr_resourcenotfound"></span>**DXFILEERR\_RESOURCENOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-159">No se encontró el recurso.</span><span class="sxs-lookup"><span data-stu-id="0d62f-159">Resource could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-160"><span id="DXFILEERR_NOTEMPLATE"></span><span id="dxfileerr_notemplate"></span>**DXFILEERR \_ NOtemplate**</span><span class="sxs-lookup"><span data-stu-id="0d62f-160"><span id="DXFILEERR_NOTEMPLATE"></span><span id="dxfileerr_notemplate"></span>**DXFILEERR\_NOTEMPLATE**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-161">No hay ninguna plantilla disponible.</span><span class="sxs-lookup"><span data-stu-id="0d62f-161">No template available.</span></span>

</dd> <dt>

<span data-ttu-id="0d62f-162"><span id="DXFILEERR_URLNOTFOUND"></span><span id="dxfileerr_urlnotfound"></span>**DXFILEERR \_ URLNOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="0d62f-162"><span id="DXFILEERR_URLNOTFOUND"></span><span id="dxfileerr_urlnotfound"></span>**DXFILEERR\_URLNOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="0d62f-163">No se encontró la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="0d62f-163">URL could not be found.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d62f-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d62f-164">Requirements</span></span>



| <span data-ttu-id="0d62f-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d62f-165">Requirement</span></span> | <span data-ttu-id="0d62f-166">Value</span><span class="sxs-lookup"><span data-stu-id="0d62f-166">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0d62f-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d62f-167">Header</span></span><br/> | <dl> <span data-ttu-id="0d62f-168"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d62f-168"><dt>DXFile.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d62f-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d62f-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d62f-170">Referencia de archivo X (heredado)</span><span class="sxs-lookup"><span data-stu-id="0d62f-170">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 




