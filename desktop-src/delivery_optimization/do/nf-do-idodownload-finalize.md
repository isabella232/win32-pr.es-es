---
title: MÉTODO IDODownload::Finalize
description: Finalizará la descarga.
keywords:
- MÉTODO IDODownload::Finalize
topic_type:
- apiref
api_name:
- IDODownload.Finalize
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 620b8cf1671c18f2e4a79a798fac366d61c9e09f5a83ecda2c1ade531c6a558a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636044"
---
# <a name="idodownloadfinalize-method"></a>MÉTODO IDODownload::Finalize

Finalizará la descarga. Una vez finalizado, no se puede reanudar una descarga mediante una llamada **a Start**.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT Finalize();
```

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un [**código de**](/windows/desktop/com/structure-of-com-error-codes) error [HRESULT](/windows/desktop/com/com-error-codes-10).

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | Do.h |
