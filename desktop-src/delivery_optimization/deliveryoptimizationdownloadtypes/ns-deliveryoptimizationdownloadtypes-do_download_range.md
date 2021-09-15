---
title: DO_DOWNLOAD_RANGE estructura
description: Identifica un único intervalo de bytes que se van a descargar de un archivo.
keywords:
- DO_DOWNLOAD_RANGE estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566784"
---
# <a name="do_download_range-structure"></a>DO_DOWNLOAD_RANGE estructura

La **DO_DOWNLOAD_RANGE** estructura identifica un único intervalo de bytes para descargar de un archivo. La **DO_DOWNLOAD_RANGE** se incluye dentro **de DO_DOWNLOAD_RANGES_INFO** estructura para proporcionar una matriz de intervalos para descargar.

## <a name="syntax"></a>Sintaxis
```cpp
typedef struct _DO_DOWNLOAD_RANGE
{
  UINT64 Offset;
  UINT64 Length;
} DO_DOWNLOAD_RANGE;
```

## <a name="members"></a>Members

`Offset`

Desplazamiento de base cero al principio del intervalo de bytes que se va a descargar de un archivo.

`Length`

Longitud del intervalo, en bytes. No especifique una longitud de cero bytes. Para indicar que el intervalo se extiende hasta el final del archivo, especifique **DO_LENGTH_TO_EOF**.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | DeliveryOptimizationDownloadTypes.h |
