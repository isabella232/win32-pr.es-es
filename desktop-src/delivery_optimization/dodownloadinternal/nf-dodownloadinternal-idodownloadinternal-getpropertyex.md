---
title: Método IDODownloadInternal::GetPropertyEx
description: Recupera un puntero a variant **que** contiene un valor de propiedad de descarga extendido específico.
keywords:
- Método IDODownloadInternal::GetPropertyEx
topic_type:
- apiref
api_name:
- IDODownloadInternal.GetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 908f9b15df5c0c4a2769149419ff12d545201e5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965127"
---
# <a name="idodownloadinternalgetpropertyex-method"></a>Método IDODownloadInternal::GetPropertyEx

> [!IMPORTANT]
> La **interfaz IDODownloadInternal** está en desuso. En su lugar, use [la interfaz IDODownload.](../do/nn-do-idodownload.md)

Recupera un puntero a variant **que** contiene un valor de propiedad de descarga extendido específico.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT GetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parámetros

`propId`

Identificador de propiedad necesario para obtener (de tipo **DODownloadPropertyEx**).

`propVal`

Valor de propiedad resultante, almacenado en **variant.**

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un [**código de**](/windows/desktop/com/structure-of-com-error-codes) error [HRESULT](/windows/desktop/com/com-error-codes-10).

|Valor devuelto|Descripción|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* es desconocido.|
|DO_E_WRITE_ONLY_PROPERTY|La propiedad es de solo escritura y no se puede leer.|
|E_NOT_SET|No se estableció dicha propiedad a través **de SetPropertyEx**.|

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | DODownloadInternal.h |