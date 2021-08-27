---
description: Los miembros de la enumeración PARTICIPANT TYPED INFO identifican el tipo de información de participante que recupera el \_ \_ método ITParticipant::get \_ ParticipantTypedInfo. Esta enumeración la usan las aplicaciones que acceden al MSP de IPConf.
ms.assetid: ca933d8c-bfb4-4a92-b412-112e228ccca2
title: PARTICIPANT_TYPED_INFO enumeración (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de57331cd0774409118b7253fd5705879e3b3504b04b20a16aa2df269504512
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100575"
---
# <a name="participant_typed_info-enumeration"></a>PARTICIPANT \_ TYPED \_ INFO (enumeración)

\[**PARTICIPANTE \_ TYPED \_ INFO** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

Los miembros de la enumeración **PARTICIPANT \_ TYPED \_ INFO** identifican el tipo de información de participante que recupera el [**método ITParticipant::get \_ ParticipantTypedInfo.**](itparticipant-get-participanttypedinfo.md) Esta enumeración la usan las aplicaciones que acceden al [MSP de IPConf.](ipconf-msp.md)

## <a name="syntax"></a>Syntax


```C++
} PARTICIPANT_TYPED_INFO;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**PTI \_ CANONICALNAME**
</dt> <dd>

Nombre canónico del participante, como someone@example.com .

</dd> <dt>

<span id="PTI_NAME"></span><span id="pti_name"></span>**PTI \_ NAME**
</dt> <dd>

Nombre que se puede mostrar del participante.

</dd> <dt>

<span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**DIRECCIÓN DE CORREO ELECTRÓNICO DE PTI \_**
</dt> <dd>

Dirección de correo electrónico del participante.

</dd> <dt>

<span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**PTI \_ PHONENUMBER**
</dt> <dd>

Dirección de teléfono del participante.

</dd> <dt>

<span id="PTI_LOCATION"></span><span id="pti_location"></span>**UBICACIÓN \_ DE PTI**
</dt> <dd>

Dirección geográfica del participante.

</dd> <dt>

<span id="PTI_TOOL"></span><span id="pti_tool"></span>**HERRAMIENTA \_ PTI**
</dt> <dd>

Aplicación del participante.

</dd> <dt>

<span id="PTI_NOTES"></span><span id="pti_notes"></span>**NOTAS \_ DE PTI**
</dt> <dd>

Notas relativas al participante.

</dd> <dt>

<span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI \_ PRIVATE**
</dt> <dd>

Define una extensión de descripción de origen (SDES) experimental o específica de la aplicación. Consulte RFC 1889 para obtener más información.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITParticipant::get \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md)
</dt> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> <dt>

[IPConf MSP Interfaces](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




