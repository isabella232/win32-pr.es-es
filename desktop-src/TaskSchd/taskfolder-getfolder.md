---
title: Propiedad TaskFolder.GetFolder
description: Para el scripting, obtiene una carpeta que contiene tareas en una ubicación especificada.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- Propiedad GetFolder Programador de tareas
- Propiedad GetFolder Programador de tareas , objeto TaskFolder
- Objeto TaskFolder Programador de tareas , propiedad GetFolder
topic_type:
- apiref
api_name:
- TaskFolder.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c65b3f50cc5b8ab75bb041a61b36ad66bb35891
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387034"
---
# <a name="taskfoldergetfolder-property"></a><span data-ttu-id="6b9cc-106">Propiedad TaskFolder.GetFolder</span><span class="sxs-lookup"><span data-stu-id="6b9cc-106">TaskFolder.GetFolder property</span></span>

<span data-ttu-id="6b9cc-107">Para el scripting, obtiene una carpeta que contiene tareas en una ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="6b9cc-107">For scripting, gets a folder that contains tasks at a specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b9cc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b9cc-108">Syntax</span></span>


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="6b9cc-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6b9cc-109">Property value</span></span>

<span data-ttu-id="6b9cc-110">Ruta de acceso (ubicación) a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="6b9cc-110">The path (location) to the folder.</span></span> <span data-ttu-id="6b9cc-111">No use una barra diagonal inversa después del nombre de la última carpeta en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="6b9cc-111">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="6b9cc-112">La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="6b9cc-112">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="6b9cc-113">Un ejemplo de una ruta de acceso de carpeta de tareas, en la carpeta de tareas raíz, \\ es MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="6b9cc-113">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="6b9cc-114">No se puede usar el carácter '.' para especificar la carpeta de tareas actual y '..'.</span><span class="sxs-lookup"><span data-stu-id="6b9cc-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="6b9cc-115">no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="6b9cc-115">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6b9cc-116">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="6b9cc-116">Error codes</span></span>

<span data-ttu-id="6b9cc-117">Carpeta en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="6b9cc-117">The folder at the specified location.</span></span> <span data-ttu-id="6b9cc-118">La carpeta es un [**objeto TaskFolder.**](taskfolder.md)</span><span class="sxs-lookup"><span data-stu-id="6b9cc-118">The folder is a [**TaskFolder**](taskfolder.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b9cc-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b9cc-119">Requirements</span></span>



| <span data-ttu-id="6b9cc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b9cc-120">Requirement</span></span> | <span data-ttu-id="6b9cc-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6b9cc-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b9cc-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b9cc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6b9cc-123">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="6b9cc-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6b9cc-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b9cc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6b9cc-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6b9cc-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6b9cc-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6b9cc-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="6b9cc-127"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6b9cc-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6b9cc-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6b9cc-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b9cc-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b9cc-129"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





