---
title: Método IDODownloadInternal::SetPropertyEx
description: Establece una propiedad de descarga extendida. El método acepta un puntero a **un variant** que contiene un valor de propiedad específico que se aplicará a la descarga.
keywords:
- Método IDODownloadInternal::SetPropertyEx
topic_type:
- apiref
api_name:
- IDODownloadInternal.SetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: d6156f4309c0eac9d2d250c85f7e9ab365e4a3b1e4072aabec7f6aa7e17c437f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858805"
---
# <a name="idodownloadinternalsetpropertyex-method"></a>Método IDODownloadInternal::SetPropertyEx

> [!IMPORTANT]
> La **interfaz IDODownloadInternal** está en desuso. En su lugar, use [la interfaz IDODownload.](../do/nn-do-idodownload.md)

Establece una propiedad de descarga extendida. El método acepta un puntero a **un variant** que contiene un valor de propiedad específico que se aplicará a la descarga.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT SetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parámetros

`propId`

Identificador de propiedad necesario que se debe establecer (de tipo **DODownloadPropertyEx).**

`propVal`

Valor de propiedad que se debe establecer, almacenado en **variant.**

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un [**código de**](/windows/desktop/com/structure-of-com-error-codes) error [HRESULT](/windows/desktop/com/com-error-codes-10).

|Valor devuelto|Descripción|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* es desconocido.|
|DO_E_INVALID_STATE|La descarga no está actualmente en un estado que permita establecer propiedades.|

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | DODownloadInternal.h |