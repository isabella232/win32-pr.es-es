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
ms.openlocfilehash: 1e5712c9fd18e7503d477908886868784e7dc7a9f4ced7e77ab54b7d7dc71d0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119302795"
---
# <a name="pid_map-structure"></a>Estructura DE MAPA DE PID \_

La estructura contiene identifica el contenido de un identificador de paquete de flujo de transporte `PID_MAP` MPEG-2.

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

Especifica el contenido de la carga del paquete, como un tipo de [**enumeración MEDIA \_ SAMPLE \_ CONTENT.**](media-sample-content.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Bdatypes.h (incluir Bdaiface.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[DirectShow Estructuras](directshow-structures.md)
</dt> <dt>

[**IEnumPIDMap (Interfaz)**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-ienumpidmap)
</dt> </dl>

 

 




