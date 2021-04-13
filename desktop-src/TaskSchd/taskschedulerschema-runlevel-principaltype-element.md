---
title: Elemento nivel (runLevelType)
description: Contiene un valor que especifica el nivel de contexto de seguridad para ejecutar la tarea.
ms.assetid: dc113ffa-8ac9-4dcd-a106-45295da42f46
keywords:
- Programador de tareas del elemento nivel
topic_type:
- apiref
api_name:
- RunLevel
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d374f5b9ad388f3ad0a626e1b99ecae96eeef1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359859"
---
# <a name="runlevel-runleveltype-element"></a><span data-ttu-id="76599-104">Elemento nivel (runLevelType)</span><span class="sxs-lookup"><span data-stu-id="76599-104">RunLevel (runLevelType) Element</span></span>

<span data-ttu-id="76599-105">Contiene un valor que especifica el nivel de contexto de seguridad para ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="76599-105">Contains a value that specifies the security context level for running the task.</span></span> <span data-ttu-id="76599-106">Puede especificar que se ejecute una tarea con privilegios mínimos o privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="76599-106">You can specify to run a task using least privileges or elevated privileges.</span></span> <span data-ttu-id="76599-107">Un valor de 0 especifica que se ejecute la tarea con los privilegios más bajos y un valor de 1 especifica que se ejecute la tarea con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="76599-107">A value of 0 specifies to run the task with lowest privileges, and a value of 1 specifies to run the task with elevated privileges.</span></span>

``` syntax
<xs:element name="RunLevel"
    type="runLevelType"
 />
```

<span data-ttu-id="76599-108">El elemento **nivel** se define mediante el tipo simple [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md) .</span><span class="sxs-lookup"><span data-stu-id="76599-108">The **RunLevel** element is defined by the [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md) simple type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="76599-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="76599-109">Parent element</span></span>



| <span data-ttu-id="76599-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="76599-110">Element</span></span>                                                                                  | <span data-ttu-id="76599-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="76599-111">Derived from</span></span>                                                           | <span data-ttu-id="76599-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="76599-112">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76599-113">**Entidad de seguridad (principalType)**</span><span class="sxs-lookup"><span data-stu-id="76599-113">**Principal (principalType)**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="76599-114">**principalType**</span><span class="sxs-lookup"><span data-stu-id="76599-114">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="76599-115">Especifica las credenciales de seguridad para una entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="76599-115">Specifies the security credentials for a principal.</span></span> <span data-ttu-id="76599-116">Estas credenciales definen el contexto de seguridad en el que se ejecuta una tarea.</span><span class="sxs-lookup"><span data-stu-id="76599-116">These credentials define the security context that a task runs under.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="76599-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76599-117">Remarks</span></span>

<span data-ttu-id="76599-118">Para el desarrollo de C++, consulte la [**propiedad nivel de IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).</span><span class="sxs-lookup"><span data-stu-id="76599-118">For C++ development, see [**RunLevel Property of IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).</span></span>

<span data-ttu-id="76599-119">Para el desarrollo de scripts, consulte [**principal. nivel**](principal-runlevel.md).</span><span class="sxs-lookup"><span data-stu-id="76599-119">For script development, see [**Principal.RunLevel**](principal-runlevel.md).</span></span>

<span data-ttu-id="76599-120">Si una tarea se registra mediante la **cuenta de \\ Administrador de Builtin** o las cuentas [LocalSystem](/windows/desktop/Services/localsystem-account) o [LocalService](/windows/desktop/Services/localservice-account) , se omite la propiedad [**nivel**](principal-runlevel.md) .</span><span class="sxs-lookup"><span data-stu-id="76599-120">If a task is registered using the **Builtin\\Administrator** account or the [LocalSystem](/windows/desktop/Services/localsystem-account) or [LocalService](/windows/desktop/Services/localservice-account) accounts, the [**RunLevel**](principal-runlevel.md) property is ignored.</span></span> <span data-ttu-id="76599-121">El valor del atributo también se omitirá si el [control de cuentas de usuario](/windows/desktop/SecAuthZ/user-account-control) (UAC) está desactivado.</span><span class="sxs-lookup"><span data-stu-id="76599-121">The attribute value will also be ignored if [User Account Control](/windows/desktop/SecAuthZ/user-account-control) (UAC) is turned off.</span></span>

<span data-ttu-id="76599-122">Si una tarea se registra mediante el grupo de **administradores** para el contexto de seguridad de la tarea, también debe establecer la propiedad [**nivel**](principal-runlevel.md) en "HighestAvailable" para ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="76599-122">If a task is registered using the **Administrators** group for the security context of the task, then you must also set the [**RunLevel**](principal-runlevel.md) property to "HighestAvailable" to run the task.</span></span> <span data-ttu-id="76599-123">Para obtener más información, vea [contextos de seguridad para tareas](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="76599-123">For more information, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="76599-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76599-124">Requirements</span></span>



| <span data-ttu-id="76599-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="76599-125">Requirement</span></span> | <span data-ttu-id="76599-126">Value</span><span class="sxs-lookup"><span data-stu-id="76599-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="76599-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76599-127">Minimum supported client</span></span><br/> | <span data-ttu-id="76599-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="76599-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="76599-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76599-129">Minimum supported server</span></span><br/> | <span data-ttu-id="76599-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="76599-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

