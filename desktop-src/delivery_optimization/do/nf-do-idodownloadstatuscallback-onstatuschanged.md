---
title: 'IDODownloadStatusCallback:: OnStatusChange (método)'
description: Llama a la implementación de este método cada vez que cambia el estado de la descarga.
keywords:
- 'IDODownloadStatusCallback:: OnStatusChange (método)'
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
ms.openlocfilehash: 9abf13969a6183f98102792b9bcf7a3329ca243d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104077154"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a>IDODownloadStatusCallback:: OnStatusChange (método)

Llama a la implementación de este método cada vez que cambia el estado de la descarga.

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

Puntero a una estructura de **DO_DOWNLOAD_STATUS** que contiene el estado de la descarga.

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | Do. h |
