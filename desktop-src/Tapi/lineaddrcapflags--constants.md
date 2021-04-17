---
description: Las \_ constantes de marcador de bits LINEADDRCAPFLAGS se usan en el miembro dwAddrCapFlags de la estructura de datos LINEADDRESSCAPS para describir diversas funcionalidades de dirección booleana.
ms.assetid: 530af273-82ba-4310-8aac-266d657e1bfe
title: Constantes de LINEADDRCAPFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce6c8bebb5683d5ecb7d576ff7d376ad0d62cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690224"
---
# <a name="lineaddrcapflags_-constants"></a><span data-ttu-id="a7cd3-103">Constantes de LINEADDRCAPFLAGS \_</span><span class="sxs-lookup"><span data-stu-id="a7cd3-103">LINEADDRCAPFLAGS\_ Constants</span></span>

<span data-ttu-id="a7cd3-104">Las  \_ constantes de marcador de bits LINEADDRCAPFLAGS se usan en el miembro **dwAddrCapFlags** de la estructura de datos [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) para describir diversas funcionalidades de dirección booleana.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-104">The **LINEADDRCAPFLAGS**\_ bit-flag constants are used in the **dwAddrCapFlags** member of the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) data structure to describe various Boolean address capabilities.</span></span>

<dl> <dt>

<span data-ttu-id="a7cd3-105"><span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**LINEADDRCAPFLAGS \_ ACCEPTTOALERT**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-105"><span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**LINEADDRCAPFLAGS\_ACCEPTTOALERT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-106">**True** si se debe aceptar una llamada de oferta mediante [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) para iniciar la alerta de los usuarios en ambos extremos de la llamada. en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-106">**TRUE** if an offering call must be accepted using [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) to start alerting the users at both ends of the call; otherwise, **FALSE**.</span></span> <span data-ttu-id="a7cd3-107">Normalmente, solo se usa con ISDN.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-107">This is typically only used with ISDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-108"><span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**LINEADDRCAPFLAGS \_ ACDGROUP**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-108"><span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**LINEADDRCAPFLAGS\_ACDGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-109">La dirección admite [grupos ACD](about-call-center-controls.md#acd-group-object) en relación con las operaciones del centro de llamadas.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-109">The address supports [ACD Groups](about-call-center-controls.md#acd-group-object) in connection with call center operations.</span></span> <span data-ttu-id="a7cd3-110">Consulte [acerca de los controles del centro de llamadas](./about-call-center-controls.md) para obtener información adicional sobre los grupos ACD.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-110">See [About Call Center Controls](./about-call-center-controls.md) for additional information on ACD groups.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-111"><span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**LINEADDRCAPFLAGS \_ reconexión automática**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-111"><span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**LINEADDRCAPFLAGS\_AUTORECONNECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-112">Especifica si la eliminación de una llamada de consulta se vuelve a conectar automáticamente a la llamada en la espera de la consulta.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-112">Specifies whether dropping a consultation call automatically reconnects to the call on consultation hold.</span></span> <span data-ttu-id="a7cd3-113">**True** si la reconexión se produce automáticamente; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-113">**TRUE** if reconnect happens automatically; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-114"><span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**LINEADDRCAPFLAGS \_ BLOCKIDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-114"><span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**LINEADDRCAPFLAGS\_BLOCKIDDEFAULT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-115">Especifica si la red envía o bloquea de forma predeterminada información de identificador de autor de la llamada al efectuar una llamada a esta dirección.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-115">Specifies whether the network by default sends or blocks caller ID information when making a call on this address.</span></span> <span data-ttu-id="a7cd3-116">Si es **true**, la información del identificador está bloqueada de forma predeterminada; Si es **false**, la información del identificador se transmite de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-116">If **TRUE**, identifier information is blocked by default; if **FALSE**, identifier information is transmitted by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-117"><span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**LINEADDRCAPFLAGS \_ BLOCKIDOVERRIDE**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-117"><span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**LINEADDRCAPFLAGS\_BLOCKIDOVERRIDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-118">Especifica si se puede invalidar la configuración predeterminada para enviar o bloquear la información de identificador de llamada por llamada.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-118">Specifies whether the default setting for sending or blocking of caller ID information can be overridden per call.</span></span> <span data-ttu-id="a7cd3-119">Si es **true**, se puede reemplazar. Si es **false**, no se puede reemplazar.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-119">If **TRUE**, override is possible; if **FALSE**, override is not possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-120"><span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**LINEADDRCAPFLAGS \_ COMPLETIONID**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-120"><span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**LINEADDRCAPFLAGS\_COMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-121">Especifica si los identificadores de finalización devueltos por [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) son útiles y únicos.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-121">Specifies whether the completion identifiers returned by [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) are useful and unique.</span></span> <span data-ttu-id="a7cd3-122">**True si es** útil; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-122">**TRUE** if useful; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-123"><span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**LINEADDRCAPFLAGS \_ CONFDROP**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-123"><span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**LINEADDRCAPFLAGS\_CONFDROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-124">**True** si [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) en una llamada de conferencia Parent también tiene el efecto secundario de quitar (es decir, desconectar) las demás partes implicadas en la llamada de conferencia; **False** si la eliminación de una llamada de Conferencia sigue permitiendo a las demás partes comunicarse entre ellas.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-124">**TRUE** if [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) on a conference call parent also has the side effect of dropping (that is, disconnecting) the other parties involved in the conference call; **FALSE** if dropping a conference call still allows the other parties to talk among themselves.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-125"><span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**LINEADDRCAPFLAGS \_ CONFERENCEHELD**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-125"><span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**LINEADDRCAPFLAGS\_CONFERENCEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-126">Especifica si se puede realizar la Conferencia de una llamada de retención.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-126">Specifies whether a hard-held call can be conferenced to.</span></span> <span data-ttu-id="a7cd3-127">A menudo, solo las llamadas en la espera de la consulta se pueden agregar a como una llamada de conferencia.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-127">Often, only calls on consultation hold can be added to as a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-128"><span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**LINEADDRCAPFLAGS \_ CONFERENCEMAKE**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-128"><span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**LINEADDRCAPFLAGS\_CONFERENCEMAKE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-129">Especifica si se puede establecer una llamada completamente nueva para su uso como una llamada de consulta (para agregar) en la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-129">Specifies whether an entirely new call can be established for use as a consultation call (to add) on conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-130"><span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**LINEADDRCAPFLAGS \_ DESTOFFHOOK**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-130"><span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**LINEADDRCAPFLAGS\_DESTOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-131">Especifica si el teléfono de la entidad a la que se llama puede forzarse automáticamente OffHook al realizar llamadas.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-131">Specifies whether the called party's phone can automatically be forced offhook when making calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-132"><span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**\_marcado LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-132"><span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**LINEADDRCAPFLAGS\_DIALED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-133">Especifica si se puede marcar una dirección de destino en esta dirección para realizar una llamada.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-133">Specifies whether a destination address can be dialed on this address for making a call.</span></span> <span data-ttu-id="a7cd3-134">**True** si se debe marcar una dirección de destino; **False** si la dirección de destino es fija (como con un "teléfono activo").</span><span class="sxs-lookup"><span data-stu-id="a7cd3-134">**TRUE** if a destination address must be dialed; **FALSE** if the destination address is fixed (as with a "hot phone").</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-135"><span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**LINEADDRCAPFLAGS \_ FWDBUSYNAADDR**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-135"><span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**LINEADDRCAPFLAGS\_FWDBUSYNAADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-136">Especifica si el reenvío de llamadas para ocupado y para ninguna respuesta puede usar diferentes direcciones de reenvío.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-136">Specifies whether call forwarding for busy and for no answer can use different forwarding addresses.</span></span> <span data-ttu-id="a7cd3-137">Esta marca solo es significativa si el reenvío está ocupado y no se puede controlar por separado.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-137">This flag is meaningful only if forwarding for busy and for no answer can be controlled separately.</span></span> <span data-ttu-id="a7cd3-138">Esta marca es **true** si el reenvío está ocupado y para ninguna respuesta puede usar direcciones de destino diferentes. de lo contrario, es **false**.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-138">This flag is **TRUE** if forwarding for busy and for no answer can use different destination addresses; otherwise, it is **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-139"><span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**LINEADDRCAPFLAGS \_ FWDCONSULT**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-139"><span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**LINEADDRCAPFLAGS\_FWDCONSULT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-140">Especifica si el reenvío de llamadas implica el establecimiento de una llamada de consulta.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-140">Specifies whether call forwarding involves the establishment of a consultation call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-141"><span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**LINEADDRCAPFLAGS \_ FWDINTEXTADDR**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-141"><span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**LINEADDRCAPFLAGS\_FWDINTEXTADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-142">Especifica si las llamadas internas y externas se pueden reenviar a diferentes direcciones de reenvío.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-142">Specifies whether internal and external calls can be forwarded to different forwarding addresses.</span></span> <span data-ttu-id="a7cd3-143">Este marcador solo es significativo si el reenvío de llamadas internas y externas se puede controlar por separado.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-143">This flag is meaningful only if forwarding of internal and external calls can be controlled separately.</span></span> <span data-ttu-id="a7cd3-144">Esta marca es **true** si las llamadas internas y externas se pueden reenviar a direcciones de destino diferentes; de lo contrario, es **false**.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-144">This flag is **TRUE** if internal and external calls can be forwarded to different destination addresses; otherwise, it is **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-145"><span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**LINEADDRCAPFLAGS \_ FWDNUMRINGS**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-145"><span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**LINEADDRCAPFLAGS\_FWDNUMRINGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-146">Especifica si el número de anillos de una respuesta no se puede especificar cuando el reenvío de llamadas no responde.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-146">Specifies whether the number of rings for a no-answer can be specified when forwarding calls on no answer.</span></span> <span data-ttu-id="a7cd3-147">Si es **true**, el intervalo válido se proporciona en los miembros **dwMinFwdNumRings** y **dwMaxFwdNumRings** de la estructura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .</span><span class="sxs-lookup"><span data-stu-id="a7cd3-147">If **TRUE**, the valid range is provided in the **dwMinFwdNumRings** and **dwMaxFwdNumRings** members of the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-148"><span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**LINEADDRCAPFLAGS \_ FWDSTATUSVALID**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-148"><span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**LINEADDRCAPFLAGS\_FWDSTATUSVALID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-149">Especifica si el estado de reenvío de la estructura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) para esta dirección es válido o es como máximo una "estimación óptima", dada la ausencia de confirmación precisa del conmutador o la red.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-149">Specifies whether the forwarding status in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure for this address is valid or is at most a "best estimate," given absence of accurate confirmation by the switch or network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-150"><span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**LINEADDRCAPFLAGS \_ HOLDMAKESNEW**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-150"><span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**LINEADDRCAPFLAGS\_HOLDMAKESNEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-151">Cuando una llamada en esta dirección se coloca en espera (mediante [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) o una acción externa), se crea automáticamente una nueva llamada (lo que es más probable en LINECALLSTATE \_ ditono).</span><span class="sxs-lookup"><span data-stu-id="a7cd3-151">When a call on this address is placed on hold (using [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) or external action), a new call is automatically created (most likely in LINECALLSTATE\_DIALTONE).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-152"><span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**LINEADDRCAPFLAGS \_ NOEXTERNALCALLS**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-152"><span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**LINEADDRCAPFLAGS\_NOEXTERNALCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-153">La dirección está asociada a una línea interna en una PBX que está restringida de forma que no se puede usar para realizar llamadas a una dirección fuera del conmutador (por ejemplo, es una Intercom).</span><span class="sxs-lookup"><span data-stu-id="a7cd3-153">The address is associated with an internal line on a PBX that is restricted in such a way that it cannot be used to place calls to an address outside the switch (for example, it is an intercom).</span></span> <span data-ttu-id="a7cd3-154">La aplicación puede usar esta indicación para ayudar al usuario a seleccionar la apariencia de llamada correcta que se va a usar para realizar una llamada.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-154">The application can use this indication to assist the user in selecting the correct call appearance to use for making a call.</span></span> <span data-ttu-id="a7cd3-155">Cuando este bit está desactivado, no indica necesariamente que la dirección se puede usar para realizar llamadas externas, ya que el proveedor de servicios no puede ser Cognizant del tipo de línea.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-155">When this bit is off, it does not necessarily indicate that the address can be used to make external calls, because the service provider may not be cognizant of the line type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-156"><span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**LINEADDRCAPFLAGS \_ NOINTERNALCALLS**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-156"><span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**LINEADDRCAPFLAGS\_NOINTERNALCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-157">La dirección está asociada a una línea directa (tronco) y no se puede usar para realizar llamadas internas en una PBX.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-157">The address is associated with a direct CO line (trunk), and cannot be used to make internal calls on a PBX.</span></span> <span data-ttu-id="a7cd3-158">La aplicación puede usar esta indicación para ayudar al usuario a seleccionar la apariencia de llamada correcta que se va a usar para realizar una llamada.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-158">The application can use this indication to assist the user in selecting the correct call appearance to use for making a call.</span></span> <span data-ttu-id="a7cd3-159">Cuando este bit está desactivado, no indica necesariamente que la dirección se puede usar para realizar llamadas internas, ya que el proveedor de servicios no puede ser Cognizant del tipo de línea.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-159">When this bit is off, it does not necessarily indicate that the address can be used to make internal calls, because the service provider may not be cognizant of the line type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-160"><span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**LINEADDRCAPFLAGS \_ NOPSTNADDRESSTRANSLATION**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-160"><span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**LINEADDRCAPFLAGS\_NOPSTNADDRESSTRANSLATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-161">Esta dirección no admite la traducción de direcciones de red telefónicas conmutadas públicamente.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-161">This address does not support public switched telephone network address translation.</span></span> <span data-ttu-id="a7cd3-162">Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 3,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-162">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-163"><span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**LINEADDRCAPFLAGS \_ ORIGOFFHOOK**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-163"><span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**LINEADDRCAPFLAGS\_ORIGOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-164">Especifica si el teléfono de la entidad de origen puede tomarse automáticamente OffHook al realizar llamadas.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-164">Specifies whether the originating party's phone can automatically be taken offhook when making calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-165"><span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**LINEADDRCAPFLAGS \_ PARTIALDIAL**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-165"><span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**LINEADDRCAPFLAGS\_PARTIALDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-166">Especifica si el marcado parcial está disponible.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-166">Specifies whether partial dialing is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-167"><span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**LINEADDRCAPFLAGS \_ PICKUPCALLWAIT**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-167"><span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**LINEADDRCAPFLAGS\_PICKUPCALLWAIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-168">**True** si [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) se puede usar para recoger una llamada detectada por el usuario como una llamada de llamada en espera; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-168">**TRUE** if [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) can be used to pick up a call detected by the user as a call-waiting call; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-169"><span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**LINEADDRCAPFLAGS \_ PICKUPGROUPID**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-169"><span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**LINEADDRCAPFLAGS\_PICKUPGROUPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-170">Especifica si se requiere un identificador de grupo para la recogida de llamadas.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-170">Specifies whether a group identifier is required for call pickup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-171"><span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**LINEADDRCAPFLAGS \_ PREDICTIVEDIALER**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-171"><span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**LINEADDRCAPFLAGS\_PREDICTIVEDIALER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-172">Esta dirección tiene funciones mejoradas de supervisión del progreso de las llamadas que se pueden aplicar a las llamadas salientes para determinar los Estados de la llamada, como *timbre*, *ocupado*, *specialinfo* y *conectado*, o el tipo de medio del dispositivo que responde a la llamada.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-172">This address has enhanced call progress monitoring capabilities which can be applied to outgoing calls to determine call states such as *ringback*, *busy*, *specialinfo*, and *connected*, or the media type of the device answering the call.</span></span> <span data-ttu-id="a7cd3-173">También puede tener la capacidad de transferir automáticamente llamadas salientes a otra dirección cuando una llamada alcanza cualquiera de un conjunto predefinido de Estados.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-173">It may also have the ability to automatically transfer outgoing calls to another address when a call reaches any of a predefined set of states.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-174"><span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**\_cola LINEADDRCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-174"><span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**LINEADDRCAPFLAGS\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-175">Esta dirección no está asociada a una estación o un dispositivo físico determinados, pero es un lugar en el que las llamadas esperan para un procesamiento posterior.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-175">This address is not associated with a particular station or physical device, but is a holding place where calls wait for further processing.</span></span> <span data-ttu-id="a7cd3-176">Las llamadas que se colocan en la cola pueden recibir un tratamiento determinado.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-176">The calls placed in the queue may receive a particular treatment.</span></span> <span data-ttu-id="a7cd3-177">También se pueden transferir automáticamente cuando un recurso determinado está disponible (por ejemplo, si la cola es una cola de ACD y las llamadas están esperando a un agente disponible).</span><span class="sxs-lookup"><span data-stu-id="a7cd3-177">They may also be automatically transferred when a particular resource becomes available (for example, if the queue is an ACD queue and calls are waiting for an available agent).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-178"><span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**LINEADDRCAPFLAGS \_ ROUTEPOINT**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-178"><span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**LINEADDRCAPFLAGS\_ROUTEPOINT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-179">Esta dirección no está asociada a una estación o un dispositivo físico determinados, pero es un lugar en el que las llamadas esperan a que la aplicación realice el enrutamiento (la aplicación examina la dirección a la que se llama y puede redirigir la llamada a otra dirección).</span><span class="sxs-lookup"><span data-stu-id="a7cd3-179">This address is not associated with a particular station or physical device, but is a holding place where calls wait for routing by the application (the application examines the called address, and can redirect the call to another address).</span></span> <span data-ttu-id="a7cd3-180">La llamada también se puede transferir automáticamente si expira el tiempo de espera de enrutamiento (el conmutador normalmente presupone un enrutamiento predeterminado).</span><span class="sxs-lookup"><span data-stu-id="a7cd3-180">The call can also be automatically transferred if a routing timeout expires (the switch usually assumes a default routing).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-181"><span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**LINEADDRCAPFLAGS \_ seguro**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-181"><span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**LINEADDRCAPFLAGS\_SECURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-182">Especifica si las llamadas en esta dirección se pueden proteger en el momento de la configuración de la llamada.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-182">Specifies whether calls on this address can be made secure at call-setup time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-183"><span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**LINEADDRCAPFLAGS \_ SETCALLINGID**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-183"><span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**LINEADDRCAPFLAGS\_SETCALLINGID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-184">La aplicación puede optar por establecer el miembro **CallingPartyID** en [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) al llamar a [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) y a otras funciones que aceptan una estructura **LINECALLPARAMS** .</span><span class="sxs-lookup"><span data-stu-id="a7cd3-184">The application can choose to set the **CallingPartyID** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) when calling [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) and other functions that accept a **LINECALLPARAMS** structure.</span></span> <span data-ttu-id="a7cd3-185">El proveedor de servicios, si el contenido del identificador es aceptable y está disponible una ruta de acceso, pasar el identificador a la parte llamada para indicar la identidad de la entidad de llamada.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-185">The service provider will, if the content of the identifier is acceptable and a path is available, pass the identifier along to the called party to indicate the identity of the calling party.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-186"><span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**LINEADDRCAPFLAGS \_ SETUPCONFNULL**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-186"><span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**LINEADDRCAPFLAGS\_SETUPCONFNULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-187">Especifica si la configuración de una llamada de conferencia comienza con una llamada inicial (**false**) o sin una llamada inicial (**true**).</span><span class="sxs-lookup"><span data-stu-id="a7cd3-187">Specifies whether setting up a conference call starts out with an initial call (**FALSE**) or with no initial call (**TRUE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-188"><span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**LINEADDRCAPFLAGS \_ TRANSFERHELD**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-188"><span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**LINEADDRCAPFLAGS\_TRANSFERHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-189">Especifica si se puede transferir una llamada de retención.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-189">Specifies whether a hard-held call can be transferred.</span></span> <span data-ttu-id="a7cd3-190">A menudo, solo se pueden transferir llamadas en la espera de la consulta.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-190">Often, only calls on consultation hold can be transferred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7cd3-191"><span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**LINEADDRCAPFLAGS \_ TRANSFERMAKE**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-191"><span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**LINEADDRCAPFLAGS\_TRANSFERMAKE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7cd3-192">Especifica si se puede establecer una llamada completamente nueva para su uso como una llamada de consulta en la transferencia.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-192">Specifies whether an entirely new call can be established for use as a consultation call on transfer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7cd3-193">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7cd3-193">Remarks</span></span>

<span data-ttu-id="a7cd3-194">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-194">No extensibility.</span></span> <span data-ttu-id="a7cd3-195">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="a7cd3-195">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7cd3-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7cd3-196">Requirements</span></span>



| <span data-ttu-id="a7cd3-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7cd3-197">Requirement</span></span> | <span data-ttu-id="a7cd3-198">Value</span><span class="sxs-lookup"><span data-stu-id="a7cd3-198">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a7cd3-199">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="a7cd3-199">TAPI version</span></span><br/> | <span data-ttu-id="a7cd3-200">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a7cd3-200">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="a7cd3-201">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7cd3-201">Header</span></span><br/>       | <dl> <span data-ttu-id="a7cd3-202"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7cd3-202"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7cd3-203">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7cd3-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7cd3-204">**lineAccept**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-204">**lineAccept**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaccept)
</dt> <dt>

[<span data-ttu-id="a7cd3-205">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-205">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="a7cd3-206">**LINEADDRESSSTATUS**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-206">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="a7cd3-207">**LINECALLPARAMS**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-207">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="a7cd3-208">**lineCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-208">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[<span data-ttu-id="a7cd3-209">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-209">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="a7cd3-210">**lineHold**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-210">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> <dt>

[<span data-ttu-id="a7cd3-211">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-211">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="a7cd3-212">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="a7cd3-212">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

