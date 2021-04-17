---
description: Contiene la fecha de fabricación de una batería.
ms.assetid: 0cda66fc-bf4a-4a38-b43c-6eecde46c414
title: BATTERY_MANUFACTURE_DATE estructura (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_MANUFACTURE_DATE
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: cdd3f067bc3ed2e3339710e0a5bd48c8f42e6525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667223"
---
# <a name="battery_manufacture_date-structure"></a>Estructura de fecha de \_ fabricación de la batería \_

Contiene la fecha de fabricación de una batería. La estructura de [**\_ \_ información de consulta**](battery-query-information-str.md) de la batería usa esta estructura cuando se solicita el nivel de información de BatteryManufactureDate.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _BATTERY_MANUFACTURE_DATE {
  UCHAR  Day;
  UCHAR  Month;
  USHORT Year;
} BATTERY_MANUFACTURE_DATE, *PBATTERY_MANUFACTURE_DATE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Day**
</dt> <dd>

Día del mes de fabricación, en el intervalo de 1 a 31. A pesar del tipo de datos, no es un valor codificado en ASCII. Es un byte sin signo.

</dd> <dt>

**Mensuales**
</dt> <dd>

El mes de fabricación, en el intervalo de 1 (enero) a 12 (diciembre). A pesar del tipo de datos, no es un valor codificado en ASCII. Es un byte sin signo.

</dd> <dt>

**Anual**
</dt> <dd>

Año de fabricación. Normalmente estará en el intervalo 1900-2100.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La fecha se codifica en el formato de calendario gregoriano o occidental.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Encabezado<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h en Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_información de consulta de la batería \_**](battery-query-information-str.md)
</dt> <dt>

[**\_información de \_ consulta de batería ioctl \_**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




