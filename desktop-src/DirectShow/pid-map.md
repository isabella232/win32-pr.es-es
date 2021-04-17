---
description: La \_ estructura de asignación de PID contiene el contenido de un identificador de paquete de flujo de transporte MPEG-2.
ms.assetid: c247ec75-483d-4587-a82f-07bbf6d277b4
title: PID_MAP estructura (Bdatypes. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690854"
---
# <a name="pid_map-structure"></a>Estructura de asignación de PID \_

La `PID_MAP` estructura contiene identifica el contenido de un identificador de paquete de flujo de transporte MPEG-2.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  ULONG                ulPID;
  MEDIA_SAMPLE_CONTENT MediaSampleContent;
} PID_MAP;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ulPID**
</dt> <dd>

Especifica el identificador de paquete (PID)

</dd> <dt>

**MediaSampleContent**
</dt> <dd>

Especifica el contenido de la carga de paquete, como un tipo de enumeración de [**\_ \_ contenido de ejemplo multimedia**](media-sample-content.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Bdatypes. h (incluye Bdaiface. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de DirectShow](directshow-structures.md)
</dt> <dt>

[**Interfaz IEnumPIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-ienumpidmap)
</dt> </dl>

 

 




