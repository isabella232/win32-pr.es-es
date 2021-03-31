---
title: Propiedad TaskFolder. GetFolder
description: En el caso de scripting, obtiene una carpeta que contiene tareas en una ubicación especificada.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- Propiedad GetFolder Programador de tareas
- Propiedad GetFolder Programador de tareas, objeto TaskFolder
- Programador de tareas de objeto TaskFolder, propiedad GetFolder
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
ms.openlocfilehash: 308173660ffff7d2062febd087c89cb63bcd8d99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150046"
---
# <a name="taskfoldergetfolder-property"></a><span data-ttu-id="d10aa-106">Propiedad TaskFolder. GetFolder</span><span class="sxs-lookup"><span data-stu-id="d10aa-106">TaskFolder.GetFolder property</span></span>

<span data-ttu-id="d10aa-107">En el caso de scripting, obtiene una carpeta que contiene tareas en una ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="d10aa-107">For scripting, gets a folder that contains tasks at a specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="d10aa-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d10aa-108">Syntax</span></span>


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="d10aa-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d10aa-109">Property value</span></span>

<span data-ttu-id="d10aa-110">La ruta de acceso (ubicación) de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d10aa-110">The path (location) to the folder.</span></span> <span data-ttu-id="d10aa-111">No use una barra diagonal inversa después del nombre de la última carpeta en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="d10aa-111">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="d10aa-112">La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \) .</span><span class="sxs-lookup"><span data-stu-id="d10aa-112">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="d10aa-113">Un ejemplo de una ruta de carpeta de tareas, en la carpeta de tareas raíz, es \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="d10aa-113">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="d10aa-114">No se puede usar el carácter '. ' para especificar la carpeta de tareas actual y '.. '</span><span class="sxs-lookup"><span data-stu-id="d10aa-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="d10aa-115">no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="d10aa-115">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d10aa-116">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d10aa-116">Error codes</span></span>

<span data-ttu-id="d10aa-117">Carpeta en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="d10aa-117">The folder at the specified location.</span></span> <span data-ttu-id="d10aa-118">La carpeta es un objeto [**TaskFolder**](taskfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="d10aa-118">The folder is a [**TaskFolder**](taskfolder.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d10aa-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d10aa-119">Requirements</span></span>



| <span data-ttu-id="d10aa-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d10aa-120">Requirement</span></span> | <span data-ttu-id="d10aa-121">Value</span><span class="sxs-lookup"><span data-stu-id="d10aa-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d10aa-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d10aa-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d10aa-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d10aa-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d10aa-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d10aa-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d10aa-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d10aa-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d10aa-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d10aa-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="d10aa-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d10aa-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d10aa-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d10aa-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d10aa-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d10aa-129"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





