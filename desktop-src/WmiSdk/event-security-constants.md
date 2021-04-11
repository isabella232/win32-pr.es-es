---
description: A continuación se muestran las constantes de seguridad de WMI que se usan para los eventos. Se usan para establecer entradas de control de acceso (ACE) en descriptores de seguridad usados para eventos o receptores.
ms.assetid: 18318262-d948-4329-8d48-23664798fc58
ms.tgt_platform: multiple
title: Constantes de seguridad de evento (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3009b16e468a647ee96b9be365286caba2c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156001"
---
# <a name="event-security-constants"></a><span data-ttu-id="ddb5b-104">Constantes de seguridad de eventos</span><span class="sxs-lookup"><span data-stu-id="ddb5b-104">Event Security Constants</span></span>

<span data-ttu-id="ddb5b-105">A continuación se muestran las constantes de seguridad de WMI que se usan para los eventos.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-105">The following shows the WMI security constants used for events.</span></span> <span data-ttu-id="ddb5b-106">Se usan para establecer entradas de control de acceso (ACE) en descriptores de seguridad usados para eventos o receptores.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-106">They are used to set access control entries (ACEs) in security descriptors used for events or sinks.</span></span>

<dl> <dt>

<span data-ttu-id="ddb5b-107"><span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**\_publicación correcta de WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="ddb5b-107"><span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**WBEM\_RIGHT\_PUBLISH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb5b-108">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="ddb5b-108">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="ddb5b-109">Especifica que la cuenta puede publicar eventos en la instancia de [**\_ \_ EventFilter**](--eventfilter.md) que define el filtro de eventos para un consumidor permanente.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-109">Specifies that the account can publish events to the instance of [**\_\_EventFilter**](--eventfilter.md) that defines the event filter for a permanent consumer.</span></span> <span data-ttu-id="ddb5b-110">Disponible en wbemcli. h.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-110">Available in wbemcli.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ddb5b-111"><span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**suscripción de WBEM \_ right \_**</span><span class="sxs-lookup"><span data-stu-id="ddb5b-111"><span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**WBEM\_RIGHT\_SUBSCRIBE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb5b-112">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="ddb5b-112">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="ddb5b-113">Especifica que un consumidor puede suscribirse a los eventos entregados a un receptor.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-113">Specifies that a consumer can subscribe to the events delivered to a sink.</span></span> <span data-ttu-id="ddb5b-114">Se usa en [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity).</span><span class="sxs-lookup"><span data-stu-id="ddb5b-114">Used in [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity).</span></span> <span data-ttu-id="ddb5b-115">Disponible en wbemcli. h.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-115">Available in wbemcli.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ddb5b-116"><span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**WBEM \_ S \_ sujeto \_ a \_ SDS**</span><span class="sxs-lookup"><span data-stu-id="ddb5b-116"><span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**WBEM\_S\_SUBJECT\_TO\_SDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb5b-117">274435 (0x43003)</span><span class="sxs-lookup"><span data-stu-id="ddb5b-117">274435 (0x43003)</span></span>
</dt> <dt>



<span data-ttu-id="ddb5b-118">El proveedor de eventos indica que WMI comprueba la propiedad del **\_ descriptor de seguridad** en cada evento (heredado del [**\_ \_ evento**](--event.md)) y solo envía eventos a los consumidores con los permisos de acceso adecuados.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-118">Event provider indicates that WMI checks the **SECURITY\_DESCRIPTOR** property in each event (inherited from [**\_\_Event**](--event.md)), and only sends events to consumers with the appropriate access permissions.</span></span> <span data-ttu-id="ddb5b-119">Disponible en wbemprov. h.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-119">Available in wbemprov.h.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ddb5b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddb5b-120">Requirements</span></span>



| <span data-ttu-id="ddb5b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddb5b-121">Requirement</span></span> | <span data-ttu-id="ddb5b-122">Value</span><span class="sxs-lookup"><span data-stu-id="ddb5b-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddb5b-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddb5b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ddb5b-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ddb5b-124">Windows Vista</span></span><br/>                                                                                                                               |
| <span data-ttu-id="ddb5b-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddb5b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ddb5b-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddb5b-126">Windows Server 2008</span></span><br/>                                                                                                                         |
| <span data-ttu-id="ddb5b-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ddb5b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddb5b-128"><dt>Wbemcli. h; </dt> <dt>Wbemprov. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddb5b-128"><dt>Wbemcli.h; </dt> <dt>Wbemprov.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddb5b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddb5b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddb5b-130">Constantes de seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="ddb5b-130">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="ddb5b-131">Mantenimiento de la seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="ddb5b-131">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="ddb5b-132">Proteger eventos WMI</span><span class="sxs-lookup"><span data-stu-id="ddb5b-132">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

 




