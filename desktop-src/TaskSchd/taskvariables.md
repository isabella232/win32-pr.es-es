---
title: Objeto TaskVariables
description: Objeto de scripting que define las variables de tarea que se pueden pasar como parámetros a los controladores de tareas y los archivos ejecutables externos iniciados por las tareas.
ms.assetid: 194babe0-16bd-4a78-af45-139c9c7eacbe
keywords:
- Objeto TaskVariables Programador de tareas
- Programador de tareas de objeto TaskVariables, descrito
topic_type:
- apiref
api_name:
- TaskVariables
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fe20153b0d6d66ca6c7f263a8e76d5a4d480b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492244"
---
# <a name="taskvariables-object"></a><span data-ttu-id="8b249-105">Objeto TaskVariables</span><span class="sxs-lookup"><span data-stu-id="8b249-105">TaskVariables object</span></span>

<span data-ttu-id="8b249-106">Objeto de scripting que define las variables de tarea que se pueden pasar como parámetros a los controladores de tareas y los archivos ejecutables externos iniciados por las tareas.</span><span class="sxs-lookup"><span data-stu-id="8b249-106">Scripting object that defines task variables that can be passed as parameters to task handlers and external executables that are launched by tasks.</span></span>

## <a name="members"></a><span data-ttu-id="8b249-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8b249-107">Members</span></span>

<span data-ttu-id="8b249-108">El objeto **TaskVariables** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8b249-108">The **TaskVariables** object has these types of members:</span></span>

-   [<span data-ttu-id="8b249-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="8b249-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8b249-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="8b249-110">Methods</span></span>

<span data-ttu-id="8b249-111">El objeto **TaskVariables** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="8b249-111">The **TaskVariables** object has these methods.</span></span>



| <span data-ttu-id="8b249-112">Método</span><span class="sxs-lookup"><span data-stu-id="8b249-112">Method</span></span>                                         | <span data-ttu-id="8b249-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b249-113">Description</span></span>                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b249-114">**GetContext**</span><span class="sxs-lookup"><span data-stu-id="8b249-114">**GetContext**</span></span>](taskvariables-getcontext.md) | <span data-ttu-id="8b249-115">Se usa para compartir el contexto entre diferentes pasos y tareas que se encuentran en la misma instancia de trabajo.</span><span class="sxs-lookup"><span data-stu-id="8b249-115">Used to share the context between different steps and tasks that are in the same job instance.</span></span><br/> |
| [<span data-ttu-id="8b249-116">**GetInput**</span><span class="sxs-lookup"><span data-stu-id="8b249-116">**GetInput**</span></span>](taskvariables-getinput.md)     | <span data-ttu-id="8b249-117">Obtiene las variables de entrada para una tarea.</span><span class="sxs-lookup"><span data-stu-id="8b249-117">Gets the input variables for a task.</span></span><br/>                                                           |
| [<span data-ttu-id="8b249-118">**SetOutput**</span><span class="sxs-lookup"><span data-stu-id="8b249-118">**SetOutput**</span></span>](taskvariables-setoutput.md)   | <span data-ttu-id="8b249-119">Establece las variables de salida de una tarea.</span><span class="sxs-lookup"><span data-stu-id="8b249-119">Sets the output variables for a task.</span></span><br/>                                                          |



 

## <a name="requirements"></a><span data-ttu-id="8b249-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b249-120">Requirements</span></span>



| <span data-ttu-id="8b249-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b249-121">Requirement</span></span> | <span data-ttu-id="8b249-122">Value</span><span class="sxs-lookup"><span data-stu-id="8b249-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b249-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b249-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8b249-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8b249-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8b249-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b249-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8b249-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8b249-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8b249-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8b249-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="8b249-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8b249-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8b249-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8b249-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b249-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b249-130"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





