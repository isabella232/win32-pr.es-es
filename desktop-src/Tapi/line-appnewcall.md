---
description: Se envía el mensaje APPNEWCALL de línea de TAPI \_ para informar a una aplicación cuando se ha creado un nuevo identificador de llamada espontáneamente en su nombre.
ms.assetid: 0c263025-e719-453e-91c4-a9f2d9321db3
title: Mensaje de LINE_APPNEWCALL (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33d24ca816fb69384e90e4215edbc90b9410b887
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680775"
---
# <a name="line_appnewcall-message"></a><span data-ttu-id="ff0c5-103">Mensaje de línea \_ APPNEWCALL</span><span class="sxs-lookup"><span data-stu-id="ff0c5-103">LINE\_APPNEWCALL message</span></span>

<span data-ttu-id="ff0c5-104">Se envía el mensaje **\_ APPNEWCALL de línea** de TAPI para informar a una aplicación cuando un nuevo identificador de llamada se ha creado espontáneamente en su nombre (excepto a través de una llamada de API de la aplicación, en cuyo caso el identificador se habría devuelto a través de un parámetro de puntero pasado a la función).</span><span class="sxs-lookup"><span data-stu-id="ff0c5-104">The TAPI **LINE\_APPNEWCALL** message is sent to inform an application when a new call handle has been spontaneously created on its behalf (other than through an API call from the application, in which case the handle would have been returned through a pointer parameter passed into the function).</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="ff0c5-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff0c5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff0c5-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="ff0c5-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="ff0c5-107">Identificador de la aplicación para el dispositivo de línea en el que se ha creado la llamada.</span><span class="sxs-lookup"><span data-stu-id="ff0c5-107">The application's handle to the line device on which the call has been created.</span></span>

</dd> <dt>

<span data-ttu-id="ff0c5-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="ff0c5-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="ff0c5-109">Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ff0c5-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="ff0c5-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="ff0c5-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="ff0c5-111">Identificador de la dirección en la línea en la que aparece la llamada.</span><span class="sxs-lookup"><span data-stu-id="ff0c5-111">Identifier of the address on the line on which the call appears.</span></span> <span data-ttu-id="ff0c5-112">Un identificador de dirección está asociado de forma permanente a una dirección; el identificador permanece constante en las actualizaciones del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ff0c5-112">An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.</span></span>

</dd> <dt>

<span data-ttu-id="ff0c5-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="ff0c5-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="ff0c5-114">Identificador de la aplicación para la nueva llamada.</span><span class="sxs-lookup"><span data-stu-id="ff0c5-114">The application's handle to the new call.</span></span>

</dd> <dt>

<span data-ttu-id="ff0c5-115">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="ff0c5-115">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="ff0c5-116">El privilegio Applications para la nueva llamada (LINECALLPRIVILEGE \_ Owner o LINECALLPRIVILEGE \_ monitor).</span><span class="sxs-lookup"><span data-stu-id="ff0c5-116">The applications privilege to the new call (LINECALLPRIVILEGE\_OWNER or LINECALLPRIVILEGE\_MONITOR).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff0c5-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff0c5-117">Return value</span></span>

<span data-ttu-id="ff0c5-118">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ff0c5-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff0c5-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff0c5-119">Remarks</span></span>

<span data-ttu-id="ff0c5-120">Las aplicaciones que admiten la versión 2,0 o posterior de TAPI recibirán un mensaje de **línea \_ APPNEWCALL** cada vez que la aplicación reciba un identificador de una nueva llamada espontáneamente.</span><span class="sxs-lookup"><span data-stu-id="ff0c5-120">Applications supporting TAPI version 2.0 or later are sent a **LINE\_APPNEWCALL** message whenever the application is spontaneously given a handle to a new call.</span></span> <span data-ttu-id="ff0c5-121">Dado que el mensaje incluye los parámetros *hLine* y *dwAddressID* en los que existe la llamada, la aplicación puede crear fácilmente un nuevo objeto de llamada en el contexto correcto.</span><span class="sxs-lookup"><span data-stu-id="ff0c5-121">Because the message includes the *hLine* and *dwAddressID* parameters on which the call exists, the application can readily create a new call object in the correct context.</span></span> <span data-ttu-id="ff0c5-122">El mensaje **line \_ APPNEWCALL** siempre va seguido inmediatamente de un mensaje [**line \_ CALLSTATE**](line-callstate.md) que indica el estado inicial de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ff0c5-122">The **LINE\_APPNEWCALL** message is always immediately followed by a [**LINE\_CALLSTATE**](line-callstate.md) message indicating the initial state of the call.</span></span>

<span data-ttu-id="ff0c5-123">Las aplicaciones anteriores (que negociaron una versión de API anterior a 2,0) solo se envían a un mensaje de [**línea \_ CALLSTATE**](line-callstate.md) , como se documenta en versiones anteriores de la API.</span><span class="sxs-lookup"><span data-stu-id="ff0c5-123">Older applications (that negotiated an API version earlier than 2.0) are sent only a [**LINE\_CALLSTATE**](line-callstate.md) message, as documented in previous versions of the API.</span></span> <span data-ttu-id="ff0c5-124">Dichas aplicaciones crearían un nuevo objeto Call al recibir un mensaje [**line \_ CALLSTATE**](line-callstate.md) que tiene *dwParam3* establecido en un valor distinto de cero y que contiene un identificador de llamada que la aplicación no conoce actualmente.</span><span class="sxs-lookup"><span data-stu-id="ff0c5-124">Such applications would create a new call object upon receiving a [**LINE\_CALLSTATE**](line-callstate.md) message that has *dwParam3* set to a nonzero value and containing a call handle not presently known by the application.</span></span> <span data-ttu-id="ff0c5-125">Las desventajas son que (a) la aplicación debe llamar a [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) para determinar los parámetros *hLine* y *dwAddressID* asociados con la llamada. (b) la aplicación debe examinar todos los identificadores de llamadas conocidos para determinar que la llamada es una llamada nueva. y (c) es posible, en determinadas condiciones, para que la aplicación piense que está recibiendo un nuevo identificador de llamada cuando en realidad ha desasignado su identificador a la llamada (por ejemplo, la aplicación ha desasignado simplemente un identificador de llamada, pero un mensaje de [**línea \_ CALLSTATE**](line-callstate.md) que le asigna la propiedad de la aplicación de la llamada debido a un [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff) de otra aplicación ya estaba en la cola de mensajes TAPI de la aplicación)</span><span class="sxs-lookup"><span data-stu-id="ff0c5-125">The disadvantages are that (a) the application must call [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) to determine the *hLine* and *dwAddressID* parameters associated with the call; (b) the application must scan all known call handles to determine that the call is a new call; and (c) it is possible, under certain conditions, for the application to think it is receiving a new call handle when in reality it has just deallocated its handle to the call (for example, the application has just deallocated a call handle, but a [**LINE\_CALLSTATE**](line-callstate.md) message giving the application ownership of the call due to a [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff) from another application was already in the application's TAPI message queue).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff0c5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff0c5-126">Requirements</span></span>



| <span data-ttu-id="ff0c5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff0c5-127">Requirement</span></span> | <span data-ttu-id="ff0c5-128">Value</span><span class="sxs-lookup"><span data-stu-id="ff0c5-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ff0c5-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="ff0c5-129">TAPI version</span></span><br/> | <span data-ttu-id="ff0c5-130">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="ff0c5-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ff0c5-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff0c5-131">Header</span></span><br/>       | <dl> <span data-ttu-id="ff0c5-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff0c5-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff0c5-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff0c5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff0c5-134">**LÍNEA \_ CALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="ff0c5-134">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="ff0c5-135">**lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="ff0c5-135">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[<span data-ttu-id="ff0c5-136">**lineHandoff**</span><span class="sxs-lookup"><span data-stu-id="ff0c5-136">**lineHandoff**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehandoff)
</dt> </dl>

 

 




