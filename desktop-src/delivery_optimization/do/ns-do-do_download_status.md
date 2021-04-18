---
title: Estructura de DO_DOWNLOAD_STATUS
description: Se usa para obtener el estado de una descarga específica.
keywords:
- Estructura de DO_DOWNLOAD_STATUS
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_STATUS
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5e113bb4866ef1033886dbb1579d21aa296d0e5e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105720101"
---
# <a name="do_download_status-structure"></a>Estructura de DO_DOWNLOAD_STATUS

La estructura de **DO_DOWNLOAD_STATUS** se utiliza para obtener el estado de una descarga específica. Se obtiene mediante una llamada a la función **IDODownload:: getStatus** .

## <a name="syntax"></a>Sintaxis
```cpp
typedef struct _DO_DOWNLOAD_STATUS
{
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  DODownloadState State;
  HRESULT Error;
  HRESULT ExtendedError;
} DO_DOWNLOAD_STATUS;
```

## <a name="members"></a>Miembros

`BytesTotal`

Número total de bytes que se van a descargar.

`BytesTransferred`

Número de bytes que ya se han descargado.

`State`

Estado de descarga actual tal y como se define en la enumeración **DODownloadState** .

`Error`

La información de error (si existe) que está asociada a la descarga actual.

`ExtendedError`

La información de error extendida (si existe) que está asociada a la descarga actual.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | Do. h |
