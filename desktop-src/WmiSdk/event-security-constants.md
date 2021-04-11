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
# <a name="event-security-constants"></a>Constantes de seguridad de eventos

A continuación se muestran las constantes de seguridad de WMI que se usan para los eventos. Se usan para establecer entradas de control de acceso (ACE) en descriptores de seguridad usados para eventos o receptores.

<dl> <dt>

<span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**\_publicación correcta de WBEM \_**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Especifica que la cuenta puede publicar eventos en la instancia de [**\_ \_ EventFilter**](--eventfilter.md) que define el filtro de eventos para un consumidor permanente. Disponible en wbemcli. h.


</dt> </dl> </dd> <dt>

<span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**suscripción de WBEM \_ right \_**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Especifica que un consumidor puede suscribirse a los eventos entregados a un receptor. Se usa en [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity). Disponible en wbemcli. h.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**WBEM \_ S \_ sujeto \_ a \_ SDS**
</dt> <dd> <dl> <dt>

274435 (0x43003)
</dt> <dt>



El proveedor de eventos indica que WMI comprueba la propiedad del **\_ descriptor de seguridad** en cada evento (heredado del [**\_ \_ evento**](--event.md)) y solo envía eventos a los consumidores con los permisos de acceso adecuados. Disponible en wbemprov. h.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                         |
| Encabezado<br/>                   | <dl> <dt>Wbemcli. h; </dt> <dt>Wbemprov. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de seguridad de WMI](wmi-security-constants.md)
</dt> <dt>

[Mantenimiento de la seguridad de WMI](maintaining-wmi-security.md)
</dt> <dt>

[Proteger eventos WMI](securing-wmi-events.md)
</dt> </dl>

 

 




