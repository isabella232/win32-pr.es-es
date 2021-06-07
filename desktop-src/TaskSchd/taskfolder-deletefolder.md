---
title: Método TaskFolder.DeleteFolder
description: Para el scripting, elimina una subcarpeta de la carpeta primaria.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- Método DeleteFolder Programador de tareas
- Método DeleteFolder Programador de tareas , objeto TaskFolder
- TaskFolder object Programador de tareas , DeleteFolder (método)
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
ms.openlocfilehash: 31080f017329cde376b646befd4b7e12ba02926b
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387044"
---
# <a name="taskfolderdeletefolder-method"></a><span data-ttu-id="6f409-106">Método TaskFolder.DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="6f409-106">TaskFolder.DeleteFolder method</span></span>

<span data-ttu-id="6f409-107">Para el scripting, elimina una subcarpeta de la carpeta primaria.</span><span class="sxs-lookup"><span data-stu-id="6f409-107">For scripting, deletes a subfolder from the parent folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f409-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f409-108">Syntax</span></span>


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="6f409-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f409-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f409-110">*folderName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="6f409-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f409-111">Nombre de la subcarpeta que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="6f409-111">The name of the subfolder to be removed.</span></span> <span data-ttu-id="6f409-112">La carpeta de tareas raíz se especifica con una barra diagonal inversa ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="6f409-112">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="6f409-113">Este parámetro puede ser una ruta de acceso relativa a la carpeta que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="6f409-113">This parameter can be a relative path to the folder you want to delete.</span></span> <span data-ttu-id="6f409-114">Un ejemplo de una ruta de acceso de carpeta de tareas, en la carpeta de tareas raíz, \\ es MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="6f409-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="6f409-115">No se puede usar el carácter '.' para especificar la carpeta de tareas actual y '..'.</span><span class="sxs-lookup"><span data-stu-id="6f409-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="6f409-116">no se pueden usar caracteres para especificar la carpeta de tareas primaria en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="6f409-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="6f409-117">*flags* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="6f409-117">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f409-118">No compatible.</span><span class="sxs-lookup"><span data-stu-id="6f409-118">Not supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f409-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f409-119">Return value</span></span>

<span data-ttu-id="6f409-120">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6f409-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f409-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f409-121">Requirements</span></span>



| <span data-ttu-id="6f409-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f409-122">Requirement</span></span> | <span data-ttu-id="6f409-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6f409-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f409-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f409-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6f409-125">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="6f409-125">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6f409-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f409-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6f409-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f409-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6f409-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6f409-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="6f409-129"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6f409-129"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6f409-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f409-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f409-131"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f409-131"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f409-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f409-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f409-133">**TaskFolder**</span><span class="sxs-lookup"><span data-stu-id="6f409-133">**TaskFolder**</span></span>](taskfolder.md)
</dt> <dt>

[<span data-ttu-id="6f409-134">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="6f409-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





