---
title: TaskFolder. DeleteFolder, método
description: En el caso de scripting, elimina una subcarpeta de la carpeta principal.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- Método DeleteFolder Programador de tareas
- Método DeleteFolder Programador de tareas, objeto TaskFolder
- Programador de tareas de objeto TaskFolder, método DeleteFolder
topic_type:
- apiref
api_name:
- TaskFolder.DeleteFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea9b8aaa7da7710cedc49e10d6be2a203f62b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491374"
---
# <a name="taskfolderdeletefolder-method"></a><span data-ttu-id="5f074-106">TaskFolder. DeleteFolder, método</span><span class="sxs-lookup"><span data-stu-id="5f074-106">TaskFolder.DeleteFolder method</span></span>

<span data-ttu-id="5f074-107">En el caso de scripting, elimina una subcarpeta de la carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="5f074-107">For scripting, deletes a subfolder from the parent folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f074-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f074-108">Syntax</span></span>


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="5f074-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f074-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f074-110">*nombrecarpeta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5f074-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f074-111">Nombre de la subcarpeta que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="5f074-111">The name of the subfolder to be removed.</span></span> <span data-ttu-id="5f074-112">La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \) .</span><span class="sxs-lookup"><span data-stu-id="5f074-112">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="5f074-113">Este parámetro puede ser una ruta de acceso relativa a la carpeta que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="5f074-113">This parameter can be a relative path to the folder you want to delete.</span></span> <span data-ttu-id="5f074-114">Un ejemplo de una ruta de carpeta de tareas, en la carpeta de tareas raíz, es \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="5f074-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="5f074-115">No se puede usar el carácter '. ' para especificar la carpeta de tareas actual y '.. '</span><span class="sxs-lookup"><span data-stu-id="5f074-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="5f074-116">no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="5f074-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="5f074-117">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5f074-117">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f074-118">No se admite.</span><span class="sxs-lookup"><span data-stu-id="5f074-118">Not supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f074-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f074-119">Return value</span></span>

<span data-ttu-id="5f074-120">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5f074-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f074-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f074-121">Requirements</span></span>



| <span data-ttu-id="5f074-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f074-122">Requirement</span></span> | <span data-ttu-id="5f074-123">Value</span><span class="sxs-lookup"><span data-stu-id="5f074-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f074-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f074-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5f074-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5f074-125">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5f074-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f074-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5f074-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f074-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5f074-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5f074-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="5f074-129"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5f074-129"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5f074-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5f074-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f074-131"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f074-131"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f074-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f074-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f074-133">**TaskFolder**</span><span class="sxs-lookup"><span data-stu-id="5f074-133">**TaskFolder**</span></span>](taskfolder.md)
</dt> <dt>

[<span data-ttu-id="5f074-134">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="5f074-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





