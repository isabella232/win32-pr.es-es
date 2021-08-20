---
title: Método IDODownload::GetStatus
description: Recupera un puntero a una **estructura DO_DOWNLOAD_STATUS** que refleja el estado actual de la descarga.
keywords:
- Método IDODownload::GetStatus
topic_type:
- apiref
api_name:
- IDODownload.GetStatus
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: e3a5aec5e35187a51865e074dae26ff012b75dfa3a41ffd13a8bed7371515fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047113"
---
# <a name="idodownloadgetstatus-method"></a>Método IDODownload::GetStatus

Recupera un puntero a una **estructura DO_DOWNLOAD_STATUS** que refleja el estado actual de la descarga.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT GetStatus(
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>Parámetros

`status`

Puntero a una **estructura DO_DOWNLOAD_STATUS** datos.

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un [**código de**](/windows/desktop/com/structure-of-com-error-codes) error [HRESULT](/windows/desktop/com/com-error-codes-10).

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | Do.h |
