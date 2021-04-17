---
description: El método ExtractFiles del objeto Merge extrae el archivo. cab incrustado de un módulo y, a continuación, escribe esos archivos en el directorio de destino.
ms.assetid: 846355d6-32f2-4b04-91dc-acd60445fbd9
title: Merge. ExtractFiles (método) (Advpub. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFiles
- IMsmMerge.ExtractFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 3869dc37b841d386891eb70940054bd78805bf94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670800"
---
# <a name="mergeextractfiles-method"></a><span data-ttu-id="1b24d-103">Merge. ExtractFiles (método)</span><span class="sxs-lookup"><span data-stu-id="1b24d-103">Merge.ExtractFiles method</span></span>

<span data-ttu-id="1b24d-104">El método **ExtractFiles** del objeto [**Merge**](merge-object.md) extrae el archivo. cab incrustado de un módulo y, a continuación, escribe esos archivos en el directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="1b24d-104">The **ExtractFiles** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and then writes those files to the destination directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b24d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b24d-105">Syntax</span></span>


```JScript
Merge.ExtractFiles(
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="1b24d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b24d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b24d-107">*Ruta de acceso*</span><span class="sxs-lookup"><span data-stu-id="1b24d-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="1b24d-108">Directorio de destino completo.</span><span class="sxs-lookup"><span data-stu-id="1b24d-108">The fully qualified destination directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b24d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b24d-109">Return value</span></span>

<span data-ttu-id="1b24d-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1b24d-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b24d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b24d-111">Remarks</span></span>

<span data-ttu-id="1b24d-112">Se sobrescriben los archivos del directorio de destino con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="1b24d-112">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="1b24d-113">Si aún no existe, se crea la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="1b24d-113">The path is created if it does not already exist.</span></span>

<span data-ttu-id="1b24d-114">**ExtractFiles** siempre extrae los archivos con nombres de archivo cortos para la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="1b24d-114">**ExtractFiles** always extracts files using short file names for the path.</span></span> <span data-ttu-id="1b24d-115">Para utilizar nombres de archivo largos para la ruta de acceso, use el [**método ExtractFilesEx**](merge-extractfilesex.md).</span><span class="sxs-lookup"><span data-stu-id="1b24d-115">To use long file names for the path, use the [**ExtractFilesEx method**](merge-extractfilesex.md).</span></span>

### <a name="c"></a><span data-ttu-id="1b24d-116">C++</span><span class="sxs-lookup"><span data-stu-id="1b24d-116">C++</span></span>

<span data-ttu-id="1b24d-117">Vea [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) (función).</span><span class="sxs-lookup"><span data-stu-id="1b24d-117">See [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b24d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b24d-118">Requirements</span></span>



| <span data-ttu-id="1b24d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b24d-119">Requirement</span></span> | <span data-ttu-id="1b24d-120">Value</span><span class="sxs-lookup"><span data-stu-id="1b24d-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b24d-121">Versión</span><span class="sxs-lookup"><span data-stu-id="1b24d-121">Version</span></span><br/> | <span data-ttu-id="1b24d-122">Mergemod.dll 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="1b24d-122">Mergemod.dll 1.0 or later</span></span><br/>                                                                     |
| <span data-ttu-id="1b24d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b24d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1b24d-124"><dt>Advpub. h (incluye Mergemod. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b24d-124"><dt>Advpub.h (include Mergemod.h)</dt></span></span> </dl> |
| <span data-ttu-id="1b24d-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1b24d-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="1b24d-126"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b24d-126"><dt>Mergemod.dll</dt></span></span> </dl>                  |



 

 
