---
title: Propiedad principal. DisplayName
description: En el caso de scripting, obtiene o establece el nombre de la entidad de seguridad.
ms.assetid: 73caf263-f597-4bea-ae89-32f9919d7a70
keywords:
- Propiedad DisplayName Programador de tareas
- Propiedad DisplayName Programador de tareas, objeto principal
- Objeto de entidad de seguridad Programador de tareas, DisplayName (propiedad)
topic_type:
- apiref
api_name:
- Principal.DisplayName
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31a76ec9473bccb20ec484259ab8adfe26ad6441
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802557"
---
# <a name="principaldisplayname-property"></a><span data-ttu-id="0423d-106">Propiedad principal. DisplayName</span><span class="sxs-lookup"><span data-stu-id="0423d-106">Principal.DisplayName property</span></span>

<span data-ttu-id="0423d-107">En el caso de scripting, obtiene o establece el nombre de la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="0423d-107">For scripting, gets or sets the name of the principal..</span></span>

## <a name="syntax"></a><span data-ttu-id="0423d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0423d-108">Syntax</span></span>


```VB
Principal.DisplayName As String
```



## <a name="property-value"></a><span data-ttu-id="0423d-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0423d-109">Property value</span></span>

<span data-ttu-id="0423d-110">Nombre de la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="0423d-110">The name of the principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="0423d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0423d-111">Remarks</span></span>

<span data-ttu-id="0423d-112">Al leer o escribir XML para una tarea, el nombre para mostrar de una entidad de seguridad se especifica en el elemento [**displayName**](taskschedulerschema-displayname-principaltype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="0423d-112">When reading or writing XML for a task, the display name for a principal is specified in the [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="0423d-113">Al establecer este valor de propiedad, el valor puede ser texto que se recupera de un archivo resource. dll.</span><span class="sxs-lookup"><span data-stu-id="0423d-113">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="0423d-114">Una cadena especializada se usa para hacer referencia al texto del archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0423d-114">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="0423d-115">El formato de la cadena es $ (@ \[ dll \] , \[ resourceId \] ), donde \[ dll \] es la ruta de acceso al archivo. dll que contiene el recurso y \[ resourceId \] es el identificador del texto del recurso.</span><span class="sxs-lookup"><span data-stu-id="0423d-115">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="0423d-116">Por ejemplo, si se establece el valor de esta propiedad en $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101), la propiedad se establecerá en el valor del texto del recurso con un identificador igual a-101 en el archivo% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="0423d-116">For example, setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="0423d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0423d-117">Requirements</span></span>



| <span data-ttu-id="0423d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0423d-118">Requirement</span></span> | <span data-ttu-id="0423d-119">Value</span><span class="sxs-lookup"><span data-stu-id="0423d-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0423d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0423d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0423d-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0423d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0423d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0423d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0423d-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0423d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0423d-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0423d-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="0423d-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0423d-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0423d-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0423d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0423d-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0423d-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0423d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0423d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0423d-129">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="0423d-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="0423d-130">**Principal**</span><span class="sxs-lookup"><span data-stu-id="0423d-130">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 





