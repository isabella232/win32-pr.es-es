---
title: Método IDODownloadStatusCallback::OnStatusChange
description: DO llama a la implementación de este método cada vez que cambia un estado de descarga.
keywords:
- Método IDODownloadStatusCallback::OnStatusChange
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback.OnStatusChange
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0395b6bc64ad3abe102a0a4f0dc7afd8e8d59f336949a3b97eaf683a4f4900cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736231"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a>Método IDODownloadStatusCallback::OnStatusChange

DO llama a la implementación de este método cada vez que cambia un estado de descarga.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT OnStatusChange(
  IDODownload *download,
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>Parámetros

`download`

Puntero a la interfaz **IDODownload** cuyo estado ha cambiado.

`status`

Puntero a una **DO_DOWNLOAD_STATUS** estructura que contiene el estado de la descarga.

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un [**código de**](/windows/desktop/com/structure-of-com-error-codes) error [HRESULT](/windows/desktop/com/com-error-codes-10).

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | Do.h |
