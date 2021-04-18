---
description: Desusado. El PenInputPanel se ha reemplazado por el panel de entrada de texto (TIP). Se produce cuando el foco de entrada cambia antes de que el objeto PenInputPanel pudiera insertar la entrada del usuario en el control adjunto.
ms.assetid: a5928f78-29d6-40e8-8f87-17c188e51ba9
title: Evento PenInputPanel. InputFailed (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 198c2b466dc03357d9851d7c8a6b7f44c6bf6884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697818"
---
# <a name="peninputpanelinputfailed-event"></a><span data-ttu-id="57ee5-104">Evento PenInputPanel. InputFailed</span><span class="sxs-lookup"><span data-stu-id="57ee5-104">PenInputPanel.InputFailed event</span></span>

<span data-ttu-id="57ee5-105">En desuso.</span><span class="sxs-lookup"><span data-stu-id="57ee5-105">Deprecated.</span></span> <span data-ttu-id="57ee5-106">El [**PenInputPanel**](peninputpanel-class.md) se ha reemplazado por el [Panel de entrada de texto (TIP)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="57ee5-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="57ee5-107">Se produce cuando el foco de entrada cambia antes de que el objeto [**PenInputPanel**](peninputpanel-class.md) pudiera insertar la entrada del usuario en el control adjunto.</span><span class="sxs-lookup"><span data-stu-id="57ee5-107">Occurs when input focus changes before the [**PenInputPanel**](peninputpanel-class.md) object was able to insert user input into the attached control.</span></span>

## <a name="syntax"></a><span data-ttu-id="57ee5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57ee5-108">Syntax</span></span>


```C++
HRESULT InputFailed(
  [in] long  hWnd,
  [in] long  Key,
  [in] BSTR  Text,
  [in] short ShiftKey
);
```



## <a name="parameters"></a><span data-ttu-id="57ee5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57ee5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57ee5-110">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="57ee5-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57ee5-111">Identificador de ventana del control que invocó el objeto [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="57ee5-111">The window handle of the control that invoked the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="57ee5-112">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="57ee5-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57ee5-113">La clave virtual correspondiente a la tecla presionada.</span><span class="sxs-lookup"><span data-stu-id="57ee5-113">The virtual key corresponding to the key pressed.</span></span>

</dd> <dt>

<span data-ttu-id="57ee5-114">*Texto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="57ee5-114">*Text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57ee5-115">Cadena que se va a insertar en el control representado por el parámetro *hWnd* cuando se generó el evento **InputFailed** .</span><span class="sxs-lookup"><span data-stu-id="57ee5-115">The string that was to be inserted into the control represented by the *hWnd* parameter when the **InputFailed** event was raised.</span></span>

<span data-ttu-id="57ee5-116">Para obtener más información sobre el tipo de datos BSTR, vea [usar la biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="57ee5-116">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="57ee5-117">*ShiftKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="57ee5-117">*ShiftKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57ee5-118">El estado de los modificadores de teclado, incluidos Mayús, Mayús, CTRL y ALT.</span><span class="sxs-lookup"><span data-stu-id="57ee5-118">The state of the keyboard modifiers, including SHIFT, CAPS, CTRL, and ALT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57ee5-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57ee5-119">Return value</span></span>

<span data-ttu-id="57ee5-120">Si este evento se realiza correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="57ee5-120">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="57ee5-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="57ee5-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="57ee5-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57ee5-122">Remarks</span></span>

<span data-ttu-id="57ee5-123">El evento **InputFailed** se produce cuando el foco de entrada cambia antes de que se insertara la entrada del usuario en el control adjunto.</span><span class="sxs-lookup"><span data-stu-id="57ee5-123">The **InputFailed** event occurs when input focus changes before user input was inserted into the attached control.</span></span> <span data-ttu-id="57ee5-124">Por ejemplo, si el usuario escribe la entrada manuscrita en el panel de escritura y, a continuación, pulsa en otro control de edición antes de que el reconocedor haya tenido la oportunidad de finalizar, este evento se desencadena.</span><span class="sxs-lookup"><span data-stu-id="57ee5-124">For example, if the user enters ink into the writing pad, then taps on another edit control before the recognizer has had a chance to finish, this event fires.</span></span>

<span data-ttu-id="57ee5-125">Con el identificador de ventana que se pasa a este evento, puede optar por insertar el texto usted mismo cuando se produce este evento.</span><span class="sxs-lookup"><span data-stu-id="57ee5-125">Using the window handle passed into this event, you can choose to insert the text yourself when this event occurs.</span></span>

> [!Note]  
> <span data-ttu-id="57ee5-126">A partir de Microsoft Windows XP Tablet PC Edition 2005, el evento **InputFailed** ya no se aplica.</span><span class="sxs-lookup"><span data-stu-id="57ee5-126">Starting with Microsoft Windows XP Tablet PC Edition 2005, the **InputFailed** event no longer applies.</span></span> <span data-ttu-id="57ee5-127">El texto se inserta siempre antes de que cambie el foco.</span><span class="sxs-lookup"><span data-stu-id="57ee5-127">Text is always inserted before focus changes.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="57ee5-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57ee5-128">Requirements</span></span>



| <span data-ttu-id="57ee5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="57ee5-129">Requirement</span></span> | <span data-ttu-id="57ee5-130">Value</span><span class="sxs-lookup"><span data-stu-id="57ee5-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57ee5-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57ee5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="57ee5-132">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="57ee5-132">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="57ee5-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57ee5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="57ee5-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="57ee5-134">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="57ee5-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57ee5-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="57ee5-136"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="57ee5-136"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="57ee5-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="57ee5-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="57ee5-138"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57ee5-138"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="57ee5-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="57ee5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57ee5-140">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="57ee5-140">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 




