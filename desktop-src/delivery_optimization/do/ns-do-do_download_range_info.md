---
title: DO_DOWNLOAD_RANGE_INFO estructura
description: Identifica una matriz de intervalos de bytes que se van a descargar de un archivo.
keywords:
- DO_DOWNLOAD_RANGE_INFO estructura
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
ms.openlocfilehash: 30df22c7232ad1d28315e8152396ddd92bdab9a7cbf67d748af134c0f0760c33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543749"
---
# <a name="do_download_range_info-structure"></a>DO_DOWNLOAD_RANGE_INFO estructura

La **DO_DOWNLOAD_RANGE_INFO** identifica una matriz de intervalos de bytes que se van a descargar de un archivo. Normalmente se pasa como argumento opcional a la **función IDODownload::Start.**

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

Número de elementos en Intervalos.

`Ranges`

Matriz de una o **varias estructuras DO_DOWNLOAD_RANGE** que especifican los intervalos que se van a descargar.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | Do.h |
