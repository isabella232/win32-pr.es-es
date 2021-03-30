---
title: Propiedad RegistrationInfo. Source
description: Para scripting, obtiene o establece el origen desde el que se originó la tarea. Por ejemplo, una tarea se puede originar a partir de un componente, servicio, aplicación o usuario.
ms.assetid: b5bd987f-5c9f-4af0-99e2-aec92951f2be
keywords:
- Propiedad de origen Programador de tareas
- Propiedad Source Programador de tareas, objeto RegistrationInfo
- Programador de tareas de objeto RegistrationInfo, propiedad Source
topic_type:
- apiref
api_name:
- RegistrationInfo.Source
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d360a20d1f0f4736db4dd6f136a579178a65ca70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802983"
---
# <a name="registrationinfosource-property"></a><span data-ttu-id="ae456-107">Propiedad RegistrationInfo. Source</span><span class="sxs-lookup"><span data-stu-id="ae456-107">RegistrationInfo.Source property</span></span>

<span data-ttu-id="ae456-108">Para scripting, obtiene o establece el origen desde el que se originó la tarea.</span><span class="sxs-lookup"><span data-stu-id="ae456-108">For scripting, gets or sets where the task originated from.</span></span> <span data-ttu-id="ae456-109">Por ejemplo, una tarea se puede originar a partir de un componente, servicio, aplicación o usuario.</span><span class="sxs-lookup"><span data-stu-id="ae456-109">For example, a task may originate from a component, service, application, or user.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae456-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae456-110">Syntax</span></span>


```VB
RegistrationInfo.Source As String
```



## <a name="property-value"></a><span data-ttu-id="ae456-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ae456-111">Property value</span></span>

<span data-ttu-id="ae456-112">Donde se originó la tarea.</span><span class="sxs-lookup"><span data-stu-id="ae456-112">Where the task originated from.</span></span> <span data-ttu-id="ae456-113">Por ejemplo, de un componente, servicio, aplicación o usuario.</span><span class="sxs-lookup"><span data-stu-id="ae456-113">For example, from a component, service, application, or user.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae456-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae456-114">Remarks</span></span>

<span data-ttu-id="ae456-115">Al leer o escribir XML para una tarea, la información de origen de la tarea se especifica utilizando el elemento de [**origen**](taskschedulerschema-source-registrationinfotype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="ae456-115">When reading or writing XML for a task, the task source information is specified using the [**Source**](taskschedulerschema-source-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="ae456-116">Al establecer este valor de propiedad, el valor puede ser texto que se recupera de un archivo resource. dll.</span><span class="sxs-lookup"><span data-stu-id="ae456-116">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="ae456-117">Una cadena especializada se usa para hacer referencia al texto del archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ae456-117">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="ae456-118">El formato de la cadena es $ (@ \[ dll \] , \[ resourceId \] ), donde \[ dll \] es la ruta de acceso al archivo. dll que contiene el recurso y \[ resourceId \] es el identificador del texto del recurso.</span><span class="sxs-lookup"><span data-stu-id="ae456-118">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="ae456-119">Por ejemplo, al establecer este valor de propiedad en $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101), la propiedad se establecerá en el valor del texto del recurso con un identificador igual a-101 en el archivo% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="ae456-119">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae456-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae456-120">Requirements</span></span>



| <span data-ttu-id="ae456-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae456-121">Requirement</span></span> | <span data-ttu-id="ae456-122">Value</span><span class="sxs-lookup"><span data-stu-id="ae456-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae456-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae456-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ae456-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ae456-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ae456-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae456-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ae456-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ae456-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ae456-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ae456-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="ae456-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ae456-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ae456-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ae456-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae456-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae456-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae456-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae456-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae456-132">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="ae456-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





