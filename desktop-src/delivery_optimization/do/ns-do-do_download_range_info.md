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
ms.openlocfilehash: 01628ea29895012f60552e696b7f68854f426f8d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566777"
---
# <a name="do_download_range_info-structure"></a>DO_DOWNLOAD_RANGE_INFO estructura

La **DO_DOWNLOAD_RANGE_INFO** estructura identifica una matriz de intervalos de bytes que se van a descargar de un archivo. Normalmente se pasa como argumento opcional a la **función IDODownload::Start.**

## <a name="syntax"></a>Sintaxis
```cpp
typedef struct _DO_DOWNLOAD_RANGES_INFO
{
  UINT RangeCount;
  [size_is(RangeCount)] DO_DOWNLOAD_RANGE Ranges[];
} DO_DOWNLOAD_RANGES_INFO;
```

## <a name="members"></a>Members

`RangeCount`

Número de elementos en intervalos.

`Ranges`

Matriz de una o **varias estructuras DO_DOWNLOAD_RANGE** que especifican los intervalos que se van a descargar.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | Do.h |
