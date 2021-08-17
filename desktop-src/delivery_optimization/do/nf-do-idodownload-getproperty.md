---
title: Método IDODownload::GetProperty
description: Recupera un puntero a un **variant que** contiene una propiedad de descarga específica.
keywords:
- Método IDODownload::GetProperty
topic_type:
- apiref
api_name:
- IDODownload.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: f498900e8dd2e87460a5fe4e75ea1269272788488159379d64f5332f2006f97a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736252"
---
# <a name="idodownloadgetproperty-method"></a>Método IDODownload::GetProperty

Recupera un puntero a un **variant que** contiene una propiedad de descarga específica.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT GetProperty(
  DODownloadProperty propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parámetros

`propId`

Identificador de propiedad necesario para obtener (de tipo **DODownloadProperty**).

`propVal`

Valor de propiedad resultante, almacenado en **variant.**

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un [**código de**](/windows/desktop/com/structure-of-com-error-codes) error [HRESULT](/windows/desktop/com/com-error-codes-10).

|Valor devuelto|Descripción|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* es desconocido.|
|DO_E_WRITE_ONLY_PROPERTY|La propiedad es de solo escritura y no se puede leer.|
|E_NOT_SET|No se estableció ninguna propiedad de este tipo a **través de SetProperty**.|

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | Do.h |
