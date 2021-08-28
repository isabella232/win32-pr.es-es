---
description: La \_ enumeración PARTICIPANT EVENT describe los eventos del participante.
ms.assetid: 678165f2-ad0b-415f-86bf-8c4e3bd8d793
title: PARTICIPANT_EVENT enumeración (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5eb7a98a445ecb89b25fe2d18ef77be31aa54b5fac2920814fba2c4a3f6b08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959775"
---
# <a name="participant_event-enumeration"></a>ENUMERACIÓN \_ PARTICIPANT EVENT

\[Esta enumeración no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **\_ enumeración PARTICIPANT EVENT** describe los eventos del participante. El [**método ITParticipantEvent::get \_ Event**](itparticipantevent-get-event.md) devuelve un miembro de esta enumeración para indicar el tipo de evento de participante de la conferencia que se ha producido. Esta enumeración la usan las aplicaciones que acceden al [MSP de IPConf.](ipconf-msp.md)

## <a name="syntax"></a>Syntax


```C++
} PARTICIPANT_EVENT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**NUEVO PARTICIPANTE DE PE \_ \_**
</dt> <dd>

Se ha agregado un nuevo participante a la conferencia.

</dd> <dt>

<span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**CAMBIO DE \_ INFORMACIÓN DE \_ PE**
</dt> <dd>

La información sobre un participante ha cambiado.

</dd> <dt>

<span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**PE \_ PARTICIPANT \_ LEAVE**
</dt> <dd>

Un participante ha dejado la conferencia.

</dd> <dt>

<span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**NUEVA \_ \_ SECUENCIA DE PE**
</dt> <dd>

Se ha agregado una nueva subsección al participante.

</dd> <dt>

<span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**PE \_ SUBSTREAM \_ REMOVED**
</dt> <dd>

Se ha quitado una nueva subsección del participante.

</dd> <dt>

<span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**PE \_ SUBSTREAM \_ MAPPED**
</dt> <dd>

Un participante se ha asignado a una subsección.

</dd> <dt>

<span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**PE \_ SUBSTREAM \_ UNMAPPED**
</dt> <dd>

Se ha desaprobado un participante de una subsección.

</dd> <dt>

<span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**TIEMPO DE ESPERA \_ DEL PARTICIPANTE DE PE \_**
</dt> <dd>

Un participante se ha quitado de la conferencia debido a un tiempo de espera.

</dd> <dt>

<span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**PARTICIPANTE DE PE \_ \_ RECUPERADO**
</dt> <dd>

Un participante eliminado vuelve a estar visible. Normalmente, se trata de un participante que ha pasado el tiempo de espera, pero ahora se reciben señales.

</dd> <dt>

<span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**PARTICIPANTE DE PE \_ \_ ACTIVO**
</dt> <dd>

El participante se ha activado en la conferencia.

</dd> <dt>

<span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**PARTICIPANTE DE PE \_ \_ INACTIVO**
</dt> <dd>

El participante se ha vuelto inactivo en la conferencia.

</dd> <dt>

<span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**PE \_ LOCAL \_ TALKING**
</dt> <dd>

El participante local ha empezado a hablar.

</dd> <dt>

<span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**PE \_ LOCAL \_ SILENT**
</dt> <dd>

El participante local se ha quedado silencioso en la conferencia.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                              |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITParticipantEvent::get \_ (Evento)**](itparticipantevent-get-event.md)
</dt> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> <dt>

[IPConf MSP Interfaces](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




