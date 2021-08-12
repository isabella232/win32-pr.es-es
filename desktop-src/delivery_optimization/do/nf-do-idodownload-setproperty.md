---
title: Método IDODownload::SetProperty
description: Establece una propiedad de descarga.
keywords:
- Método IDODownload::SetProperty
topic_type:
- apiref
api_name:
- IDODownload.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a7d966edb083107b80f0723bce195bfc588797efb8ad1931e0e75a468bec5a3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543904"
---
# <a name="idodownloadsetproperty-method"></a>Método IDODownload::SetProperty

Establece una propiedad de descarga. El método acepta un puntero a **un variant** que contiene una propiedad específica que se aplicará a la descarga.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT SetProperty(
  DODownloadProperty propId,
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parámetros

`propId`

Identificador de propiedad necesario que se debe establecer (de tipo **DODownloadProperty**).

`propVal`

Valor de propiedad que se establece, almacenado en **variant.**

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
| **Header** | Do.h |
