---
title: ShowMessageAction. title (propiedad)
description: En el caso de scripting, obtiene o establece el título del cuadro de mensaje.
ms.assetid: f61177fc-287c-4da9-9bdc-88aaa6868204
keywords:
- Propiedad título Programador de tareas
- Propiedad title Programador de tareas, objeto ShowMessageAction
- Programador de tareas de objeto ShowMessageAction, propiedad title
topic_type:
- apiref
api_name:
- ShowMessageAction.Title
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2e552bb51653248e0a70ccfc0edea907749900e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801603"
---
# <a name="showmessageactiontitle-property"></a><span data-ttu-id="8442a-106">ShowMessageAction. title (propiedad)</span><span class="sxs-lookup"><span data-stu-id="8442a-106">ShowMessageAction.Title property</span></span>

<span data-ttu-id="8442a-107">\[Este objeto ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="8442a-107">\[This object is no longer supported.</span></span> <span data-ttu-id="8442a-108">Puede usar IExecAction con la [**función MsgBox**](/previous-versions/sfw6660x(v=vs.80)) de scripting de Windows para mostrar un mensaje en la sesión de usuario.\]</span><span class="sxs-lookup"><span data-stu-id="8442a-108">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.\]</span></span>

<span data-ttu-id="8442a-109">En el caso de scripting, obtiene o establece el título del cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="8442a-109">For scripting, gets or sets the title of the message box.</span></span>

## <a name="syntax"></a><span data-ttu-id="8442a-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8442a-110">Syntax</span></span>


```VB
ShowMessageAction.Title As String
```



## <a name="property-value"></a><span data-ttu-id="8442a-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8442a-111">Property value</span></span>

<span data-ttu-id="8442a-112">Título del cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="8442a-112">The title of the message box.</span></span>

## <a name="remarks"></a><span data-ttu-id="8442a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8442a-113">Remarks</span></span>

<span data-ttu-id="8442a-114">Las cadenas con parámetros se pueden usar en el texto del título del cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="8442a-114">Parameterized strings can be used in the title text of the message box.</span></span> <span data-ttu-id="8442a-115">Para obtener más información, vea la sección ejemplos en [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md).</span><span class="sxs-lookup"><span data-stu-id="8442a-115">For more information, see the Examples section in [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).</span></span>

<span data-ttu-id="8442a-116">Al establecer este valor de propiedad, el valor puede ser texto que se recupera de un archivo resource. dll.</span><span class="sxs-lookup"><span data-stu-id="8442a-116">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="8442a-117">Una cadena especializada se usa para hacer referencia al texto del archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8442a-117">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="8442a-118">El formato de la cadena es $ (@ \[ dll \] , \[ resourceId \] ), donde \[ dll \] es la ruta de acceso al archivo. dll que contiene el recurso y \[ resourceId \] es el identificador del texto del recurso.</span><span class="sxs-lookup"><span data-stu-id="8442a-118">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="8442a-119">Por ejemplo, al establecer este valor de propiedad en $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101), la propiedad se establecerá en el valor del texto del recurso con un identificador igual a-101 en el archivo% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="8442a-119">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="8442a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8442a-120">Requirements</span></span>



| <span data-ttu-id="8442a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8442a-121">Requirement</span></span> | <span data-ttu-id="8442a-122">Value</span><span class="sxs-lookup"><span data-stu-id="8442a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8442a-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8442a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8442a-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8442a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8442a-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8442a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8442a-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8442a-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8442a-127">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="8442a-127">End of client support</span></span><br/>    | <span data-ttu-id="8442a-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8442a-128">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="8442a-129">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="8442a-129">End of server support</span></span><br/>    | <span data-ttu-id="8442a-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8442a-130">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="8442a-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8442a-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="8442a-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8442a-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8442a-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8442a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8442a-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8442a-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8442a-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="8442a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8442a-136">**ShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="8442a-136">**ShowMessageAction**</span></span>](showmessageaction.md)
</dt> </dl>

 

