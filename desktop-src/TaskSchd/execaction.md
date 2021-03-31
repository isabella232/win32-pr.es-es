---
title: Objeto ExecAction
description: Objeto de scripting que representa una acción que ejecuta una operación de línea de comandos.
ms.assetid: 51d2746d-3a90-4e8b-ac2b-d73193b3aa74
keywords:
- ejecutar acción Programador de tareas, interfaz
- Objeto ExecAction Programador de tareas
- Programador de tareas de objeto ExecAction, descrito
topic_type:
- apiref
api_name:
- ExecAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cddd1b9b44612b4ce896fb3ceb99a6deeaa5e3a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150956"
---
# <a name="execaction-object"></a><span data-ttu-id="a1993-106">Objeto ExecAction</span><span class="sxs-lookup"><span data-stu-id="a1993-106">ExecAction object</span></span>

<span data-ttu-id="a1993-107">Objeto de scripting que representa una acción que ejecuta una operación de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="a1993-107">Scripting object that represents an action that executes a command-line operation.</span></span>

## <a name="members"></a><span data-ttu-id="a1993-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a1993-108">Members</span></span>

<span data-ttu-id="a1993-109">El objeto **ExecAction** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a1993-109">The **ExecAction** object has these types of members:</span></span>

-   [<span data-ttu-id="a1993-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a1993-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1993-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a1993-111">Properties</span></span>

<span data-ttu-id="a1993-112">El objeto **ExecAction** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a1993-112">The **ExecAction** object has these properties.</span></span>



| <span data-ttu-id="a1993-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a1993-113">Property</span></span>                                                            | <span data-ttu-id="a1993-114">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="a1993-114">Access type</span></span>           | <span data-ttu-id="a1993-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1993-115">Description</span></span>                                                                                                                       |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1993-116">**Argumentos**</span><span class="sxs-lookup"><span data-stu-id="a1993-116">**Arguments**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)<br/>               | <span data-ttu-id="a1993-117">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1993-117">Read/write</span></span><br/> | <span data-ttu-id="a1993-118">Obtiene o establece los argumentos asociados a la operación de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="a1993-118">Gets or sets the arguments associated with the command-line operation.</span></span><br/>                                                 |
| [<span data-ttu-id="a1993-119">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="a1993-119">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_id)<br/>                                 | <span data-ttu-id="a1993-120">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1993-120">Read/write</span></span><br/> | <span data-ttu-id="a1993-121">Heredado del objeto de [**acción**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="a1993-121">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="a1993-122">Obtiene o establece el identificador de la acción.</span><span class="sxs-lookup"><span data-stu-id="a1993-122">Gets or sets the identifier of the action.</span></span><br/>                         |
| [<span data-ttu-id="a1993-123">**Ruta**</span><span class="sxs-lookup"><span data-stu-id="a1993-123">**Path**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)<br/>                         | <span data-ttu-id="a1993-124">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1993-124">Read/write</span></span><br/> | <span data-ttu-id="a1993-125">Obtiene o establece la ruta de acceso a un archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="a1993-125">Gets or sets the path to an executable file.</span></span><br/>                                                                           |
| [<span data-ttu-id="a1993-126">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a1993-126">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_type)<br/>                             | <span data-ttu-id="a1993-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a1993-127">Read-only</span></span><br/>  | <span data-ttu-id="a1993-128">Heredado del objeto de [**acción**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="a1993-128">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="a1993-129">Obtiene el tipo de la acción.</span><span class="sxs-lookup"><span data-stu-id="a1993-129">Gets the type of the action.</span></span><br/>                                       |
| [<span data-ttu-id="a1993-130">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="a1993-130">**WorkingDirectory**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory)<br/> | <span data-ttu-id="a1993-131">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1993-131">Read/write</span></span><br/> | <span data-ttu-id="a1993-132">Obtiene o establece el directorio que contiene el archivo ejecutable o los archivos utilizados por el archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="a1993-132">Gets or sets the directory that contains either the executable file or the files that are used by the executable file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a1993-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1993-133">Remarks</span></span>

<span data-ttu-id="a1993-134">Si se usan variables de entorno en las propiedades [**path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path), [**arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)o [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) , los valores de las variables de entorno se almacenan en caché y se usan cuando se inicia el Taskeng.exe (el motor de tareas).</span><span class="sxs-lookup"><span data-stu-id="a1993-134">If environment variables are used in the [**Path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path), [**Arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments), or [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) properties, then the values of the environment variables are cached and used when the Taskeng.exe (the task engine) is launched.</span></span> <span data-ttu-id="a1993-135">El motor de tareas no utilizará los cambios en las variables de entorno que se producen después de iniciar el motor de tareas.</span><span class="sxs-lookup"><span data-stu-id="a1993-135">Changes to the environment variables that occur after the task engine is launched will not be used by the task engine.</span></span>

<span data-ttu-id="a1993-136">Esta acción realiza una operación de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="a1993-136">This action performs a command-line operation.</span></span> <span data-ttu-id="a1993-137">Por ejemplo, la acción podría ejecutar un script o iniciar un ejecutable.</span><span class="sxs-lookup"><span data-stu-id="a1993-137">For example, the action could run a script or launch an executable.</span></span>

<span data-ttu-id="a1993-138">Al leer o escribir XML, se especifica una acción de ejecución en el elemento [**exec**](taskschedulerschema-exec-actiongroup-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="a1993-138">When reading or writing XML, an execution action is specified in the [**Exec**](taskschedulerschema-exec-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="a1993-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a1993-139">Examples</span></span>

<span data-ttu-id="a1993-140">Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="a1993-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1993-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1993-141">Requirements</span></span>



| <span data-ttu-id="a1993-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1993-142">Requirement</span></span> | <span data-ttu-id="a1993-143">Value</span><span class="sxs-lookup"><span data-stu-id="a1993-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1993-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1993-144">Minimum supported client</span></span><br/> | <span data-ttu-id="a1993-145">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a1993-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a1993-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1993-146">Minimum supported server</span></span><br/> | <span data-ttu-id="a1993-147">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a1993-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a1993-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a1993-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="a1993-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a1993-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a1993-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a1993-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1993-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1993-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





