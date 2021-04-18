---
title: IMsRdpClientNonScriptable SendKeys (método)
description: Envía una serie de pulsaciones de teclas al control. Las pulsaciones de teclas están en formato de código de examen, que son los datos de teclado de las claves físicas reales.
ms.assetid: 1f07a9cc-4795-43cb-ac99-4bb70b8b544a
ms.tgt_platform: multiple
keywords:
- Método SendKeys Servicios de Escritorio remoto
- Método SendKeys Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable, método SendKeys
- Método SendKeys Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable2, método SendKeys
- Método SendKeys Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, método SendKeys
- Método SendKeys Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, método SendKeys
- Método SendKeys Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, método SendKeys
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.SendKeys
- IMsRdpClientNonScriptable2.SendKeys
- IMsRdpClientNonScriptable3.SendKeys
- IMsRdpClientNonScriptable4.SendKeys
- IMsRdpClientNonScriptable5.SendKeys
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9effa3bbd40eb64df55914b9adbc07a03ea0c465
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491657"
---
# <a name="imsrdpclientnonscriptablesendkeys-method"></a><span data-ttu-id="c04b6-115">IMsRdpClientNonScriptable:: SendKeys (método)</span><span class="sxs-lookup"><span data-stu-id="c04b6-115">IMsRdpClientNonScriptable::SendKeys method</span></span>

<span data-ttu-id="c04b6-116">Envía una serie de pulsaciones de teclas al control.</span><span class="sxs-lookup"><span data-stu-id="c04b6-116">Sends a series of keystrokes to the control.</span></span> <span data-ttu-id="c04b6-117">Las pulsaciones de teclas están en formato de código de examen, que son los datos de teclado de las claves físicas reales.</span><span class="sxs-lookup"><span data-stu-id="c04b6-117">The keystrokes are in scan code form, which is the keyboard data from the actual physical keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="c04b6-118">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c04b6-118">Syntax</span></span>


```C++
HRESULT SendKeys(
  [in] LONG         numKeys,
  [in] VARIANT_BOOL *pbArrayKeyUp,
  [in] LONG         *plKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="c04b6-119">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c04b6-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c04b6-120">*numKeys* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c04b6-120">*numKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c04b6-121">Número de pulsaciones de tecla que se van a enviar.</span><span class="sxs-lookup"><span data-stu-id="c04b6-121">The number of keystrokes to send.</span></span> <span data-ttu-id="c04b6-122">El número máximo de claves que se pueden enviar en una operación es 20.</span><span class="sxs-lookup"><span data-stu-id="c04b6-122">The maximum number of keys that can be sent in one operation is 20.</span></span> <span data-ttu-id="c04b6-123">El método devuelve **E \_ INVALIDARG** si este parámetro es mayor que 20.</span><span class="sxs-lookup"><span data-stu-id="c04b6-123">The method returns **E\_INVALIDARG** if this parameter is greater than 20.</span></span> <span data-ttu-id="c04b6-124">Para obtener más información, vea la sección Comentarios que se muestra más adelante.</span><span class="sxs-lookup"><span data-stu-id="c04b6-124">For more information, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="c04b6-125">*pbArrayKeyUp* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c04b6-125">*pbArrayKeyUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c04b6-126">Matriz cuyo tamaño es igual a *numKeys*.</span><span class="sxs-lookup"><span data-stu-id="c04b6-126">An array whose size is equal to *numKeys*.</span></span> <span data-ttu-id="c04b6-127">Un elemento es **true** si la tecla correspondiente está activa y **false** si la tecla correspondiente está fuera de la actividad.</span><span class="sxs-lookup"><span data-stu-id="c04b6-127">An element is **TRUE** if the corresponding key is UP and **FALSE** if the corresponding key is DOWN.</span></span>

</dd> <dt>

<span data-ttu-id="c04b6-128">*plKeyData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c04b6-128">*plKeyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c04b6-129">Matriz cuyo tamaño es igual a *numKeys*.</span><span class="sxs-lookup"><span data-stu-id="c04b6-129">An array whose size is equal to *numKeys*.</span></span> <span data-ttu-id="c04b6-130">La matriz contiene datos de pulsación de teclas y corresponde al valor del parámetro *lParam* del mensaje de [ \_ KEYDOWN de WM](../inputdev/wm-keydown.md) .</span><span class="sxs-lookup"><span data-stu-id="c04b6-130">The array contains keystroke data and corresponds to the value of the *lParam* parameter of the [WM\_KEYDOWN](../inputdev/wm-keydown.md) message.</span></span> <span data-ttu-id="c04b6-131">Los datos especifican el número de repeticiones, el código de digitalización, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición.</span><span class="sxs-lookup"><span data-stu-id="c04b6-131">The data specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag.</span></span> <span data-ttu-id="c04b6-132">Para obtener una descripción de los bits de esta matriz, vea la muestra de [WM \_ ](../inputdev/wm-keydown.md).</span><span class="sxs-lookup"><span data-stu-id="c04b6-132">For a description of the bits in this array, see [WM\_KEYDOWN](../inputdev/wm-keydown.md).</span></span>

<span data-ttu-id="c04b6-133">El elemento correspondiente en *pbArrayKeyUp* indica si la tecla está arriba o abajo.</span><span class="sxs-lookup"><span data-stu-id="c04b6-133">The corresponding element in *pbArrayKeyUp* indicates if the key is UP or DOWN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c04b6-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c04b6-134">Return value</span></span>

<span data-ttu-id="c04b6-135">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="c04b6-135">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c04b6-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c04b6-136">Remarks</span></span>

<span data-ttu-id="c04b6-137">El método **SendKeys** no combina las pulsaciones de teclas realizadas por el usuario local con pulsaciones de teclas que el método está enviando.</span><span class="sxs-lookup"><span data-stu-id="c04b6-137">The **SendKeys** method does not mix keystrokes made by the local user with keystrokes that the method is sending.</span></span> <span data-ttu-id="c04b6-138">Todas las pulsaciones de tecla que se pasan al método se envían a la sesión remota en una sola secuencia atómica.</span><span class="sxs-lookup"><span data-stu-id="c04b6-138">All keystrokes passed to the method are sent to the remote session in a single atomic sequence.</span></span>

<span data-ttu-id="c04b6-139">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c04b6-139">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c04b6-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c04b6-140">Requirements</span></span>



| <span data-ttu-id="c04b6-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="c04b6-141">Requirement</span></span> | <span data-ttu-id="c04b6-142">Value</span><span class="sxs-lookup"><span data-stu-id="c04b6-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c04b6-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c04b6-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c04b6-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c04b6-144">Windows Vista</span></span><br/>                                                                     |
| <span data-ttu-id="c04b6-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c04b6-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c04b6-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c04b6-146">Windows Server 2008</span></span><br/>                                                               |
| <span data-ttu-id="c04b6-147">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c04b6-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="c04b6-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c04b6-148"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="c04b6-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c04b6-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c04b6-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c04b6-150"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="c04b6-151">IID</span><span class="sxs-lookup"><span data-stu-id="c04b6-151">IID</span></span><br/>                      | <span data-ttu-id="c04b6-152">IID \_ IMsRdpClientNonScriptable se define como 2f079c4c-87b2-4afd-97ab-20cdb43038ae</span><span class="sxs-lookup"><span data-stu-id="c04b6-152">IID\_IMsRdpClientNonScriptable is defined as 2f079c4c-87b2-4afd-97ab-20cdb43038ae</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c04b6-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="c04b6-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c04b6-154">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="c04b6-154">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="c04b6-155">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="c04b6-155">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="c04b6-156">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="c04b6-156">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="c04b6-157">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="c04b6-157">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="c04b6-158">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="c04b6-158">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="c04b6-159">KEYDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="c04b6-159">WM\_KEYDOWN</span></span>](../inputdev/wm-keydown.md)
</dt> </dl>

 

