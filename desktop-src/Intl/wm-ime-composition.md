---
description: Se envía a una aplicación cuando el IME cambia el estado de composición como resultado de una pulsación de tecla. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 6de1c4c2-d910-487c-8b82-408cb6e02c44
title: Mensaje de WM_IME_COMPOSITION (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d795c1e270be978927e3b93743de5fece7021b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003138"
---
# <a name="wm_ime_composition-message"></a><span data-ttu-id="f78b5-104">Mensaje de composición de \_ IME de WM \_</span><span class="sxs-lookup"><span data-stu-id="f78b5-104">WM\_IME\_COMPOSITION message</span></span>

<span data-ttu-id="f78b5-105">Se envía a una aplicación cuando el IME cambia el estado de composición como resultado de una pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="f78b5-105">Sent to an application when the IME changes composition status as a result of a keystroke.</span></span> <span data-ttu-id="f78b5-106">Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f78b5-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,     
  WM_IME_COMPOSITION,   
  WPARAM wParam,
  LPARAM lParam          
);
```



## <a name="parameters"></a><span data-ttu-id="f78b5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f78b5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f78b5-108">*identificador*</span><span class="sxs-lookup"><span data-stu-id="f78b5-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f78b5-109">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="f78b5-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="f78b5-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f78b5-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f78b5-111">Carácter DBCS que representa el cambio más reciente en la cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="f78b5-111">DBCS character representing the latest change to the composition string.</span></span>

</dd> <dt>

<span data-ttu-id="f78b5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f78b5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f78b5-113">Valor que especifica cómo cambió el carácter o la cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="f78b5-113">Value specifying how the composition string or character changed.</span></span> <span data-ttu-id="f78b5-114">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f78b5-114">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="f78b5-115">Para obtener más información sobre estos valores, vea [valores de cadena de composición de IME](ime-composition-string-values.md).</span><span class="sxs-lookup"><span data-stu-id="f78b5-115">For more information about these values, see [IME Composition String Values](ime-composition-string-values.md).</span></span>

<dl><span id="GCS_COMPATTR"></span><span id="gcs_compattr"></span><dt>

<span data-ttu-id="f78b5-116">**GC \_ COMPATTR**</span><span class="sxs-lookup"><span data-stu-id="f78b5-116">**GCS\_COMPATTR**</span></span>
</dt><span id="GCS_COMPCLAUSE"></span><span id="gcs_compclause"></span><dt>

<span data-ttu-id="f78b5-117">**GC \_ COMPCLAUSE**</span><span class="sxs-lookup"><span data-stu-id="f78b5-117">**GCS\_COMPCLAUSE**</span></span>
</dt><span id="GCS_COMPREADSTR"></span><span id="gcs_compreadstr"></span><dt>

<span data-ttu-id="f78b5-118">**GC \_ COMPREADSTR**</span><span class="sxs-lookup"><span data-stu-id="f78b5-118">**GCS\_COMPREADSTR**</span></span>
</dt><span id="GCS_COMPREADATTR"></span><span id="gcs_compreadattr"></span><dt>

<span data-ttu-id="f78b5-119">**GC \_ COMPREADATTR**</span><span class="sxs-lookup"><span data-stu-id="f78b5-119">**GCS\_COMPREADATTR**</span></span>
</dt><span id="GCS_COMPREADCLAUSE"></span><span id="gcs_compreadclause"></span><dt>

<span data-ttu-id="f78b5-120">**GC \_ COMPREADCLAUSE**</span><span class="sxs-lookup"><span data-stu-id="f78b5-120">**GCS\_COMPREADCLAUSE**</span></span>
</dt><span id="GCS_COMPSTR"></span><span id="gcs_compstr"></span><dt>

<span data-ttu-id="f78b5-121">**GC \_ COMPSTR**</span><span class="sxs-lookup"><span data-stu-id="f78b5-121">**GCS\_COMPSTR**</span></span>
</dt><span id="GCS_CURSORPOS"></span><span id="gcs_cursorpos"></span><dt>

<span data-ttu-id="f78b5-122">**GC \_ CURSORPOS**</span><span class="sxs-lookup"><span data-stu-id="f78b5-122">**GCS\_CURSORPOS**</span></span>
</dt><span id="GCS_DELTASTART"></span><span id="gcs_deltastart"></span><dt>

<span data-ttu-id="f78b5-123">**GC \_ DELTASTART**</span><span class="sxs-lookup"><span data-stu-id="f78b5-123">**GCS\_DELTASTART**</span></span>
</dt><span id="GCS_RESULTCLAUSE"></span><span id="gcs_resultclause"></span><dt>

<span data-ttu-id="f78b5-124">**GC \_ RESULTCLAUSE**</span><span class="sxs-lookup"><span data-stu-id="f78b5-124">**GCS\_RESULTCLAUSE**</span></span>
</dt><span id="GCS_RESULTREADCLAUSE"></span><span id="gcs_resultreadclause"></span><dt>

<span data-ttu-id="f78b5-125">**GC \_ RESULTREADCLAUSE**</span><span class="sxs-lookup"><span data-stu-id="f78b5-125">**GCS\_RESULTREADCLAUSE**</span></span>
</dt><span id="GCS_RESULTREADSTR"></span><span id="gcs_resultreadstr"></span><dt>

<span data-ttu-id="f78b5-126">**GC \_ RESULTREADSTR**</span><span class="sxs-lookup"><span data-stu-id="f78b5-126">**GCS\_RESULTREADSTR**</span></span>
</dt><span id="GCS_RESULTSTR"></span><span id="gcs_resultstr"></span><dt>

<span data-ttu-id="f78b5-127">**RESULTSTR de GC \_**</span><span class="sxs-lookup"><span data-stu-id="f78b5-127">**GCS\_RESULTSTR**</span></span>
</dt> </dl>

<span data-ttu-id="f78b5-128">El parámetro *lParam* también puede tener uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f78b5-128">The *lParam* parameter can also have one or more of the following values.</span></span>



| <span data-ttu-id="f78b5-129">Value</span><span class="sxs-lookup"><span data-stu-id="f78b5-129">Value</span></span>                                                                                                                                                            | <span data-ttu-id="f78b5-130">Significado</span><span class="sxs-lookup"><span data-stu-id="f78b5-130">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CS_INSERTCHAR"></span><span id="cs_insertchar"></span><dl> <span data-ttu-id="f78b5-131"><dt>**\_INSERTCHAR CS**</dt></span><span class="sxs-lookup"><span data-stu-id="f78b5-131"><dt>**CS\_INSERTCHAR**</dt></span></span> </dl>    | <span data-ttu-id="f78b5-132">Inserte el carácter de composición *wParam* en el punto de inserción actual.</span><span class="sxs-lookup"><span data-stu-id="f78b5-132">Insert the *wParam* composition character at the current insertion point.</span></span> <span data-ttu-id="f78b5-133">Una aplicación debe mostrar el carácter de composición si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="f78b5-133">An application should display the composition character if it processes this message.</span></span><br/>                                                                                                                                                                                                                                |
| <span id="CS_NOMOVECARET"></span><span id="cs_nomovecaret"></span><dl> <span data-ttu-id="f78b5-134"><dt>**\_NOMOVECARET CS**</dt></span><span class="sxs-lookup"><span data-stu-id="f78b5-134"><dt>**CS\_NOMOVECARET**</dt></span></span> </dl> | <span data-ttu-id="f78b5-135">No mover la posición del símbolo de intercalación como resultado del procesamiento del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f78b5-135">Do not move the caret position as a result of processing the message.</span></span> <span data-ttu-id="f78b5-136">Por ejemplo, si un IME especifica una combinación de CS \_ INSERTCHAR y CS \_ NOMOVECARET, la aplicación debe insertar el carácter especificado en la posición actual del símbolo de intercalación, pero no debe mover el símbolo de intercalación a la posición siguiente.</span><span class="sxs-lookup"><span data-stu-id="f78b5-136">For example, if an IME specifies a combination of CS\_INSERTCHAR and CS\_NOMOVECARET, the application should insert the specified character at the current caret position but should not move the caret to the next position.</span></span> <span data-ttu-id="f78b5-137">Un mensaje de \_ composición del IME de WM posterior \_ con RESULTSTR de GC \_ reemplazará este carácter.</span><span class="sxs-lookup"><span data-stu-id="f78b5-137">A subsequent WM\_IME\_COMPOSITION message with GCS\_RESULTSTR will replace this character.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f78b5-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f78b5-138">Return value</span></span>

<span data-ttu-id="f78b5-139">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="f78b5-139">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f78b5-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f78b5-140">Remarks</span></span>

<span data-ttu-id="f78b5-141">Una aplicación debe procesar este mensaje si muestra los propios caracteres de composición.</span><span class="sxs-lookup"><span data-stu-id="f78b5-141">An application should process this message if it displays composition characters itself.</span></span> <span data-ttu-id="f78b5-142">De lo contrario, debe enviar el mensaje a la ventana del IME.</span><span class="sxs-lookup"><span data-stu-id="f78b5-142">Otherwise, it should send the message to the IME window.</span></span>

<span data-ttu-id="f78b5-143">Si la aplicación ha creado una ventana de IME, debe pasar este mensaje a esa ventana.</span><span class="sxs-lookup"><span data-stu-id="f78b5-143">If the application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="f78b5-144">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  procesa este mensaje pasándolo a la ventana IME predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f78b5-144">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing it to the default IME window.</span></span> <span data-ttu-id="f78b5-145">La ventana del IME procesa este mensaje actualizando su apariencia en función de la marca de cambio especificada.</span><span class="sxs-lookup"><span data-stu-id="f78b5-145">The IME window processes this message by updating its appearance based on the change flag specified.</span></span> <span data-ttu-id="f78b5-146">Una aplicación puede llamar a [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) para recuperar el nuevo estado de composición.</span><span class="sxs-lookup"><span data-stu-id="f78b5-146">An application can call [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) to retrieve the new composition status.</span></span>

<span data-ttu-id="f78b5-147">Si no se establece ninguno de los valores de GC \_ , el mensaje indica que se ha cancelado la composición actual y que las aplicaciones que dibujan la cadena de composición deben eliminar la cadena.</span><span class="sxs-lookup"><span data-stu-id="f78b5-147">If none of the GCS\_ values are set, the message indicates that the current composition has been canceled and applications that draw the composition string should delete the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="f78b5-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f78b5-148">Requirements</span></span>



| <span data-ttu-id="f78b5-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="f78b5-149">Requirement</span></span> | <span data-ttu-id="f78b5-150">Value</span><span class="sxs-lookup"><span data-stu-id="f78b5-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f78b5-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f78b5-151">Minimum supported client</span></span><br/> | <span data-ttu-id="f78b5-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f78b5-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="f78b5-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f78b5-153">Minimum supported server</span></span><br/> | <span data-ttu-id="f78b5-154">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f78b5-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="f78b5-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f78b5-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="f78b5-156"><dt>Winuser. h (include Windows. h); </dt> <dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f78b5-156"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f78b5-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="f78b5-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f78b5-158">Administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="f78b5-158">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="f78b5-159">Mensajes del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="f78b5-159">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="f78b5-160">**ImmGetCompositionString**</span><span class="sxs-lookup"><span data-stu-id="f78b5-160">**ImmGetCompositionString**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)
</dt> </dl>

 

 
