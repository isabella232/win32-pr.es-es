---
title: 'IDODownload:: Finalize (método)'
description: Finaliza la descarga.
keywords:
- 'IDODownload:: Finalize (método)'
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
ms.openlocfilehash: 6befc9a7e64fb0963d45257d68d6bb8d2ba7a2cb
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105720107"
---
# <a name="idodownloadfinalize-method"></a>IDODownload:: Finalize (método)

Finaliza la descarga. Una vez finalizada, una descarga no se puede reanudar mediante una llamada a **Start**.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT Finalize();
```

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | Do. h |
