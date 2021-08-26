---
description: Contiene la fecha de fabricación de una batería.
ms.assetid: 0cda66fc-bf4a-4a38-b43c-6eecde46c414
title: BATTERY_MANUFACTURE_DATE estructura (Poclass.h)
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
ms.openlocfilehash: 30a70fed151304d189fa91b20106e1154ca0e9f4ea5225c52bf1023dbd218346
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032975"
---
# <a name="battery_manufacture_date-structure"></a>Battery \_ Manufacture \_ Date Structure

Contiene la fecha de fabricación de una batería. Esta estructura la usa la estructura [**BATTERY \_ QUERY \_ INFORMATION**](battery-query-information-str.md) cuando se solicita el nivel de información BatteryManufactureDate.

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

El día del mes de fabricación, en el intervalo de 1 a 31. A pesar del tipo de datos, no se trata de un valor codificado ASCII. Es un byte sin signo.

</dd> <dt>

**Month (Mes)**
</dt> <dd>

El mes de fabricación, en el intervalo de 1 (enero) a 12 (diciembre). A pesar del tipo de datos, no se trata de un valor codificado ASCII. Es un byte sin signo.

</dd> <dt>

**año**
</dt> <dd>

Año de fabricación. Normalmente, estará en el intervalo 1900-2100.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La fecha se codifica en el formato de calendario gregoriano u occidental.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                                                                                                                                                                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h en Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INFORMACIÓN DE \_ CONSULTA DE \_ BATERÍA**](battery-query-information-str.md)
</dt> <dt>

[**INFORMACIÓN DE CONSULTA \_ DE LA \_ BATERÍA DE IOCTL \_**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




