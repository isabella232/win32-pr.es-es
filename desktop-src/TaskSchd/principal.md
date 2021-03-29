---
title: Objeto principal
description: Objeto de scripting que proporciona las credenciales de seguridad para una entidad de seguridad.
ms.assetid: 9589f3c2-2709-4e71-8986-2347be049f6b
keywords:
- Programador de tareas de objeto principal
- Programador de tareas de objeto principal, descrito
topic_type:
- apiref
api_name:
- Principal
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6dc9ff69973fb340bf3b140462c4012499680ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905120"
---
# <a name="principal-object"></a><span data-ttu-id="9e1bf-105">Objeto principal</span><span class="sxs-lookup"><span data-stu-id="9e1bf-105">Principal object</span></span>

<span data-ttu-id="9e1bf-106">Objeto de scripting que proporciona las credenciales de seguridad para una entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9e1bf-106">Scripting object that provides the security credentials for a principal.</span></span> <span data-ttu-id="9e1bf-107">Estas credenciales de seguridad definen el contexto de seguridad para las tareas que están asociadas a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9e1bf-107">These security credentials define the security context for the tasks that are associated with the principal.</span></span>

## <a name="members"></a><span data-ttu-id="9e1bf-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9e1bf-108">Members</span></span>

<span data-ttu-id="9e1bf-109">El objeto **principal** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9e1bf-109">The **Principal** object has these types of members:</span></span>

-   [<span data-ttu-id="9e1bf-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9e1bf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e1bf-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9e1bf-111">Properties</span></span>

<span data-ttu-id="9e1bf-112">El objeto de **entidad** de seguridad tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9e1bf-112">The **Principal** object has these properties.</span></span>



| <span data-ttu-id="9e1bf-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9e1bf-113">Property</span></span>                                                | <span data-ttu-id="9e1bf-114">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="9e1bf-114">Access type</span></span>           | <span data-ttu-id="9e1bf-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e1bf-115">Description</span></span>                                                                                                                                                  |
|:--------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e1bf-116">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="9e1bf-116">**DisplayName**</span></span>](principal-displayname.md)<br/> | <span data-ttu-id="9e1bf-117">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9e1bf-117">Read/write</span></span><br/> | <span data-ttu-id="9e1bf-118">Obtiene o establece el nombre de la entidad de seguridad que se muestra en la interfaz de usuario de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="9e1bf-118">Gets or sets the name of the principal that is displayed in the Task Scheduler UI.</span></span><br/>                                                                |
| [<span data-ttu-id="9e1bf-119">**GroupId**</span><span class="sxs-lookup"><span data-stu-id="9e1bf-119">**GroupId**</span></span>](principal-groupid.md)<br/>         | <span data-ttu-id="9e1bf-120">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9e1bf-120">Read/write</span></span><br/> | <span data-ttu-id="9e1bf-121">Obtiene o establece el identificador del grupo de usuarios necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9e1bf-121">Gets or sets the identifier of the user group that is required to run the tasks that are associated with the principal.</span></span><br/>                           |
| [<span data-ttu-id="9e1bf-122">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="9e1bf-122">**Id**</span></span>](principal-id.md)<br/>                   | <span data-ttu-id="9e1bf-123">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9e1bf-123">Read/write</span></span><br/> | <span data-ttu-id="9e1bf-124">Obtiene o establece el identificador de la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9e1bf-124">Gets or sets the identifier of the principal.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="9e1bf-125">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="9e1bf-125">**LogonType**</span></span>](principal-logontype.md)<br/>     | <span data-ttu-id="9e1bf-126">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9e1bf-126">Read/write</span></span><br/> | <span data-ttu-id="9e1bf-127">Obtiene o establece el método de inicio de sesión de seguridad necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9e1bf-127">Gets or sets the security logon method that is required to run the tasks that are associated with the principal.</span></span><br/>                                  |
| [<span data-ttu-id="9e1bf-128">**Nivel**</span><span class="sxs-lookup"><span data-stu-id="9e1bf-128">**RunLevel**</span></span>](principal-runlevel.md)<br/>       | <span data-ttu-id="9e1bf-129">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9e1bf-129">Read/write</span></span><br/> | <span data-ttu-id="9e1bf-130">Obtiene o establece el identificador que se usa para especificar el nivel de privilegios necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9e1bf-130">Gets or sets the identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span><br/> |
| [<span data-ttu-id="9e1bf-131">**Deberían**</span><span class="sxs-lookup"><span data-stu-id="9e1bf-131">**UserId**</span></span>](principal-userid.md)<br/>           | <span data-ttu-id="9e1bf-132">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9e1bf-132">Read/write</span></span><br/> | <span data-ttu-id="9e1bf-133">Obtiene o establece el identificador de usuario necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9e1bf-133">Gets or sets the user identifier that is required to run the tasks that are associated with the principal.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="9e1bf-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e1bf-134">Remarks</span></span>

<span data-ttu-id="9e1bf-135">Al especificar una cuenta, no olvide usar correctamente la doble barra diagonal inversa en el código para especificar el dominio y el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="9e1bf-135">When specifying an account, remember to properly use the double backslash in code to specify the domain and user name.</span></span> <span data-ttu-id="9e1bf-136">Por ejemplo, use \\ \\ el nombre de usuario de dominio para especificar un valor para la propiedad [**userid**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) .</span><span class="sxs-lookup"><span data-stu-id="9e1bf-136">For example, use DOMAIN\\\\UserName to specify a value for the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) property.</span></span>

<span data-ttu-id="9e1bf-137">Al leer o escribir XML para una tarea, las credenciales de seguridad de una entidad de seguridad se especifican en el elemento [**principal**](taskschedulerschema-principal-principaltype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="9e1bf-137">When reading or writing XML for a task, the security credentials for a principal are specified in the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="9e1bf-138">Si una tarea se registra con la herramienta de línea de comandos at.exe y este objeto se usa para recuperar información sobre la tarea, la propiedad [**LogonType**](principal-logontype.md) devolverá 0, la propiedad [**nivel**](principal-runlevel.md) devolverá 0 y la propiedad [**userid**](principal-userid.md) no devolverá nada.</span><span class="sxs-lookup"><span data-stu-id="9e1bf-138">If a task is registered using the at.exe command line tool, and this object is used to retrieve information about the task, then the [**LogonType**](principal-logontype.md) property will return 0, the [**RunLevel**](principal-runlevel.md) property will return 0, and the [**UserId**](principal-userid.md) property will return Nothing.</span></span>

## <a name="examples"></a><span data-ttu-id="9e1bf-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9e1bf-139">Examples</span></span>

<span data-ttu-id="9e1bf-140">Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="9e1bf-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e1bf-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e1bf-141">Requirements</span></span>



| <span data-ttu-id="9e1bf-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e1bf-142">Requirement</span></span> | <span data-ttu-id="9e1bf-143">Value</span><span class="sxs-lookup"><span data-stu-id="9e1bf-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e1bf-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e1bf-144">Minimum supported client</span></span><br/> | <span data-ttu-id="9e1bf-145">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9e1bf-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9e1bf-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e1bf-146">Minimum supported server</span></span><br/> | <span data-ttu-id="9e1bf-147">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e1bf-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9e1bf-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9e1bf-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="9e1bf-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9e1bf-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9e1bf-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9e1bf-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e1bf-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e1bf-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





