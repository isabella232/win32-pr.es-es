---
description: La \_ enumeración de eventos participante describe los eventos de los participantes.
ms.assetid: 678165f2-ad0b-415f-86bf-8c4e3bd8d793
title: Enumeración PARTICIPANT_EVENT (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 225b1b9901efa5648dfaa326c53ed69cff2c4295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690328"
---
# <a name="participant_event-enumeration"></a>\_Enumeración de eventos de participantes

\[ Esta enumeración no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La enumeración de **\_ eventos participante** describe los eventos de los participantes. El método de [**\_ evento ITParticipantEvent:: get**](itparticipantevent-get-event.md) devuelve un miembro de esta enumeración para indicar el tipo de evento de participante de conferencia que se ha producido. Esta enumeración la usan las aplicaciones que acceden a [IPCONF MSP](ipconf-msp.md).

## <a name="syntax"></a>Sintaxis


```C++
} PARTICIPANT_EVENT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**\_nuevo \_ participante de PE**
</dt> <dd>

Se ha agregado un nuevo participante a la Conferencia.

</dd> <dt>

<span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**\_cambio de información de PE \_**
</dt> <dd>

La información sobre un participante ha cambiado.

</dd> <dt>

<span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**\_ausencia de participante de PE \_**
</dt> <dd>

Un participante ha abandonado la Conferencia.

</dd> <dt>

<span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**\_nuevo \_ subflujo de PE**
</dt> <dd>

Se ha agregado un subflujo nuevo al participante.

</dd> <dt>

<span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**\_SUBFLUJO PE \_ quitado**
</dt> <dd>

Se ha quitado un subflujo nuevo del participante.

</dd> <dt>

<span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**subsecuencia de PE \_ \_ asignada**
</dt> <dd>

Un participante se ha asignado a un subflujo.

</dd> <dt>

<span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**subsecuencia PE sin \_ \_ asignar**
</dt> <dd>

Un participante se ha desasignado de un subflujo.

</dd> <dt>

<span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**tiempo de espera de \_ participante de PE \_**
</dt> <dd>

Se ha quitado un participante de la Conferencia debido a un tiempo de espera agotado.

</dd> <dt>

<span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**participante de PE \_ \_ recuperado**
</dt> <dd>

Un participante quitado vuelve a estar visible. Normalmente, es un participante que ha agotado el tiempo de espera, pero ahora se están recibiendo señales.

</dd> <dt>

<span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**participante de PE \_ \_ activo**
</dt> <dd>

El participante se ha vuelto activo en la Conferencia.

</dd> <dt>

<span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**participante de PE \_ \_ inactivo**
</dt> <dd>

El participante ha dejado de estar activo en la Conferencia.

</dd> <dt>

<span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**\_comunicación local de PE \_**
</dt> <dd>

El participante local ha empezado a hablar.

</dd> <dt>

<span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**PE \_ local \_ silenciosa**
</dt> <dd>

El participante local se ha vuelto silencioso en la Conferencia.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                              |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITParticipantEvent:: get ( \_ evento)**](itparticipantevent-get-event.md)
</dt> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> <dt>

[Interfaces de IPConf MSP](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




