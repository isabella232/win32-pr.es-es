---
title: Método IDODownload::P ause
description: Pausa la descarga.
keywords:
- Método IDODownload::P ause
topic_type:
- apiref
api_name:
- IDODownload.Pause
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: fd9598cb18790c78b32cddc04afb20e4a1a44efb111f2d562df2c6e1fe3f34fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953635"
---
# <a name="idodownloadpause-method"></a>Método IDODownload::P ause

Pausa la descarga.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT Pause();
```

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un [**código de**](/windows/desktop/com/structure-of-com-error-codes) error [HRESULT](/windows/desktop/com/com-error-codes-10).

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | Do.h |
