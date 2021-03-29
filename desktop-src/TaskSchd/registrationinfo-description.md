---
title: RegistrationInfo. Description (propiedad)
description: En el caso de scripting, obtiene o establece la descripción de la tarea.
ms.assetid: bb85fa09-155c-452b-bf6e-28ac4f60cc42
keywords:
- Propiedad Description Programador de tareas
- Propiedad Description Programador de tareas, objeto RegistrationInfo
- Programador de tareas objeto RegistrationInfo, propiedad Description
topic_type:
- apiref
api_name:
- RegistrationInfo.Description
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9c79b60fe6a96493c52011e5bd731679b3fee1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421895"
---
# <a name="registrationinfodescription-property"></a><span data-ttu-id="ca293-106">RegistrationInfo. Description (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ca293-106">RegistrationInfo.Description property</span></span>

<span data-ttu-id="ca293-107">En el caso de scripting, obtiene o establece la descripción de la tarea.</span><span class="sxs-lookup"><span data-stu-id="ca293-107">For scripting, gets or sets the description of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca293-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca293-108">Syntax</span></span>


```VB
RegistrationInfo.Description As String
```



## <a name="property-value"></a><span data-ttu-id="ca293-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ca293-109">Property value</span></span>

<span data-ttu-id="ca293-110">Descripción de la tarea.</span><span class="sxs-lookup"><span data-stu-id="ca293-110">The description of the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca293-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca293-111">Remarks</span></span>

<span data-ttu-id="ca293-112">Al leer o escribir XML para una tarea, la descripción de la tarea se especifica mediante el elemento [**Description**](taskschedulerschema-description-registrationinfotype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="ca293-112">When reading or writing XML for a task, the description of the task is specified using the [**Description**](taskschedulerschema-description-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="ca293-113">Al establecer este valor de propiedad, el valor puede ser texto que se recupera de un archivo resource. dll.</span><span class="sxs-lookup"><span data-stu-id="ca293-113">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="ca293-114">Una cadena especializada se usa para hacer referencia al texto del archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca293-114">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="ca293-115">El formato de la cadena es $ (@ \[ dll \] , \[ resourceId \] ), donde \[ dll \] es la ruta de acceso al archivo. dll que contiene el recurso y \[ resourceId \] es el identificador del texto del recurso.</span><span class="sxs-lookup"><span data-stu-id="ca293-115">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="ca293-116">Por ejemplo, al establecer este valor de propiedad en $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101), la propiedad se establecerá en el valor del texto del recurso con un identificador igual a-101 en el archivo% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="ca293-116">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca293-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca293-117">Requirements</span></span>



| <span data-ttu-id="ca293-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca293-118">Requirement</span></span> | <span data-ttu-id="ca293-119">Value</span><span class="sxs-lookup"><span data-stu-id="ca293-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca293-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca293-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ca293-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ca293-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ca293-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca293-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ca293-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ca293-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ca293-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ca293-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="ca293-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ca293-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ca293-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ca293-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca293-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca293-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca293-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca293-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca293-129">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="ca293-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





