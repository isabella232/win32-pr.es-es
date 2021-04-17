---
description: El objeto de dependencia devuelve un módulo del que depende el módulo actual y que aún no se ha combinado en la base de datos de instalación actual.
ms.assetid: 3157f07d-99de-4628-9b03-eb86eb4896a4
title: Objeto de dependencia (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dependency
- IMsmDependency
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 24b215b67d22d27639f3e002590e7d08dd54b0c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653677"
---
# <a name="dependency-object"></a><span data-ttu-id="92186-103">Objeto de dependencia</span><span class="sxs-lookup"><span data-stu-id="92186-103">Dependency object</span></span>

<span data-ttu-id="92186-104">El objeto de **dependencia** devuelve un módulo del que depende el módulo actual y que aún no se ha combinado en la base de datos de instalación actual.</span><span class="sxs-lookup"><span data-stu-id="92186-104">The **Dependency** object returns a module that the current module is dependent upon and which has not yet been merged into the current installation database.</span></span>

## <a name="members"></a><span data-ttu-id="92186-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="92186-105">Members</span></span>

<span data-ttu-id="92186-106">El objeto de **dependencia** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="92186-106">The **Dependency** object has these types of members:</span></span>

-   [<span data-ttu-id="92186-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="92186-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92186-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="92186-108">Properties</span></span>

<span data-ttu-id="92186-109">El objeto de **dependencia** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="92186-109">The **Dependency** object has these properties.</span></span>



| <span data-ttu-id="92186-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="92186-110">Property</span></span>                                           | <span data-ttu-id="92186-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="92186-111">Description</span></span>                                             |
|:---------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="92186-112">**Idioma**</span><span class="sxs-lookup"><span data-stu-id="92186-112">**Language**</span></span>](dependency-language.md)<br/> | <span data-ttu-id="92186-113">Devuelve el idioma del módulo.</span><span class="sxs-lookup"><span data-stu-id="92186-113">Return the language of the module.</span></span><br/>           |
| [<span data-ttu-id="92186-114">**Módulo**</span><span class="sxs-lookup"><span data-stu-id="92186-114">**Module**</span></span>](dependency-module.md)<br/>     | <span data-ttu-id="92186-115">Devuelve el identificador de módulo del módulo necesario.</span><span class="sxs-lookup"><span data-stu-id="92186-115">Return the module ID of the required module.</span></span><br/> |
| [<span data-ttu-id="92186-116">**Versión**</span><span class="sxs-lookup"><span data-stu-id="92186-116">**Version**</span></span>](dependency-version.md)<br/>   | <span data-ttu-id="92186-117">Devuelve la versión del módulo necesario.</span><span class="sxs-lookup"><span data-stu-id="92186-117">Return the version of the required module.</span></span><br/>   |



 

## <a name="c"></a><span data-ttu-id="92186-118">C++</span><span class="sxs-lookup"><span data-stu-id="92186-118">C++</span></span>

<span data-ttu-id="92186-119">interfaz **IMsmDependency: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="92186-119">interface **IMsmDependency : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="92186-120">IDENTIFICADOR de interfaz</span><span class="sxs-lookup"><span data-stu-id="92186-120">Interface ID</span></span>



| <span data-ttu-id="92186-121">Constante</span><span class="sxs-lookup"><span data-stu-id="92186-121">Constant</span></span>                | <span data-ttu-id="92186-122">Value</span><span class="sxs-lookup"><span data-stu-id="92186-122">Value</span></span>                                  |
|-------------------------|----------------------------------------|
| <span data-ttu-id="92186-123">**\_IMSMDEPENDENCY IID**</span><span class="sxs-lookup"><span data-stu-id="92186-123">**IID\_IMsmDependency**</span></span> | <span data-ttu-id="92186-124">{0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6}</span><span class="sxs-lookup"><span data-stu-id="92186-124">{0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="92186-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92186-125">Requirements</span></span>



| <span data-ttu-id="92186-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="92186-126">Requirement</span></span> | <span data-ttu-id="92186-127">Value</span><span class="sxs-lookup"><span data-stu-id="92186-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92186-128">Versión</span><span class="sxs-lookup"><span data-stu-id="92186-128">Version</span></span><br/> | <span data-ttu-id="92186-129">Mergemod.dll 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="92186-129">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="92186-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92186-130">Header</span></span><br/>  | <dl> <span data-ttu-id="92186-131"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="92186-131"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="92186-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="92186-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="92186-133"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92186-133"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




