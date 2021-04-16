---
title: Elemento LogonType (principalType)
description: Especifica el método de inicio de sesión de seguridad necesario para ejecutar las tareas asociadas a la entidad de seguridad.
ms.assetid: e36a1755-96f3-45dc-8779-8bd0cfde886c
keywords:
- Programador de tareas del elemento LogonType
topic_type:
- apiref
api_name:
- LogonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a382225f526f18731b8b9f0541e617cb31dfb4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685908"
---
# <a name="logontype-principaltype-element"></a><span data-ttu-id="3cfbf-104">Elemento LogonType (principalType)</span><span class="sxs-lookup"><span data-stu-id="3cfbf-104">LogonType (principalType) Element</span></span>

<span data-ttu-id="3cfbf-105">Especifica el método de inicio de sesión de seguridad necesario para ejecutar las tareas asociadas a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="3cfbf-105">Specifies the security logon method required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="LogonType"
    type="logonType"
 />
```

<span data-ttu-id="3cfbf-106">El elemento **LogonType** se define mediante el tipo complejo de [**principalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3cfbf-106">The **LogonType** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3cfbf-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="3cfbf-107">Parent element</span></span>



| <span data-ttu-id="3cfbf-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="3cfbf-108">Element</span></span>                                                                  | <span data-ttu-id="3cfbf-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="3cfbf-109">Derived from</span></span>                                                           | <span data-ttu-id="3cfbf-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3cfbf-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="3cfbf-111">**Principal**</span><span class="sxs-lookup"><span data-stu-id="3cfbf-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="3cfbf-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="3cfbf-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="3cfbf-113">Especifica las credenciales de seguridad para una entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="3cfbf-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3cfbf-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3cfbf-114">Remarks</span></span>

<span data-ttu-id="3cfbf-115">Los elementos **LogonType** y [**userid**](taskschedulerschema-userid-principaltype-element.md) se usan juntos para definir el usuario necesario para ejecutar las tareas que usan esta entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="3cfbf-115">The **LogonType** element and the [**UserId**](taskschedulerschema-userid-principaltype-element.md) element are used together to define the user required to run those tasks that use this principal.</span></span>

<span data-ttu-id="3cfbf-116">Para el desarrollo de scripting, el tipo de inicio de sesión de la entidad de seguridad se especifica mediante la propiedad [**principal. LogonType**](principal-logontype.md) .</span><span class="sxs-lookup"><span data-stu-id="3cfbf-116">For scripting development, the logon type for the principal is specified by the [**Principal.LogonType**](principal-logontype.md) property.</span></span>

<span data-ttu-id="3cfbf-117">En el desarrollo de C++, el tipo de inicio de sesión de la entidad de seguridad se especifica mediante la propiedad [**IPrincipal:: LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) .</span><span class="sxs-lookup"><span data-stu-id="3cfbf-117">For C++ development, the logon type for the principal is specified by the [**IPrincipal::LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) property.</span></span>

<span data-ttu-id="3cfbf-118">Este elemento (definido por el tipo simple [**logonType**](taskschedulerschema-logontype-simpletype.md) ) debe tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3cfbf-118">This element (defined by the [**logonType**](taskschedulerschema-logontype-simpletype.md) simple type) must have one of the following values.</span></span>

-   <span data-ttu-id="3cfbf-119">S4U: el usuario debe iniciar sesión con un inicio de sesión de servicio para el usuario (S4U).</span><span class="sxs-lookup"><span data-stu-id="3cfbf-119">S4U: User must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="3cfbf-120">Cuando se usa un inicio de sesión de S4U, el sistema no almacena ninguna contraseña y no se tiene acceso a la red ni a los archivos cifrados.</span><span class="sxs-lookup"><span data-stu-id="3cfbf-120">When an S4U logon is used, no password is stored by the system and there is no access to the network or encrypted files.</span></span>
-   <span data-ttu-id="3cfbf-121">Contraseña: el usuario debe iniciar sesión con una contraseña.</span><span class="sxs-lookup"><span data-stu-id="3cfbf-121">Password: User must log on using a password.</span></span>
-   <span data-ttu-id="3cfbf-122">InteractiveToken: el usuario ya debe haber iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="3cfbf-122">InteractiveToken: User must already be logged on.</span></span> <span data-ttu-id="3cfbf-123">La tarea se ejecutará solo en una sesión interactiva existente.</span><span class="sxs-lookup"><span data-stu-id="3cfbf-123">The task will be run only in an existing interactive session.</span></span>

<span data-ttu-id="3cfbf-124">En el caso de una tarea que contenga una acción de cuadro de mensaje, se mostrará el cuadro de mensaje si la tarea está activada y la tarea tiene un tipo de inicio de sesión interactivo.</span><span class="sxs-lookup"><span data-stu-id="3cfbf-124">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="3cfbf-125">Para establecer que el tipo de inicio de sesión de tarea sea interactivo, especifique **InteractiveToken** en el **<LogonType>** elemento de la entidad de seguridad de la tarea.</span><span class="sxs-lookup"><span data-stu-id="3cfbf-125">To set the task logon type to be interactive, specify **InteractiveToken** in the **<LogonType>** element of the task principal.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cfbf-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cfbf-126">Requirements</span></span>



| <span data-ttu-id="3cfbf-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cfbf-127">Requirement</span></span> | <span data-ttu-id="3cfbf-128">Value</span><span class="sxs-lookup"><span data-stu-id="3cfbf-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3cfbf-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3cfbf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3cfbf-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3cfbf-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3cfbf-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3cfbf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3cfbf-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3cfbf-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3cfbf-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="3cfbf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cfbf-134">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="3cfbf-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





