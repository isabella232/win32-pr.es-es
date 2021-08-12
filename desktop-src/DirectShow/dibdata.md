---
description: La estructura DIBDATA contiene información sobre un mapa de bits independiente del dispositivo (DIB) de GDI.
ms.assetid: abbfa5b4-8789-4a44-a467-5812d3cc8238
title: Estructura DIBDATA (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIBDATA
api_type:
- HeaderDef
api_location:
- Winutil.h
ms.openlocfilehash: b4449f45afac56b202e9b23516dc849c6364e8781be7cfbe7cfb2b630bd16921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653831"
---
# <a name="dibdata-structure"></a>DIBDATA (estructura)

La estructura contiene información sobre un mapa de bits independiente del `DIBDATA` dispositivo GDI (DIB).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagDIBDATA {
  LONG       PaletteVersion;
  DIBSECTION DibSection;
  HBITMAP    hBitmap;
  HANDLE     hMapping;
  BYTE       *pBase;
} DIBDATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**PaletteVersion**
</dt> <dd>

Este miembro debe incrementarse cada vez que cambie la paleta.

</dd> <dt>

**DibSection**
</dt> <dd>

**Estructura DIBSECTION** que contiene información sobre la DIB. Consulte la documentación de GDI para obtener más información.

</dd> <dt>

**hBitmap**
</dt> <dd>

Identificador del mapa de bits.

</dd> <dt>

**hMapping**
</dt> <dd>

Identificador de un objeto de asignación de archivos que se usa para compartir memoria entre GDI y [**un objeto CImageSample.**](cimagesample.md)

</dd> <dt>

**pBase**
</dt> <dd>

Dirección del mapa de bits.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl> |



 

 




