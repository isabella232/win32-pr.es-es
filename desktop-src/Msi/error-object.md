---
description: El objeto error devuelve la información de un solo error de combinación.
ms.assetid: 38025e21-2d31-40f8-a088-2d3912c2893e
title: Objeto error (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error
- IMsmError
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 36fce310e6f75889ba5092f4fe43b6ca52ee2963
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653472"
---
# <a name="error-object"></a><span data-ttu-id="e441a-103">Objeto de error</span><span class="sxs-lookup"><span data-stu-id="e441a-103">Error object</span></span>

<span data-ttu-id="e441a-104">El objeto **error** devuelve la información de un solo error de combinación.</span><span class="sxs-lookup"><span data-stu-id="e441a-104">The **Error** object returns the information of a single merge error.</span></span>

## <a name="members"></a><span data-ttu-id="e441a-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="e441a-105">Members</span></span>

<span data-ttu-id="e441a-106">El objeto de **error** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e441a-106">The **Error** object has these types of members:</span></span>

-   [<span data-ttu-id="e441a-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e441a-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e441a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e441a-108">Properties</span></span>

<span data-ttu-id="e441a-109">El objeto de **error** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e441a-109">The **Error** object has these properties.</span></span>



| <span data-ttu-id="e441a-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e441a-110">Property</span></span>                                                | <span data-ttu-id="e441a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e441a-111">Description</span></span>                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e441a-112">**DatabaseKeys**</span><span class="sxs-lookup"><span data-stu-id="e441a-112">**DatabaseKeys**</span></span>](error-databasekeys.md)<br/>   | <span data-ttu-id="e441a-113">Devuelve las claves principales de la fila de la tabla de base de datos que provocó el error.</span><span class="sxs-lookup"><span data-stu-id="e441a-113">Returns the primary keys of the row in the database table that caused the error.</span></span><br/> |
| [<span data-ttu-id="e441a-114">**DatabaseTable**</span><span class="sxs-lookup"><span data-stu-id="e441a-114">**DatabaseTable**</span></span>](error-databasetable.md)<br/> | <span data-ttu-id="e441a-115">Devuelve el nombre de la tabla de la base de datos que produce el error.</span><span class="sxs-lookup"><span data-stu-id="e441a-115">Returns the table name of the table in the database causing the error.</span></span><br/>           |
| [<span data-ttu-id="e441a-116">**Idioma**</span><span class="sxs-lookup"><span data-stu-id="e441a-116">**Language**</span></span>](error-language.md)<br/>           | <span data-ttu-id="e441a-117">Devuelve el idioma del error.</span><span class="sxs-lookup"><span data-stu-id="e441a-117">Return the language of the error.</span></span><br/>                                                |
| [<span data-ttu-id="e441a-118">**ModuleKeys**</span><span class="sxs-lookup"><span data-stu-id="e441a-118">**ModuleKeys**</span></span>](error-modulekeys.md)<br/>       | <span data-ttu-id="e441a-119">Devuelve las claves principales de la fila de la tabla de módulos que provocó el error.</span><span class="sxs-lookup"><span data-stu-id="e441a-119">Returns the primary keys of the row in the module table that caused the error.</span></span><br/>   |
| [<span data-ttu-id="e441a-120">**ModuleTable**</span><span class="sxs-lookup"><span data-stu-id="e441a-120">**ModuleTable**</span></span>](error-moduletable.md)<br/>     | <span data-ttu-id="e441a-121">Devuelve el nombre de tabla de la tabla del módulo que produce el error.</span><span class="sxs-lookup"><span data-stu-id="e441a-121">Returns the table name of the table in the module causing the error.</span></span><br/>             |
| [<span data-ttu-id="e441a-122">**Ruta**</span><span class="sxs-lookup"><span data-stu-id="e441a-122">**Path**</span></span>](error-path.md)<br/>                   | <span data-ttu-id="e441a-123">Devuelve la ruta de acceso al archivo o directorio que provoca el error.</span><span class="sxs-lookup"><span data-stu-id="e441a-123">Return the path to the file or directory causing the error.</span></span> <span data-ttu-id="e441a-124">Actualmente no se usa.</span><span class="sxs-lookup"><span data-stu-id="e441a-124">Currently unused.</span></span><br/>    |
| [<span data-ttu-id="e441a-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e441a-125">**Type**</span></span>](error-type.md)<br/>                   | <span data-ttu-id="e441a-126">Devuelve el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="e441a-126">Return the type of error.</span></span><br/>                                                        |



 

## <a name="c"></a><span data-ttu-id="e441a-127">C++</span><span class="sxs-lookup"><span data-stu-id="e441a-127">C++</span></span>

<span data-ttu-id="e441a-128">interfaz **IMsmError: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="e441a-128">interface **IMsmError : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="e441a-129">IDENTIFICADOR de interfaz</span><span class="sxs-lookup"><span data-stu-id="e441a-129">Interface ID</span></span>



| <span data-ttu-id="e441a-130">Constante</span><span class="sxs-lookup"><span data-stu-id="e441a-130">Constant</span></span>           | <span data-ttu-id="e441a-131">Value</span><span class="sxs-lookup"><span data-stu-id="e441a-131">Value</span></span>                                  |
|--------------------|----------------------------------------|
| <span data-ttu-id="e441a-132">**\_IMSMERROR IID**</span><span class="sxs-lookup"><span data-stu-id="e441a-132">**IID\_IMsmError**</span></span> | <span data-ttu-id="e441a-133">{0ADDA828-2C26-11D2-AD65-00A0C9AF11A6}</span><span class="sxs-lookup"><span data-stu-id="e441a-133">{0ADDA828-2C26-11D2-AD65-00A0C9AF11A6}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="e441a-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e441a-134">Requirements</span></span>



| <span data-ttu-id="e441a-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e441a-135">Requirement</span></span> | <span data-ttu-id="e441a-136">Value</span><span class="sxs-lookup"><span data-stu-id="e441a-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e441a-137">Versión</span><span class="sxs-lookup"><span data-stu-id="e441a-137">Version</span></span><br/> | <span data-ttu-id="e441a-138">Mergemod.dll 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="e441a-138">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="e441a-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e441a-139">Header</span></span><br/>  | <dl> <span data-ttu-id="e441a-140"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="e441a-140"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="e441a-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e441a-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="e441a-142"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e441a-142"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




