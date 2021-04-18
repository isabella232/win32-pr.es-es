---
description: La \_ enumeración del juego de caracteres de blob \_ indica el juego de caracteres utilizado por el BLOB de la Conferencia actual.
ms.assetid: 79131b84-19b5-492b-a44e-9d47c365b298
title: Enumeración BLOB_CHARACTER_SET (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b180a8574f1643a5fc1be134be99c951faaf1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680404"
---
# <a name="blob_character_set-enumeration"></a>\_Enumeración de juegos de caracteres de blob \_

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La enumeración del **\_ \_ juego de caracteres de BLOB** indica el juego de caracteres utilizado por el BLOB de la Conferencia actual.

## <a name="syntax"></a>Sintaxis


```C++
} BLOB_CHARACTER_SET;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**ASCII de BCS \_**
</dt> <dd>

Formato ASCII estándar.

</dd> <dt>

<span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**UTF7 de BCS \_**
</dt> <dd>

Formato de transformación de siete bits de Unicode. Para obtener más información sobre este formato, realice una búsqueda en Internet de RFC 1642.

</dd> <dt>

<span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**UTF8 de BCS \_**
</dt> <dd>

Formato de transformación UCS 8. Para obtener más información sobre este formato, realice una búsqueda en Internet de ISO (el Organización internacional de normalización) e IEC (el Comisión electrotécnica internacional (CEI)) documento ISO/IEC JTC1/SC2/WG2 N 1036, con fecha del 1 de agosto de 1994, por el editor de proyectos de WG2.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                               |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> <dt>

[**obtener \_ characterSet**](itconferenceblob-get-characterset.md)
</dt> <dt>

[**Smss**](itconferenceblob-init.md)
</dt> <dt>

[**SetConferenceBlob**](itconferenceblob-setconferenceblob.md)
</dt> </dl>

 

 




