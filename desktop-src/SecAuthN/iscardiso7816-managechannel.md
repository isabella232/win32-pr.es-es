---
description: El método ManageChannel crea un comando de unidad de datos de protocolo de aplicación (APDU) que abre y cierra los canales lógicos.
ms.assetid: a55b5b3f-0404-45bd-afeb-e96173319a50
title: 'ISCardISO7816:: ManageChannel (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ManageChannel
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f0b9af92e280781405c2cb570c93e8873a279765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082456"
---
# <a name="iscardiso7816managechannel-method"></a><span data-ttu-id="84c6f-103">ISCardISO7816:: ManageChannel (método)</span><span class="sxs-lookup"><span data-stu-id="84c6f-103">ISCardISO7816::ManageChannel method</span></span>

<span data-ttu-id="84c6f-104">\[El método **ManageChannel** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="84c6f-104">\[The **ManageChannel** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="84c6f-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="84c6f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="84c6f-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="84c6f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="84c6f-107">El método **ManageChannel** crea un comando de [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) que abre y cierra los canales lógicos.</span><span class="sxs-lookup"><span data-stu-id="84c6f-107">The **ManageChannel** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that opens and closes logical channels.</span></span>

<span data-ttu-id="84c6f-108">La función Open abre un nuevo canal lógico distinto del básico.</span><span class="sxs-lookup"><span data-stu-id="84c6f-108">The open function opens a new logical channel other than the basic one.</span></span> <span data-ttu-id="84c6f-109">Se proporcionan opciones para que la tarjeta asigne un número de canal lógico, o para el número de canal lógico que se va a proporcionar a la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="84c6f-109">Options are provided for the card to assign a logical channel number, or for the logical channel number to be supplied to the card.</span></span>

<span data-ttu-id="84c6f-110">La función Close cierra explícitamente un canal lógico que no sea el básico.</span><span class="sxs-lookup"><span data-stu-id="84c6f-110">The close function explicitly closes a logical channel other than the basic one.</span></span> <span data-ttu-id="84c6f-111">Después del cierre correcto, el canal lógico estará disponible para su reutilización.</span><span class="sxs-lookup"><span data-stu-id="84c6f-111">After the successful closing, the logical channel shall be available for re-use.</span></span>

## <a name="syntax"></a><span data-ttu-id="84c6f-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84c6f-112">Syntax</span></span>


```C++
HRESULT ManageChannel(
  [in]      BYTE       byChannelState,
  [in]      BYTE       byChannel,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="84c6f-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84c6f-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84c6f-114">*byChannelState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84c6f-114">*byChannelState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84c6f-115">El bit B8 de P1 se usa para indicar la función Open o la función Close; Si B8 es 0, el canal de administración debe abrir un canal lógico y, si B8 es 1, el canal de administración debe cerrar un canal lógico:</span><span class="sxs-lookup"><span data-stu-id="84c6f-115">Bit b8 of P1 is used to indicate the open function or the close function; if b8 is 0, then MANAGE CHANNEL shall open a logical channel and if b8 is 1, then MANAGE CHANNEL shall close a logical channel:</span></span>

<span data-ttu-id="84c6f-116">P1 = ' 00 ' para abrir</span><span class="sxs-lookup"><span data-stu-id="84c6f-116">P1 = '00' to open</span></span>

<span data-ttu-id="84c6f-117">P1 = ' 80 ' para cerrar</span><span class="sxs-lookup"><span data-stu-id="84c6f-117">P1 = '80' to close</span></span>

<span data-ttu-id="84c6f-118">Otros valores son RFU</span><span class="sxs-lookup"><span data-stu-id="84c6f-118">Other values are RFU</span></span>

</dd> <dt>

<span data-ttu-id="84c6f-119">*byChannel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84c6f-119">*byChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84c6f-120">En el caso de la función Open (P1 = ' 00 '), los bits B1 y B2 de P2 se usan para codificar el número de canal lógico de la misma manera que en el byte de la clase, los otros bits de P2 son RFU.</span><span class="sxs-lookup"><span data-stu-id="84c6f-120">For the open function (P1 = '00'), the bits b1 and b2 of P2 are used to code the logical channel number in the same manner as in the class byte, the other bits of P2 are RFU.</span></span>

<span data-ttu-id="84c6f-121">Cuando B1 y B2 de P2 son **null**, la tarjeta asignará un número de canal lógico que se devolverá en los bits B1 y B2 del campo de datos.</span><span class="sxs-lookup"><span data-stu-id="84c6f-121">When b1 and b2 of P2 are **NULL**, then the card will assign a logical channel number that will be returned in bits b1 and b2 of the data field.</span></span>

<span data-ttu-id="84c6f-122">Cuando B1 y/o B2 de P2 no son **null**, codifican un número de canal lógico distinto del básico; a continuación, la tarjeta abrirá el número de canal lógico asignado externamente.</span><span class="sxs-lookup"><span data-stu-id="84c6f-122">When b1 and/or b2 of P2 are not **NULL**, they code a logical channel number other than the basic one; then the card will open the externally assigned logical channel number.</span></span>

</dd> <dt>

<span data-ttu-id="84c6f-123">*ppCmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="84c6f-123">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="84c6f-124">En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="84c6f-124">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="84c6f-125">En la devolución, se rellena con el comando APDU construido por esta operación.</span><span class="sxs-lookup"><span data-stu-id="84c6f-125">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="84c6f-126">Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="84c6f-126">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84c6f-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84c6f-127">Return value</span></span>

<span data-ttu-id="84c6f-128">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="84c6f-128">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="84c6f-129">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="84c6f-129">Return code</span></span>                                                                                   | <span data-ttu-id="84c6f-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="84c6f-130">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="84c6f-131"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="84c6f-131"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="84c6f-132">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="84c6f-132">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="84c6f-133"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="84c6f-133"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="84c6f-134">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="84c6f-134">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="84c6f-135"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="84c6f-135"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="84c6f-136">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="84c6f-136">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="84c6f-137"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="84c6f-137"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="84c6f-138">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="84c6f-138">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="84c6f-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84c6f-139">Remarks</span></span>

<span data-ttu-id="84c6f-140">Cuando la función Open se realiza correctamente desde el canal lógico básico, el MF se seleccionará implícitamente como el DF actual y el estado de seguridad del nuevo canal lógico debe ser el mismo que el canal lógico básico después de ATR.</span><span class="sxs-lookup"><span data-stu-id="84c6f-140">When the open function is successfully performed from the basic logical channel, the MF shall be implicitly selected as the current DF and the security status of the new logical channel should be the same as the basic logical channel after ATR.</span></span> <span data-ttu-id="84c6f-141">El estado de seguridad del nuevo canal lógico debe ser independiente del de cualquier otro canal lógico.</span><span class="sxs-lookup"><span data-stu-id="84c6f-141">The security status of the new logical channel should be separate from that of any other logical channel.</span></span>

<span data-ttu-id="84c6f-142">Cuando la función Open se realiza correctamente desde un canal lógico, que no es la básica, el DF actual del canal lógico que emitió el comando se seleccionará como el DF actual.</span><span class="sxs-lookup"><span data-stu-id="84c6f-142">When the open function is successfully performed from a logical channel, which is not the basic one, the current DF of the logical channel that issued the command will be selected as the current DF.</span></span> <span data-ttu-id="84c6f-143">Además, el estado de seguridad del nuevo canal lógico debe ser el mismo que el estado de seguridad del canal lógico desde el que se realizó la función abierta.</span><span class="sxs-lookup"><span data-stu-id="84c6f-143">In addition, the security status for the new logical channel should be the same as the security status of the logical channel from which the open function was performed.</span></span>

<span data-ttu-id="84c6f-144">Después de una función de cierre correcta, se pierde el estado de seguridad relacionado con este canal lógico.</span><span class="sxs-lookup"><span data-stu-id="84c6f-144">After a successful close function, the security status related to this logical channel is lost.</span></span>

<span data-ttu-id="84c6f-145">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="84c6f-145">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="84c6f-146">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="84c6f-146">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="84c6f-147">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="84c6f-147">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84c6f-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84c6f-148">Requirements</span></span>



| <span data-ttu-id="84c6f-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="84c6f-149">Requirement</span></span> | <span data-ttu-id="84c6f-150">Value</span><span class="sxs-lookup"><span data-stu-id="84c6f-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84c6f-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84c6f-151">Minimum supported client</span></span><br/> | <span data-ttu-id="84c6f-152">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="84c6f-152">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="84c6f-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84c6f-153">Minimum supported server</span></span><br/> | <span data-ttu-id="84c6f-154">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="84c6f-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="84c6f-155">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="84c6f-155">End of client support</span></span><br/>    | <span data-ttu-id="84c6f-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84c6f-156">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="84c6f-157">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="84c6f-157">End of server support</span></span><br/>    | <span data-ttu-id="84c6f-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="84c6f-158">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="84c6f-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84c6f-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="84c6f-160"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="84c6f-160"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="84c6f-161">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="84c6f-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="84c6f-162"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="84c6f-162"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="84c6f-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="84c6f-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84c6f-164"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84c6f-164"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="84c6f-165">IID</span><span class="sxs-lookup"><span data-stu-id="84c6f-165">IID</span></span><br/>                      | <span data-ttu-id="84c6f-166">IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="84c6f-166">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="84c6f-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="84c6f-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84c6f-168">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="84c6f-168">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
