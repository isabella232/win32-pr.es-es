---
title: Estructura de DO_DOWNLOAD_RANGE
description: Identifica un intervalo único de bytes que se va a descargar de un archivo.
keywords:
- Estructura de DO_DOWNLOAD_RANGE
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0f328565c80350a05cbfb23f178ea3580586f326
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105720111"
---
# <a name="do_download_range-structure"></a>Estructura de DO_DOWNLOAD_RANGE

La estructura **DO_DOWNLOAD_RANGE** identifica un intervalo único de bytes que se va a descargar de un archivo. La estructura de **DO_DOWNLOAD_RANGE** se incluye en **DO_DOWNLOAD_RANGES_INFO** estructura para proporcionar una matriz de intervalos que descargar.

## <a name="syntax"></a>Sintaxis
```cpp
typedef struct _DO_DOWNLOAD_RANGE
{
  UINT64 Offset;
  UINT64 Length;
} DO_DOWNLOAD_RANGE;
```

## <a name="members"></a>Miembros

`Offset`

Desplazamiento de base cero al principio del intervalo de bytes que se va a descargar de un archivo.

`Length`

Longitud del intervalo, en bytes. No especifique una longitud de cero bytes. Para indicar que el intervalo se extiende hasta el final del archivo, especifique **DO_LENGTH_TO_EOF**.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | DeliveryOptimizationDownloadTypes. h |
