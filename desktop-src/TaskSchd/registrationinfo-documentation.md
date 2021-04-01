---
title: RegistrationInfo.Docpropiedad umentation
description: En el caso de scripting, obtiene o establece cualquier documentación adicional para la tarea.
ms.assetid: 12ce9461-0cc7-49d0-8c57-7ff3ca32850a
keywords:
- Propiedad de documentación Programador de tareas
- Propiedad Documentation Programador de tareas, objeto RegistrationInfo
- Programador de tareas de objeto RegistrationInfo, propiedad Documentation
topic_type:
- apiref
api_name:
- RegistrationInfo.Documentation
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5832c78fae5c0ee9629077693db7e283369cc8af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149865"
---
# <a name="registrationinfodocumentation-property"></a><span data-ttu-id="ccc96-106">RegistrationInfo.Docpropiedad umentation</span><span class="sxs-lookup"><span data-stu-id="ccc96-106">RegistrationInfo.Documentation property</span></span>

<span data-ttu-id="ccc96-107">En el caso de scripting, obtiene o establece cualquier documentación adicional para la tarea.</span><span class="sxs-lookup"><span data-stu-id="ccc96-107">For scripting, gets or sets any additional documentation for the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccc96-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ccc96-108">Syntax</span></span>


```VB
RegistrationInfo.Documentation As String
```



## <a name="property-value"></a><span data-ttu-id="ccc96-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ccc96-109">Property value</span></span>

<span data-ttu-id="ccc96-110">Cualquier documentación adicional que esté asociada a la tarea.</span><span class="sxs-lookup"><span data-stu-id="ccc96-110">Any additional documentation that is associated with the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccc96-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ccc96-111">Remarks</span></span>

<span data-ttu-id="ccc96-112">Al leer o escribir XML para una tarea, se especifica la documentación adicional para la tarea mediante el elemento [**Documentation**](taskschedulerschema-documentation-registrationinfotype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="ccc96-112">When reading or writing XML for a task, the additional documentation for the task is specified using the [**Documentation**](taskschedulerschema-documentation-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="ccc96-113">Al establecer este valor de propiedad, el valor puede ser texto que se recupera de un archivo resource. dll.</span><span class="sxs-lookup"><span data-stu-id="ccc96-113">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="ccc96-114">Una cadena especializada se usa para hacer referencia al texto del archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ccc96-114">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="ccc96-115">El formato de la cadena es $ (@ \[ dll \] , \[ resourceId \] ), donde \[ dll \] es la ruta de acceso al archivo. dll que contiene el recurso y \[ resourceId \] es el identificador del texto del recurso.</span><span class="sxs-lookup"><span data-stu-id="ccc96-115">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="ccc96-116">Por ejemplo, al establecer este valor de propiedad en $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101), la propiedad se establecerá en el valor del texto del recurso con un identificador igual a-101 en el archivo% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="ccc96-116">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccc96-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccc96-117">Requirements</span></span>



| <span data-ttu-id="ccc96-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccc96-118">Requirement</span></span> | <span data-ttu-id="ccc96-119">Value</span><span class="sxs-lookup"><span data-stu-id="ccc96-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccc96-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccc96-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ccc96-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ccc96-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ccc96-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccc96-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ccc96-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ccc96-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ccc96-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ccc96-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="ccc96-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ccc96-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ccc96-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ccc96-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccc96-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccc96-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccc96-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ccc96-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccc96-129">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="ccc96-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





