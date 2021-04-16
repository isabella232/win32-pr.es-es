---
description: 'Los miembros de la \_ enumeración información con tipo de participante \_ identifican el tipo de información de participante que recupera el método ITParticipant:: get \_ ParticipantTypedInfo. Esta enumeración la usan las aplicaciones que acceden a IPConf MSP.'
ms.assetid: ca933d8c-bfb4-4a92-b412-112e228ccca2
title: Enumeración PARTICIPANT_TYPED_INFO (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ab94a487f0ea098ee9b92144874057dc463036
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679488"
---
# <a name="participant_typed_info-enumeration"></a>\_Enumeración de información con tipo de participante \_

\[**Participante \_ La \_ información con tipo** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

Los miembros de la enumeración **\_ \_ información con tipo de participante** identifican el tipo de información de participante que recupera el método [**ITParticipant:: get \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) . Esta enumeración la usan las aplicaciones que acceden a [IPCONF MSP](ipconf-msp.md).

## <a name="syntax"></a>Sintaxis


```C++
} PARTICIPANT_TYPED_INFO;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**PTI \_ CANONICALNAME**
</dt> <dd>

Nombre canónico del participante, como someone@example.com .

</dd> <dt>

<span id="PTI_NAME"></span><span id="pti_name"></span>**nombre de PTI \_**
</dt> <dd>

Nombre para mostrar del participante.

</dd> <dt>

<span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**PTI \_ EmailAddress**
</dt> <dd>

Dirección de correo electrónico del participante.

</dd> <dt>

<span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**PTI \_ PHONENUMBER**
</dt> <dd>

Dirección de teléfono del participante.

</dd> <dt>

<span id="PTI_LOCATION"></span><span id="pti_location"></span>**Ubicación de PTI \_**
</dt> <dd>

Dirección geográfica del participante.

</dd> <dt>

<span id="PTI_TOOL"></span><span id="pti_tool"></span>**\_herramienta PTI**
</dt> <dd>

Aplicación del participante.

</dd> <dt>

<span id="PTI_NOTES"></span><span id="pti_notes"></span>**Notas de PTI \_**
</dt> <dd>

Notas sobre el participante.

</dd> <dt>

<span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI \_ privado**
</dt> <dd>

Define una extensión experimental o de descripción de origen específica de la aplicación (SDES). Consulte RFC 1889 para obtener más información.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITParticipant:: get \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md)
</dt> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> <dt>

[Interfaces de IPConf MSP](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




