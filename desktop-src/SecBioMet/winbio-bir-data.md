---
title: WINBIO_BIR_DATA estructura (Winbio \_ types.h)
description: Especifica el tamaño, en bytes, y el desplazamiento de un bloque de información biométrica.
ms.assetid: 2f73eb1f-f1a1-4831-a8f7-eec28aa51645
keywords:
- WINBIO_BIR_DATA estructura Windows API de marco biométrico
topic_type:
- apiref
api_name:
- WINBIO_BIR_DATA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01978cf55d90e217aa50fb8fad696f6af90b33ab9e59975a901daa99db633181
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911058"
---
# <a name="winbio_bir_data-structure"></a>Estructura DE DATOS DE WINBIO \_ BIR \_

La **estructura DE DATOS \_ \_ DE WINBIO BIR** especifica el tamaño, en bytes, y el desplazamiento de un bloque de información biométrica. La estructura BIR de [**WINBIO \_**](winbio-bir.md) usa esta estructura para especificar dónde se encuentran las distintas partes de un registro de información biométrica.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WINBIO_BIR_DATA {
  ULONG Size;
  ULONG Offset;
} WINBIO_BIR_DATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Tamaño**
</dt> <dd>

Tamaño, en bytes, de la información biométrica.

</dd> <dt>

**Offset**
</dt> <dd>

Desplazamiento, en bytes desde el principio de la [**estructura \_ BIR de WINBIO,**](winbio-bir.md) de la información biométrica.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El uso de desplazamientos en lugar de punteros permite una serialización sencilla de BIR y una traducción menos complicada entre entornos de 32 y 64 bits o entre el modo de usuario y kernel.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> <dt>

[**WINBIO \_ BIR**](winbio-bir.md)
</dt> <dt>

[**ENCABEZADO WINBIO \_ BIR \_**](winbio-bir-header.md)
</dt> </dl>

 

 





