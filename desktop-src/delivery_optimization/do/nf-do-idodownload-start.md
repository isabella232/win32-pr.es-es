---
title: Método IDODownload::Start
description: Inicia o reanuda una descarga.
keywords:
- Método IDODownload::Start
topic_type:
- apiref
api_name:
- IDODownload.Start
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: b2a06de8319ac07983fd13cb8523fa1dcf92365ca9275da80b699b290a4a6435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736262"
---
# <a name="idodownloadstart-method"></a>Método IDODownload::Start

Inicia o reanuda una descarga, pasando intervalos opcionales como puntero a [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) estructura.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT Start(
  DO_DOWNLOAD_RANGES_INFO *ranges
);
```

## <a name="parameters"></a>Parámetros

`ranges`

Opcional. Puntero a una [**estructura DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) (para descargar solo intervalos específicos del archivo). Pase `nullptr` para descargar todo el archivo.

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un [**código de**](/windows/desktop/com/structure-of-com-error-codes) error [HRESULT](/windows/desktop/com/com-error-codes-10).

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | Do.h |
