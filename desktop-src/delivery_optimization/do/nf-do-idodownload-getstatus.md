---
title: 'IDODownload:: GetStatus (método)'
description: Recupera un puntero a una estructura de **DO_DOWNLOAD_STATUS** que refleja el estado actual de la descarga.
keywords:
- 'IDODownload:: GetStatus (método)'
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
ms.openlocfilehash: 8b9b2603354bbb5345cf866ee0c94785a254952d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104420045"
---
# <a name="idodownloadgetstatus-method"></a>IDODownload:: GetStatus (método)

Recupera un puntero a una estructura de **DO_DOWNLOAD_STATUS** que refleja el estado actual de la descarga.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT GetStatus(
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>Parámetros

`status`

Puntero a una estructura de **DO_DOWNLOAD_STATUS** .

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | Do. h |
