---
description: El método CreateSourceImage del objeto Merge permite al cliente extraer los archivos de un módulo en una imagen de origen en disco después de una combinación, teniendo en cuenta los cambios realizados en el módulo que podrían haberse realizado durante la configuración del módulo.
ms.assetid: c3e3465a-d5a7-4fcc-b26a-5a8c763c23d9
title: Método Merge. CreateSourceImage (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CreateSourceImage
- IMsmMerge.CreateSourceImage
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: e8d9365a69ff6f33c2989e9102bac7c9c22166aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670801"
---
# <a name="mergecreatesourceimage-method"></a><span data-ttu-id="3ab8c-103">Merge. CreateSourceImage (método)</span><span class="sxs-lookup"><span data-stu-id="3ab8c-103">Merge.CreateSourceImage method</span></span>

<span data-ttu-id="3ab8c-104">El método **CreateSourceImage** del objeto [**Merge**](merge-object.md) permite al cliente extraer los archivos de un módulo en una imagen de origen en disco después de una combinación, teniendo en cuenta los cambios realizados en el módulo que podrían haberse realizado durante la configuración del módulo.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-104">The **CreateSourceImage** method of the [**Merge**](merge-object.md) object allows the client to extract the files from a module to a source image on disk after a merge, taking into account changes to the module that might have been made during module configuration.</span></span> <span data-ttu-id="3ab8c-105">La lista de archivos que se van a extraer se toma de la tabla de archivos del módulo durante el proceso de mezcla.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-105">The list of files to be extracted is taken from the file table of the module during the merge process.</span></span> <span data-ttu-id="3ab8c-106">La lista de archivos se compone de todos los archivos copiados correctamente de la tabla de archivos del módulo en la base de datos de destino.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-106">The list of files consists of every file successfully copied from the file table of the module to the target database.</span></span> <span data-ttu-id="3ab8c-107">Las entradas de la tabla de archivos que no se copiaron debido a conflictos de clave principal con las filas existentes en la base de datos no forman parte de esta lista.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-107">File table entries that were not copied due to primary key conflicts with existing rows in the database are not a part of this list.</span></span> <span data-ttu-id="3ab8c-108">En el momento de la creación de la imagen, el directorio de cada uno de estos archivos procede de la base de datos abierta (posterior a la mezcla).</span><span class="sxs-lookup"><span data-stu-id="3ab8c-108">At image creation time, the directory for each of these files comes from the open (post-merge) database.</span></span> <span data-ttu-id="3ab8c-109">La ruta de acceso especificada en el parámetro *path* es la raíz de la imagen de origen de la instalación.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-109">The path specified in the *Path* parameter is the root of the source image for the install.</span></span> <span data-ttu-id="3ab8c-110">*fLongFileNames* determina si se usan nombres de archivo largos para los segmentos de ruta de acceso y los nombres de archivo finales.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-110">*fLongFileNames* determines whether or not long file names are used for both path segments and final file names.</span></span> <span data-ttu-id="3ab8c-111">Se produce un error en la función si no hay ninguna base de datos abierta, no hay ningún módulo abierto o no se ha realizado ninguna combinación.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-111">The function fails if no database is open, no module is open, or no merge has been performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ab8c-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ab8c-112">Syntax</span></span>


```JScript
Merge.CreateSourceImage(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a><span data-ttu-id="3ab8c-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3ab8c-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ab8c-114">*Ruta de acceso*</span><span class="sxs-lookup"><span data-stu-id="3ab8c-114">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="3ab8c-115">La ruta de acceso de la raíz de la imagen de origen para la instalación.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-115">The path of the root of the source image for the install.</span></span>

</dd> <dt>

<span data-ttu-id="3ab8c-116">*fLongFileNames*</span><span class="sxs-lookup"><span data-stu-id="3ab8c-116">*fLongFileNames*</span></span> 
</dt> <dd>

<span data-ttu-id="3ab8c-117">*fLongFileNames* determina si se usan nombres de archivo largos para los segmentos de ruta de acceso y los nombres de archivo finales.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-117">*fLongFileNames* determines whether or not long file names are used for both path segments and final file names.</span></span>

</dd> <dt>

<span data-ttu-id="3ab8c-118">*pFilePaths*</span><span class="sxs-lookup"><span data-stu-id="3ab8c-118">*pFilePaths*</span></span> 
</dt> <dd>

<span data-ttu-id="3ab8c-119">Esta es una lista de rutas de acceso completas para los archivos que se extrajeron correctamente.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-119">This is a list of fully qualified paths for the files that were successfully extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ab8c-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ab8c-120">Return value</span></span>

<span data-ttu-id="3ab8c-121">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ab8c-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ab8c-122">Remarks</span></span>

<span data-ttu-id="3ab8c-123">Se sobrescriben los archivos del directorio de destino con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-123">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="3ab8c-124">Si aún no existe, se crea la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="3ab8c-124">The path is created if it does not already exist.</span></span>

### <a name="c"></a><span data-ttu-id="3ab8c-125">C++</span><span class="sxs-lookup"><span data-stu-id="3ab8c-125">C++</span></span>

<span data-ttu-id="3ab8c-126">Consulte función [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) .</span><span class="sxs-lookup"><span data-stu-id="3ab8c-126">See [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ab8c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ab8c-127">Requirements</span></span>



| <span data-ttu-id="3ab8c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ab8c-128">Requirement</span></span> | <span data-ttu-id="3ab8c-129">Value</span><span class="sxs-lookup"><span data-stu-id="3ab8c-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ab8c-130">Versión</span><span class="sxs-lookup"><span data-stu-id="3ab8c-130">Version</span></span><br/> | <span data-ttu-id="3ab8c-131">Mergemod.dll 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="3ab8c-131">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="3ab8c-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ab8c-132">Header</span></span><br/>  | <dl> <span data-ttu-id="3ab8c-133"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ab8c-133"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ab8c-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3ab8c-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="3ab8c-135"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ab8c-135"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




