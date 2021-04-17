---
title: modificador/metadata_dir (MDMERGE)
description: El \_ modificador dir de/metadata especifica el directorio que contiene los archivos de metadatos de plataforma.
ms.assetid: E95D410B-D384-4337-B0A0-6D5DDA3BE699
keywords:
- /metadata_dir modificador MIDL
topic_type:
- apiref
api_name:
- /metadata_dir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd104ae63378056babdc804a93564be4005246c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681085"
---
# <a name="metadata_dir-switch-mdmerge"></a><span data-ttu-id="d1142-104">modificador/metadata_dir (MDMERGE)</span><span class="sxs-lookup"><span data-stu-id="d1142-104">/metadata_dir switch (MDMERGE)</span></span>

<span data-ttu-id="d1142-105">El modificador **\_ dir de/metadata** especifica el directorio que contiene los archivos de metadatos de plataforma.</span><span class="sxs-lookup"><span data-stu-id="d1142-105">The **/metadata\_dir** switch specifies the directory that contains platform metadata files.</span></span>

``` syntax
mdmerge /metadata_dir metadata_directory
```

## <a name="switch-options"></a><span data-ttu-id="d1142-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="d1142-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="d1142-107">*directorio de metadatos \_*</span><span class="sxs-lookup"><span data-stu-id="d1142-107">*metadata\_directory*</span></span> 
</dt> <dd>

<span data-ttu-id="d1142-108">Especifica el directorio que contiene los archivos de metadatos de plataforma.</span><span class="sxs-lookup"><span data-stu-id="d1142-108">Specifies the directory that contains platform metadata files.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1142-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1142-109">Remarks</span></span>

<span data-ttu-id="d1142-110">Use este modificador para especificar la ubicación del archivo de metadatos principal para Windows, que se denomina Windows. winmd.</span><span class="sxs-lookup"><span data-stu-id="d1142-110">Use this switch to specify the location of the main metadata file for Windows, which is named windows.winmd.</span></span>

## <a name="examples"></a><span data-ttu-id="d1142-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d1142-111">Examples</span></span>

<span data-ttu-id="d1142-112">**mdmerge/Metadata \_ dir dir1**</span><span class="sxs-lookup"><span data-stu-id="d1142-112">**mdmerge /metadata\_dir dir1**</span></span>

## <a name="requirements"></a><span data-ttu-id="d1142-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1142-113">Requirements</span></span>



| <span data-ttu-id="d1142-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1142-114">Requirement</span></span> | <span data-ttu-id="d1142-115">Value</span><span class="sxs-lookup"><span data-stu-id="d1142-115">Value</span></span> |
|-------------------|--------------------------------|
| <span data-ttu-id="d1142-116">Remoto</span><span class="sxs-lookup"><span data-stu-id="d1142-116">Client</span></span><br/> | <span data-ttu-id="d1142-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d1142-117">Windows 8</span></span><br/>           |
| <span data-ttu-id="d1142-118">Servidor</span><span class="sxs-lookup"><span data-stu-id="d1142-118">Server</span></span><br/> | <span data-ttu-id="d1142-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d1142-119">Windows Server 2012</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1142-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1142-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1142-121">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="d1142-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





