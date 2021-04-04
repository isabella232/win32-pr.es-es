---
title: 'IDODownload:: SetProperty (método)'
description: Establece una propiedad de descarga.
keywords:
- 'IDODownload:: SetProperty (método)'
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
ms.openlocfilehash: 0d496f49851aab665e49f3aaeb51e4b941d6c183
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "103785099"
---
# <a name="idodownloadsetproperty-method"></a>IDODownload:: SetProperty (método)

Establece una propiedad de descarga. El método acepta un puntero a una **variante** que contiene una propiedad específica que se va a aplicar a la descarga.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT SetProperty(
  DODownloadProperty propId,
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parámetros

`propId`

IDENTIFICADOR de propiedad necesario que se va a establecer (de tipo **DODownloadProperty**).

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
| **Header** | Do. h |
