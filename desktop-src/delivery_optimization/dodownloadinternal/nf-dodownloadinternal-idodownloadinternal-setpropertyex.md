---
title: 'IDODownloadInternal:: SetPropertyEx (método)'
description: Establece una propiedad de descarga extendida. El método acepta un puntero a una **variante** que contiene un valor de propiedad específico que se va a aplicar a la descarga.
keywords:
- 'IDODownloadInternal:: SetPropertyEx (método)'
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
ms.openlocfilehash: e6630cc3e767531dd94da39fe73d88284c9ca0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995304"
---
# <a name="idodownloadinternalsetpropertyex-method"></a>IDODownloadInternal:: SetPropertyEx (método)

> [!IMPORTANT]
> La interfaz **IDODownloadInternal** está en desuso. En su lugar, use la interfaz [IDODownload](../do/nn-do-idodownload.md) .

Establece una propiedad de descarga extendida. El método acepta un puntero a una **variante** que contiene un valor de propiedad específico que se va a aplicar a la descarga.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT SetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parámetros

`propId`

IDENTIFICADOR de propiedad necesario que se va a establecer (de tipo **DODownloadPropertyEx**).

`propVal`

Valor de propiedad que se va a establecer, almacenado en una **variante**.

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

|Valor devuelto|Descripción|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|se desconoce el *propId* .|
|DO_E_INVALID_STATE|La descarga no está actualmente en un estado que permita establecer propiedades.|

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | DODownloadInternal. h |