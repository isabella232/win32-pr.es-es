---
title: Método IDODownloadStatusCallback::OnStatusChange
description: Optimización de distribución llama a la implementación de este método cada vez que cambia un estado de descarga.
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
ms.openlocfilehash: 6dcb30690736cb2bd2548fbd5f84cf580d317eff
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128519927"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a>Método IDODownloadStatusCallback::OnStatusChange

Optimización de distribución llama a la implementación de este método cada vez que cambia un estado de descarga.

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

Si la función se realiza correctamente, **devuelve S_OK**. De lo contrario, devuelve un [**código de**](/windows/desktop/com/structure-of-com-error-codes) error [HRESULT](/windows/desktop/com/com-error-codes-10).

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | Do.h |
