---
description: La estructura PID MAP contiene identifica el contenido de un identificador de paquete de flujo de transporte \_ MPEG-2.
ms.assetid: c247ec75-483d-4587-a82f-07bbf6d277b4
title: PID_MAP estructura (Bdatypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PID_MAP
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 98b238c61ccfcfb93e4ddcc0a051d9084228f604
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063188"
---
# <a name="pid_map-structure"></a>Pid \_ MAP (estructura)

La estructura contiene identifica el contenido de un identificador de paquete de flujo de transporte `PID_MAP` MPEG-2.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  ULONG                ulPID;
  MEDIA_SAMPLE_CONTENT MediaSampleContent;
} PID_MAP;
```



## <a name="members"></a>Members

<dl> <dt>

**ulPID**
</dt> <dd>

Especifica el identificador de paquete (PID)

</dd> <dt>

**MediaSampleContent**
</dt> <dd>

Especifica el contenido de la carga del paquete, como un [**tipo de enumeración MEDIA \_ SAMPLE \_ CONTENT.**](media-sample-content.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Bdatypes.h (incluir Bdaiface.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[DirectShow Estructuras](directshow-structures.md)
</dt> <dt>

[**IEnumPIDMap (interfaz)**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-ienumpidmap)
</dt> </dl>

 

 




