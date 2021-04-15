---
description: El método ExtractFilesEx del objeto Merge extrae el archivo. cab incrustado de un módulo y, a continuación, escribe esos archivos en el directorio de destino.
ms.assetid: 8b063052-4f92-466a-9c52-bda26ed13d5c
title: Método Merge. ExtractFilesEx (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFilesEx
- IMsmMerge.ExtractFilesEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: be6aa1001be0d3ecd6cbb9c4cd1d8c04b4649f10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653951"
---
# <a name="mergeextractfilesex-method"></a><span data-ttu-id="96759-103">Merge. ExtractFilesEx (método)</span><span class="sxs-lookup"><span data-stu-id="96759-103">Merge.ExtractFilesEx method</span></span>

<span data-ttu-id="96759-104">El método **ExtractFilesEx** del objeto [**Merge**](merge-object.md) extrae el archivo. cab incrustado de un módulo y, a continuación, escribe esos archivos en el directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="96759-104">The **ExtractFilesEx** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and then writes those files to the destination directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="96759-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96759-105">Syntax</span></span>


```JScript
Merge.ExtractFilesEx(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a><span data-ttu-id="96759-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96759-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96759-107">*Ruta de acceso*</span><span class="sxs-lookup"><span data-stu-id="96759-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="96759-108">Directorio de destino completo.</span><span class="sxs-lookup"><span data-stu-id="96759-108">The fully qualified destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="96759-109">*fLongFileNames*</span><span class="sxs-lookup"><span data-stu-id="96759-109">*fLongFileNames*</span></span> 
</dt> <dd>

<span data-ttu-id="96759-110">Se establece para especificar el uso de nombres de archivo largos para los segmentos de ruta de acceso y los nombres de archivo finales.</span><span class="sxs-lookup"><span data-stu-id="96759-110">Set to specify using long file names for path segments and final file names.</span></span>

</dd> <dt>

<span data-ttu-id="96759-111">*pFilePaths*</span><span class="sxs-lookup"><span data-stu-id="96759-111">*pFilePaths*</span></span> 
</dt> <dd>

<span data-ttu-id="96759-112">Esta es una lista de rutas de acceso completas para los archivos que se extrajeron correctamente.</span><span class="sxs-lookup"><span data-stu-id="96759-112">This is a list of fully qualified paths for the files that were successfully extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96759-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96759-113">Return value</span></span>

<span data-ttu-id="96759-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="96759-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="96759-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96759-115">Remarks</span></span>

<span data-ttu-id="96759-116">Se sobrescriben los archivos del directorio de destino con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="96759-116">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="96759-117">Si aún no existe, se crea la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="96759-117">The path is created if it does not already exist.</span></span>

### <a name="c"></a><span data-ttu-id="96759-118">C++</span><span class="sxs-lookup"><span data-stu-id="96759-118">C++</span></span>

<span data-ttu-id="96759-119">Consulte función [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) .</span><span class="sxs-lookup"><span data-stu-id="96759-119">See [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="96759-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96759-120">Requirements</span></span>



| <span data-ttu-id="96759-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="96759-121">Requirement</span></span> | <span data-ttu-id="96759-122">Value</span><span class="sxs-lookup"><span data-stu-id="96759-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96759-123">Versión</span><span class="sxs-lookup"><span data-stu-id="96759-123">Version</span></span><br/> | <span data-ttu-id="96759-124">Mergemod.dll 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="96759-124">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="96759-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96759-125">Header</span></span><br/>  | <dl> <span data-ttu-id="96759-126"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="96759-126"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="96759-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="96759-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="96759-128"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96759-128"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




