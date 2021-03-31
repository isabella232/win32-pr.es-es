---
title: Propiedad ShowMessageAction. MessageBody
description: En el caso de scripting, obtiene o establece el texto del mensaje que se muestra en el cuerpo del cuadro de mensaje.
ms.assetid: 7166e379-95f0-43f1-93a0-6a3d706dd627
keywords:
- Programador de tareas de la propiedad MessageBody
- Programador de tareas de la propiedad MessageBody, objeto ShowMessageAction
- Programador de tareas de objeto ShowMessageAction, propiedad MessageBody
topic_type:
- apiref
api_name:
- ShowMessageAction.MessageBody
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1604367a8daad1ae1b5f44c6021d22bf1aa7c5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905088"
---
# <a name="showmessageactionmessagebody-property"></a><span data-ttu-id="75a58-106">Propiedad ShowMessageAction. MessageBody</span><span class="sxs-lookup"><span data-stu-id="75a58-106">ShowMessageAction.MessageBody property</span></span>

<span data-ttu-id="75a58-107">\[Este objeto ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="75a58-107">\[This object is no longer supported.</span></span> <span data-ttu-id="75a58-108">Puede usar IExecAction con la [**función MsgBox**](/previous-versions/sfw6660x(v=vs.80)) de scripting de Windows para mostrar un mensaje en la sesión de usuario.\]</span><span class="sxs-lookup"><span data-stu-id="75a58-108">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.\]</span></span>

<span data-ttu-id="75a58-109">En el caso de scripting, obtiene o establece el texto del mensaje que se muestra en el cuerpo del cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="75a58-109">For scripting, gets or sets the message text that is displayed in the body of the message box.</span></span>

## <a name="syntax"></a><span data-ttu-id="75a58-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75a58-110">Syntax</span></span>


```VB
ShowMessageAction.MessageBody As String
```



## <a name="property-value"></a><span data-ttu-id="75a58-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="75a58-111">Property value</span></span>

<span data-ttu-id="75a58-112">Texto del mensaje que se muestra en el cuerpo del cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="75a58-112">The message text that is displayed in the body of the message box.</span></span>

## <a name="remarks"></a><span data-ttu-id="75a58-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75a58-113">Remarks</span></span>

<span data-ttu-id="75a58-114">Las cadenas con parámetros se pueden usar en el texto del mensaje del cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="75a58-114">Parameterized strings can be used in the message text of the message box.</span></span> <span data-ttu-id="75a58-115">Para obtener más información, vea la sección ejemplos en [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md).</span><span class="sxs-lookup"><span data-stu-id="75a58-115">For more information, see the Examples section in [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).</span></span>

<span data-ttu-id="75a58-116">Al establecer este valor de propiedad, el valor puede ser texto que se recupera de un archivo resource. dll.</span><span class="sxs-lookup"><span data-stu-id="75a58-116">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="75a58-117">Una cadena especializada se usa para hacer referencia al texto del archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="75a58-117">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="75a58-118">El formato de la cadena es $ (@ \[ dll \] , \[ resourceId \] ), donde \[ dll \] es la ruta de acceso al archivo. dll que contiene el recurso y \[ resourceId \] es el identificador del texto del recurso.</span><span class="sxs-lookup"><span data-stu-id="75a58-118">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="75a58-119">Por ejemplo, al establecer este valor de propiedad en $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101), la propiedad se establecerá en el valor del texto del recurso con un identificador igual a-101 en el archivo% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="75a58-119">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="75a58-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75a58-120">Requirements</span></span>



| <span data-ttu-id="75a58-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="75a58-121">Requirement</span></span> | <span data-ttu-id="75a58-122">Value</span><span class="sxs-lookup"><span data-stu-id="75a58-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75a58-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75a58-123">Minimum supported client</span></span><br/> | <span data-ttu-id="75a58-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="75a58-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="75a58-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75a58-125">Minimum supported server</span></span><br/> | <span data-ttu-id="75a58-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="75a58-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="75a58-127">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="75a58-127">End of client support</span></span><br/>    | <span data-ttu-id="75a58-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="75a58-128">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="75a58-129">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="75a58-129">End of server support</span></span><br/>    | <span data-ttu-id="75a58-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="75a58-130">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="75a58-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="75a58-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="75a58-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="75a58-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="75a58-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75a58-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75a58-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75a58-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75a58-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="75a58-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75a58-136">**ShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="75a58-136">**ShowMessageAction**</span></span>](showmessageaction.md)
</dt> </dl>

 

