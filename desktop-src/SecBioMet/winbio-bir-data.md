---
title: Estructura de WINBIO_BIR_DATA (Winbio \_ Types. h)
description: Especifica el tamaño, en bytes, y el desplazamiento de un bloque de información biométrica.
ms.assetid: 2f73eb1f-f1a1-4831-a8f7-eec28aa51645
keywords:
- Plataforma de biometría de Windows API de WINBIO_BIR_DATA Structure
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
ms.openlocfilehash: 41ebf7b157c5bd806442cdc120350a89ce646f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422282"
---
# <a name="winbio_bir_data-structure"></a>Estructura de datos de WINBIO \_ Bir \_

La estructura de **\_ \_ datos de WINBIO Bir** especifica el tamaño, en bytes, y el desplazamiento de un bloque de información biométrica. La estructura [**WINBIO \_ Bir**](winbio-bir.md) usa esta estructura para especificar dónde se encuentran las distintas partes de un registro de información biométrica.

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

Desplazamiento, en bytes desde el principio de la estructura de [**\_ Bir de WINBIO**](winbio-bir.md) , de la información de biométrica.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El uso de desplazamientos en lugar de punteros permite una sencilla serialización de BIR y para una traducción menos complicada entre los entornos 32 y 64-bit o entre el modo de usuario y kernel.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de aplicación cliente](client-application-structures.md)
</dt> <dt>

[**WINBIO \_ Bir**](winbio-bir.md)
</dt> <dt>

[**WINBIO \_ \_ encabezado Bir**](winbio-bir-header.md)
</dt> </dl>

 

 





