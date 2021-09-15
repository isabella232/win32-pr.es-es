---
title: DO_DOWNLOAD_STATUS estructura
description: Se usa para obtener el estado de una descarga específica.
keywords:
- DO_DOWNLOAD_STATUS estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566776"
---
# <a name="do_download_status-structure"></a>DO_DOWNLOAD_STATUS estructura

La **DO_DOWNLOAD_STATUS** se usa para obtener el estado de una descarga específica. Se obtiene llamando a la **función IDODownload::GetStatus.**

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

## <a name="members"></a>Members

`BytesTotal`

Número total de bytes que se descargarán.

`BytesTransferred`

Número de bytes que ya se han descargado.

`State`

Estado de descarga actual definido por la **enumeración DODownloadState.**

`Error`

Información de error (si existe) asociada a la descarga actual.

`ExtendedError`

La información de error extendida (si existe) asociada a la descarga actual.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | Do.h |
