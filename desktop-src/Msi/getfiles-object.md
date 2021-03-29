---
description: El objeto GetFiles recupera los archivos necesarios en un idioma determinado del módulo. Requiere que ciertas acciones se realicen a través del objeto Merge antes de que todas las partes de esta interfaz devuelvan resultados válidos.
ms.assetid: f3bf64ec-75f7-43a6-bbd8-a51508c57002
title: Objeto GetFiles (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles
- IMsmGetFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8a26bb072b0b4a1f048ded76fbd52ffc6d42de62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653935"
---
# <a name="getfiles-object"></a><span data-ttu-id="745f1-104">GetFiles (objeto)</span><span class="sxs-lookup"><span data-stu-id="745f1-104">GetFiles object</span></span>

<span data-ttu-id="745f1-105">El objeto **GetFiles** recupera los archivos necesarios en un idioma determinado del módulo.</span><span class="sxs-lookup"><span data-stu-id="745f1-105">The **GetFiles** object retrieves the files needed in a particular language of the module.</span></span> <span data-ttu-id="745f1-106">Requiere que ciertas acciones se realicen a través del [objeto Merge](merge-object.md) antes de que todas las partes de esta interfaz devuelvan resultados válidos.</span><span class="sxs-lookup"><span data-stu-id="745f1-106">Requires certain actions be performed through the [Merge object](merge-object.md) before all parts of this interface returns valid results.</span></span>

## <a name="members"></a><span data-ttu-id="745f1-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="745f1-107">Members</span></span>

<span data-ttu-id="745f1-108">El objeto **GetFiles** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="745f1-108">The **GetFiles** object has these types of members:</span></span>

-   [<span data-ttu-id="745f1-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="745f1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="745f1-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="745f1-110">Properties</span></span>

<span data-ttu-id="745f1-111">El objeto **GetFiles** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="745f1-111">The **GetFiles** object has these properties.</span></span>



| <span data-ttu-id="745f1-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="745f1-112">Property</span></span>                                               | <span data-ttu-id="745f1-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="745f1-113">Description</span></span>                                                                                                                                                     |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="745f1-114">**ModuleFiles**</span><span class="sxs-lookup"><span data-stu-id="745f1-114">**ModuleFiles**</span></span>](getfiles-modulefiles.md)<br/> | <span data-ttu-id="745f1-115">La propiedad [**ModuleFiles**](getfiles-modulefiles.md) devuelve todas las claves principales de la [tabla de archivos](file-table.md) para el módulo actualmente abierto.</span><span class="sxs-lookup"><span data-stu-id="745f1-115">[**ModuleFiles**](getfiles-modulefiles.md) property returns all the primary keys of the [File table](file-table.md) for the currently open module.</span></span><br/> |



 

## <a name="c"></a><span data-ttu-id="745f1-116">C++</span><span class="sxs-lookup"><span data-stu-id="745f1-116">C++</span></span>

<span data-ttu-id="745f1-117">interfaz **IMsmGetFiles: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="745f1-117">interface **IMsmGetFiles : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="745f1-118">IDENTIFICADOR de interfaz</span><span class="sxs-lookup"><span data-stu-id="745f1-118">Interface ID</span></span>



| <span data-ttu-id="745f1-119">Constante</span><span class="sxs-lookup"><span data-stu-id="745f1-119">Constant</span></span>              | <span data-ttu-id="745f1-120">Value</span><span class="sxs-lookup"><span data-stu-id="745f1-120">Value</span></span>                                  |
|-----------------------|----------------------------------------|
| <span data-ttu-id="745f1-121">**\_IMSMGETFILES IID**</span><span class="sxs-lookup"><span data-stu-id="745f1-121">**IID\_IMsmGetFiles**</span></span> | <span data-ttu-id="745f1-122">{7041AE26-2D78-11D2-888A-00A0C981B015}</span><span class="sxs-lookup"><span data-stu-id="745f1-122">{7041AE26-2D78-11D2-888A-00A0C981B015}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="745f1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="745f1-123">Requirements</span></span>



| <span data-ttu-id="745f1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="745f1-124">Requirement</span></span> | <span data-ttu-id="745f1-125">Value</span><span class="sxs-lookup"><span data-stu-id="745f1-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="745f1-126">Versión</span><span class="sxs-lookup"><span data-stu-id="745f1-126">Version</span></span><br/> | <span data-ttu-id="745f1-127">Mergemod.dll 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="745f1-127">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="745f1-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="745f1-128">Header</span></span><br/>  | <dl> <span data-ttu-id="745f1-129"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="745f1-129"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="745f1-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="745f1-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="745f1-131"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="745f1-131"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




