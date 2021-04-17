---
description: La estructura DIBDATA contiene información sobre un mapa de bits independiente del dispositivo GDI (DIB).
ms.assetid: abbfa5b4-8789-4a44-a467-5812d3cc8238
title: Estructura DIBDATA (Winutil. h)
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
ms.openlocfilehash: 87590013ef905ffbdd13dd3b767435a907b08783
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680688"
---
# <a name="dibdata-structure"></a>Estructura DIBDATA

La `DIBDATA` estructura contiene información sobre un mapa de bits independiente del dispositivo GDI (DIB).

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

Estructura **DIBSECTION** que contiene información sobre el Dib. Consulte la documentación de GDI para obtener más información.

</dd> <dt>

**hBitmap**
</dt> <dd>

Identificador del mapa de bits.

</dd> <dt>

**hMapping**
</dt> <dd>

Identificador de un objeto de asignación de archivos que se utiliza para compartir la memoria entre GDI y un objeto [**CImageSample**](cimagesample.md) .

</dd> <dt>

**pBase**
</dt> <dd>

Dirección del mapa de bits.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl> |



 

 




