---
title: Estructura de DO_DOWNLOAD_RANGE_INFO
description: Identifica una matriz de intervalos de bytes que se van a descargar de un archivo.
keywords:
- Estructura de DO_DOWNLOAD_RANGE_INFO
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE_INFO
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 01628ea29895012f60552e696b7f68854f426f8d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104420041"
---
# <a name="do_download_range_info-structure"></a>Estructura de DO_DOWNLOAD_RANGE_INFO

La estructura **DO_DOWNLOAD_RANGE_INFO** identifica una matriz de intervalos de bytes que se van a descargar de un archivo. Normalmente se pasa como argumento opcional a la función **IDODownload:: Start** .

## <a name="syntax"></a>Sintaxis
```cpp
typedef struct _DO_DOWNLOAD_RANGES_INFO
{
  UINT RangeCount;
  [size_is(RangeCount)] DO_DOWNLOAD_RANGE Ranges[];
} DO_DOWNLOAD_RANGES_INFO;
```

## <a name="members"></a>Miembros

`RangeCount`

Número de elementos de intervalos.

`Ranges`

Matriz de una o varias estructuras de **DO_DOWNLOAD_RANGE** que especifican los intervalos que se van a descargar.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | Do. h |
