---
description: La \_ enumeración BLOB CHARACTER SET indica el juego de caracteres utilizado por el blob de conferencia \_ actual.
ms.assetid: 79131b84-19b5-492b-a44e-9d47c365b298
title: BLOB_CHARACTER_SET enumeración (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf3b3eeb2278dacd7d8db7aeba224e5d9549e4d0c5544af6e0facf8970f5d62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117948723"
---
# <a name="blob_character_set-enumeration"></a>Enumeración BLOB \_ CHARACTER \_ SET

\[Los controles e interfaces de conferencias de telefonía IP de Encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **\_ enumeración BLOB CHARACTER \_ SET** indica el juego de caracteres utilizado por el blob de conferencia actual.

## <a name="syntax"></a>Syntax


```C++
} BLOB_CHARACTER_SET;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**BCS \_ ASCII**
</dt> <dd>

Formato ASCII estándar.

</dd> <dt>

<span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**BCS \_ UTF7**
</dt> <dd>

Formato de transformación de siete bits de Unicode. Para obtener más información sobre este formato, realice una búsqueda en Internet de RFC 1642.

</dd> <dt>

<span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**BCS \_ UTF8**
</dt> <dd>

Formato de transformación UCS 8. Para obtener más información sobre este formato, realice una búsqueda en Internet del documento ISO (Organización internacional de normalización) e IEC (Comisión electrotécnica internacional (CEI)) ISO/IEC JTC1/SC2/WG2 N 1036, con fecha del 1 de agosto de 1994, por WG2 Project Editor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                               |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> <dt>

[**get \_ CharacterSet**](itconferenceblob-get-characterset.md)
</dt> <dt>

[**Init**](itconferenceblob-init.md)
</dt> <dt>

[**SetConferenceBlob**](itconferenceblob-setconferenceblob.md)
</dt> </dl>

 

 




