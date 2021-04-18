---
title: TaskFolder. CreateFolder, método
description: En el caso de los scripts, crea una carpeta para las tareas relacionadas.
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- CreateFolder (método) Programador de tareas
- Método CreateFolder Programador de tareas, objeto TaskFolder
- Programador de tareas de objeto TaskFolder, CreateFolder (método)
topic_type:
- apiref
api_name:
- TaskFolder.CreateFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ae66dadb0c943b1ca33be3e696ac1c8ca7d6234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676829"
---
# <a name="taskfoldercreatefolder-method"></a><span data-ttu-id="98b42-106">TaskFolder. CreateFolder, método</span><span class="sxs-lookup"><span data-stu-id="98b42-106">TaskFolder.CreateFolder method</span></span>

<span data-ttu-id="98b42-107">En el caso de los scripts, crea una carpeta para las tareas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="98b42-107">For scripting, creates a folder for related tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="98b42-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98b42-108">Syntax</span></span>


```VB
ppFolder = .CreateFolder( _
  ByVal folderName, _
  ByVal sddl _
)
```



## <a name="parameters"></a><span data-ttu-id="98b42-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98b42-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98b42-110">*nombrecarpeta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="98b42-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98b42-111">Nombre que se usa para identificar la carpeta.</span><span class="sxs-lookup"><span data-stu-id="98b42-111">The name that is used to identify the folder.</span></span> <span data-ttu-id="98b42-112">Si \\ se especifica "NombreCarpeta subcarpeta subfolder1 \\ SubFolder2", se creará el árbol de carpetas completo si las carpetas no existen.</span><span class="sxs-lookup"><span data-stu-id="98b42-112">If "FolderName\\SubFolder1\\SubFolder2" is specified, the entire folder tree will be created if the folders do not exist.</span></span> <span data-ttu-id="98b42-113">Este parámetro puede ser una ruta de acceso relativa a la instancia de [**TaskFolder**](taskfolder.md) actual.</span><span class="sxs-lookup"><span data-stu-id="98b42-113">This parameter can be a relative path to the current [**TaskFolder**](taskfolder.md) instance.</span></span> <span data-ttu-id="98b42-114">La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \) .</span><span class="sxs-lookup"><span data-stu-id="98b42-114">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="98b42-115">Un ejemplo de una ruta de carpeta de tareas, en la carpeta de tareas raíz, es \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="98b42-115">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="98b42-116">No se puede usar el carácter '. ' para especificar la carpeta de tareas actual y '.. '</span><span class="sxs-lookup"><span data-stu-id="98b42-116">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="98b42-117">no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="98b42-117">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="98b42-118">*SDDL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="98b42-118">*sddl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98b42-119">Descriptor de seguridad asociado a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="98b42-119">The security descriptor that is associated with the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98b42-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98b42-120">Return value</span></span>

<span data-ttu-id="98b42-121">Objeto [**TaskFolder**](taskfolder.md) que representa la nueva subcarpeta.</span><span class="sxs-lookup"><span data-stu-id="98b42-121">A [**TaskFolder**](taskfolder.md) object that represents the new subfolder.</span></span>

## <a name="requirements"></a><span data-ttu-id="98b42-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98b42-122">Requirements</span></span>



| <span data-ttu-id="98b42-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="98b42-123">Requirement</span></span> | <span data-ttu-id="98b42-124">Value</span><span class="sxs-lookup"><span data-stu-id="98b42-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98b42-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98b42-125">Minimum supported client</span></span><br/> | <span data-ttu-id="98b42-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="98b42-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="98b42-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98b42-127">Minimum supported server</span></span><br/> | <span data-ttu-id="98b42-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="98b42-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="98b42-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="98b42-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="98b42-130"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="98b42-130"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="98b42-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="98b42-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98b42-132"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98b42-132"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98b42-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="98b42-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98b42-134">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="98b42-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





