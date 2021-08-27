---
description: 'Más información sobre: JET_BKLOGTIME estructura'
title: JET_BKLOGTIME estructura
TOCTitle: JET_BKLOGTIME Structure
ms:assetid: 31460079-7c5b-4145-837d-b112ba0117d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269219(v=EXCHG.10)
ms:contentKeyID: 32765522
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2d6f8e3f77d905eb601441ad8ab3ca88bb08f59d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478531"
---
# <a name="jet_bklogtime-structure"></a>JET_BKLOGTIME estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_bklogtime-structure"></a>JET_BKLOGTIME estructura

La **JET_BKLOGTIME** contiene los elementos de fecha y hora de un evento. Es una extensión de [JET_LOGTIME](./jet-logtime-structure.md).

**Windows Vista: JET_BKLOGTIME** se introdujo en Windows Vista.

```cpp
    typedef struct {
      char bSeconds;
      char bMinutes;
      char bHours;
      char bDay;
      char bMonth;
        char bYear;
        union {
        char bFiller1;
        struct {
          unsigned char fTimeIsUTC: 1;
          unsigned char fUnused: 7;
        };
      };
      union {
        char bFiller2;
        struct {
          unsigned char fOSSnapshot  :1;
          unsigned char fReserved  :7;
        };
      };
    } JET_BKLOGTIME;
```

### <a name="members"></a>Miembros

**bSeconds**

Hora del evento en segundos. Puede ser de 0 (cero) a 60. Se usa 0 (cero) cuando la **JET_BKLOGTIME** estructura es "null".

**bMinutes**

Hora del evento en minutos. Puede ser de 0 (cero) a 60. Se usa 0 (cero) cuando la **JET_BKLOGTIME** estructura es "null".

**bHours**

Hora del evento en horas. Puede ser de 0 (cero) a 24. Se usa 0 (cero) cuando la **JET_BKLOGTIME** estructura es "null".

**Cumpleaños**

Día del mes del evento. Puede ser de 0 (cero) a 31. Se usa 0 (cero) cuando la **JET_BKLOGTIME** estructura es "null".

**bMonth**

Mes del año del evento. Puede ser de 0 (cero) a 12. Se usa 0 (cero) cuando la **JET_BKLOGTIME** estructura es "null".

**bYear**

Año (desplazamiento por 1900) del evento. Para lograr el año real, agregue 1900 a este valor. Se usa 0 (cero) cuando la **JET_BKLOGTIME** estructura es "null".

**bFiller1**

Este campo debe omitirse.

**fTimeIsUTC**

La hora está en formato UTC.

**fUnused**

Este campo debe omitirse.

**bFiller2**

Este campo debe omitirse.

**fOSSnapshot**

Si este evento es una copia de seguridad, esta marca contiene uno de los siguientes valores posibles:


| <p>Nombre</p> | <p>Valor</p> | 
|-------------|--------------|
| <p>copia de seguridad de streaming</p> | <p>0 (cero)</p> | 
| <p>copia de seguridad de instantáneas</p> | <p>1</p> | 



**fReserved**

Este campo debe omitirse.

### <a name="remarks"></a>Comentarios

Esta estructura se usa al depurar.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
