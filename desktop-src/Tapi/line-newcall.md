---
description: El mensaje NEWCALL de la línea de TSPI \_ se envía a la función de devolución de llamada LINEEVENT cada vez que se recibe una nueva llamada que TAPI no ha originado en una línea abierta por TAPI.
ms.assetid: 36122dfb-1ed6-459d-aa2b-69c86daaddd8
title: Mensaje de LINE_NEWCALL (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed3e7380b2f328283e5f5cad9e84f5a1d0c450dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690387"
---
# <a name="line_newcall-message"></a><span data-ttu-id="8b757-103">Mensaje de línea \_ NEWCALL</span><span class="sxs-lookup"><span data-stu-id="8b757-103">LINE\_NEWCALL message</span></span>

<span data-ttu-id="8b757-104">El mensaje **\_ NEWCALL** de la línea de TSPI se envía a la función de devolución de llamada [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) cada vez que se recibe una nueva llamada que TAPI no ha originado en una línea abierta por TAPI.</span><span class="sxs-lookup"><span data-stu-id="8b757-104">The TSPI **LINE\_NEWCALL** message is sent to the [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) callback function whenever a new call that TAPI has not originated arrives on a line that TAPI has open.</span></span> <span data-ttu-id="8b757-105">Este debe ser el primer mensaje enviado con respecto a esa llamada.</span><span class="sxs-lookup"><span data-stu-id="8b757-105">This must be the first message sent regarding that call.</span></span> <span data-ttu-id="8b757-106">TAPI escribe el identificador opaco *htCall* en la ubicación pasada por el proveedor de servicios como *dwParam2*.</span><span class="sxs-lookup"><span data-stu-id="8b757-106">TAPI writes the *htCall* opaque handle to the location passed by the service provider as *dwParam2*.</span></span> <span data-ttu-id="8b757-107">Esto proporciona al proveedor de servicios el valor *htCall* que se va a usar en los mensajes posteriores.</span><span class="sxs-lookup"><span data-stu-id="8b757-107">This gives the service provider the *htCall* value to be used in subsequent messages.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="8b757-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b757-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b757-109">*htLine*</span><span class="sxs-lookup"><span data-stu-id="8b757-109">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="8b757-110">El identificador de objeto opaco TAPI para el dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="8b757-110">The TAPI opaque object handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="8b757-111">*htCall*</span><span class="sxs-lookup"><span data-stu-id="8b757-111">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="8b757-112">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="8b757-112">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="8b757-113">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="8b757-113">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="8b757-114">La línea de valor \_ NEWCALL.</span><span class="sxs-lookup"><span data-stu-id="8b757-114">The value LINE\_NEWCALL.</span></span>

</dd> <dt>

<span data-ttu-id="8b757-115">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="8b757-115">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="8b757-116">El identificador opaco del proveedor de servicios para la llamada, de tipo [**HDRVCALL**](hdrvline.md).</span><span class="sxs-lookup"><span data-stu-id="8b757-116">The service provider's opaque handle for the call, of type [**HDRVCALL**](hdrvline.md).</span></span> <span data-ttu-id="8b757-117">TAPI pasa este valor como el parámetro *hdCall* para identificar la llamada en los procedimientos subsiguientes que invoca para operar en la llamada.</span><span class="sxs-lookup"><span data-stu-id="8b757-117">TAPI passes this value as the *hdCall* parameter to identify the call in subsequent procedures it invokes to operate on the call.</span></span>

</dd> <dt>

<span data-ttu-id="8b757-118">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="8b757-118">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="8b757-119">Puntero de tipo LPHTAPICALL que señala a un [**HTAPICALL**](htapicall.md).</span><span class="sxs-lookup"><span data-stu-id="8b757-119">A pointer of type LPHTAPICALL pointing to a [**HTAPICALL**](htapicall.md).</span></span> <span data-ttu-id="8b757-120">TAPI escribe el identificador opaco de TAPI para la llamada a la ubicación indicada.</span><span class="sxs-lookup"><span data-stu-id="8b757-120">TAPI writes the TAPI opaque handle for the call to the indicated location.</span></span> <span data-ttu-id="8b757-121">El proveedor de servicios debe guardar este valor y pasarlo como el parámetro *htCall* para identificar la llamada en los eventos posteriores que notifica a la llamada.</span><span class="sxs-lookup"><span data-stu-id="8b757-121">The service provider must save this value and pass it as the *htCall* parameter to identify the call in subsequent events it reports for the call.</span></span>

<span data-ttu-id="8b757-122">Este parámetro también puede adquirir un valor **null** (vea la sección Comentarios siguiente).</span><span class="sxs-lookup"><span data-stu-id="8b757-122">This parameter can also acquire a value of **NULL** (see the following Remarks section).</span></span>

</dd> <dt>

<span data-ttu-id="8b757-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="8b757-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="8b757-124">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="8b757-124">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b757-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b757-125">Remarks</span></span>

<span data-ttu-id="8b757-126">El proveedor de servicios debe enviar el mensaje [**line \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) como el siguiente mensaje para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="8b757-126">The service provider should send the [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) message as the next message for this call.</span></span> <span data-ttu-id="8b757-127">El evento **line \_ NEWCALL** es inusual en que también devuelve un valor al proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="8b757-127">The **LINE\_NEWCALL** event is unusual in that it also passes a value back to the service provider.</span></span>

<span data-ttu-id="8b757-128">Esta función informa de todas las llamadas nuevas que se originan en el proveedor de servicios (entrante, saliente, iniciada en el teléfono, etc.) para las que TAPI y el proveedor de servicios aún no han intercambiado los identificadores opacos.</span><span class="sxs-lookup"><span data-stu-id="8b757-128">This function reports any new calls that originate in the service provider (inbound, outbound, initiated at the phone, and so on) for which TAPI and the service provider have not yet exchanged opaque handles.</span></span> <span data-ttu-id="8b757-129">Los identificadores se intercambian para que TAPI y el proveedor de servicios puedan crear solicitudes y eventos de informe que impliquen la llamada.</span><span class="sxs-lookup"><span data-stu-id="8b757-129">The handles are exchanged so that TAPI and the service provider can subsequently make requests and report events involving the call.</span></span> <span data-ttu-id="8b757-130">Dado que estas nuevas llamadas no están necesariamente entrantes, las llamadas pueden estar inicialmente en cualquier Estado, no necesariamente en el estado de la *oferta* .</span><span class="sxs-lookup"><span data-stu-id="8b757-130">Because these new calls are not necessarily inbound, the calls can initially be in any state, not necessarily the *offering* state.</span></span> <span data-ttu-id="8b757-131">Si el proveedor de servicios se inicia y detecta que una o más llamadas ya están activas en la línea, informa a TAPI de ellas con mensajes de **línea \_ NEWCALL** seguidos de los mensajes de [**línea \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) que indican el estado actual.</span><span class="sxs-lookup"><span data-stu-id="8b757-131">If the service provider starts and discovers that one or more calls are already active on the line, it informs TAPI of them with **LINE\_NEWCALL** messages followed by [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) messages indicating the current state.</span></span> <span data-ttu-id="8b757-132">Una nueva llamada de salida, iniciada en el teléfono por el usuario, se notificará con un mensaje **line \_ NEWCALL** y el **mensaje \_ CALLSTATE** de la línea inicial indicaría que la llamada se encontraba en el estado **ditono** (y continuaría desde allí).</span><span class="sxs-lookup"><span data-stu-id="8b757-132">A new outgoing call, initiated on the phone by the user, would be reported with a **LINE\_NEWCALL** message, and the initial **LINE\_CALLSTATE** message would indicate that the call was in **DIALTONE** state (and then continuing on from there).</span></span>

<span data-ttu-id="8b757-133">Si el proveedor de servicios pasa un gran número de llamadas a TAPI en un período de tiempo muy breve (durante el mismo ciclo de interrupción), TAPI puede volver a iniciar sesión en el procesamiento de esas llamadas.</span><span class="sxs-lookup"><span data-stu-id="8b757-133">If the service provider passes a large number of calls to TAPI in a very short amount of time (during the same interrupt cycle), TAPI can become backlogged in processing those calls.</span></span> <span data-ttu-id="8b757-134">Cuando esto sucede, TAPI indica al proveedor de servicios que espere un poco de tiempo antes de enviar más llamadas.</span><span class="sxs-lookup"><span data-stu-id="8b757-134">When this happens, TAPI signals to the service provider to wait a short time before sending any more calls.</span></span> <span data-ttu-id="8b757-135">Indica esto escribiendo un valor **null**, en lugar de un [**HTAPICALL**](htapicall.md)válido, en la ubicación a la que señala el parámetro *dwParam2* de la **línea \_ NEWCALL**.</span><span class="sxs-lookup"><span data-stu-id="8b757-135">It signals this by writing a value of **NULL**, instead of a valid [**HTAPICALL**](htapicall.md), into the location pointed to by the *dwParam2* parameter of **LINE\_NEWCALL**.</span></span> <span data-ttu-id="8b757-136">Esto indica que el intento de procesar el identificador de llamada recién ofrecido no se realizó correctamente, probablemente debido a una imposibilidad temporal de asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="8b757-136">This indicates that the attempt to process the newly offered call handle was not successful, most likely due to a temporary inability to allocate memory.</span></span> <span data-ttu-id="8b757-137">El proveedor de servicios puede responder quitando la llamada o reenviando el mensaje **de \_ NEWCALL de línea** después de un retraso de programación (durante el cual el proveedor de servicios debe proporcionar el procesador para permitir que TAPI procese otras acciones pendientes).</span><span class="sxs-lookup"><span data-stu-id="8b757-137">The service provider can respond by dropping the call or by resending the **LINE\_NEWCALL** message after a scheduling delay (during which time the service provider should yield the processor to allow TAPI to process other pending actions).</span></span> <span data-ttu-id="8b757-138">En cualquier caso, no se pueden pasar más mensajes con respecto a la nueva llamada a TAPI hasta que el intercambio de identificadores se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="8b757-138">In any case, no further messages regarding the new call can be passed to TAPI until the handle exchange succeeds.</span></span> <span data-ttu-id="8b757-139">Cuando la ubicación a la que apunta *dwParam2* adquiere un valor distinto de **null** , el proveedor de servicios sabe que este valor es un identificador [**HTAPICALL**](htapicall.md) válido para la llamada.</span><span class="sxs-lookup"><span data-stu-id="8b757-139">When the location pointed to by *dwParam2* acquires a non-**NULL** value, the service provider knows that this value is a valid [**HTAPICALL**](htapicall.md) handle to the call.</span></span>

<span data-ttu-id="8b757-140">No hay ningún mensaje directamente correspondiente en el nivel de TAPI.</span><span class="sxs-lookup"><span data-stu-id="8b757-140">There is no directly corresponding message at the TAPI level.</span></span> <span data-ttu-id="8b757-141">Este mensaje se usa en el nivel TSPI para introducir de forma única y sin ambigüedad una nueva llamada entrante a TAPI y recuperar el identificador opaco de TAPI para la llamada.</span><span class="sxs-lookup"><span data-stu-id="8b757-141">This message is used at the TSPI level to uniquely and unambiguously introduce a new incoming call to TAPI and retrieve the TAPI opaque identifier for the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b757-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b757-142">Requirements</span></span>



| <span data-ttu-id="8b757-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b757-143">Requirement</span></span> | <span data-ttu-id="8b757-144">Value</span><span class="sxs-lookup"><span data-stu-id="8b757-144">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8b757-145">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="8b757-145">TAPI version</span></span><br/> | <span data-ttu-id="8b757-146">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8b757-146">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8b757-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b757-147">Header</span></span><br/>       | <dl> <span data-ttu-id="8b757-148"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b757-148"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b757-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b757-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="8b757-150">[**LÍNEA \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8b757-150">[**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8b757-151">**LINEEVENT**</span><span class="sxs-lookup"><span data-stu-id="8b757-151">**LINEEVENT**</span></span>](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> </dl>

 

