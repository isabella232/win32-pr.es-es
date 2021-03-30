---
title: 'IDODownload:: GetProperty (método)'
description: Recupera un puntero a un **valor de tipo Variant** que contiene una propiedad de descarga específica.
keywords:
- 'IDODownload:: GetProperty (método)'
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
ms.openlocfilehash: e734f109e596663ee699c764ca85f1ee45ad7947
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "103904324"
---
# <a name="idodownloadgetproperty-method"></a>IDODownload:: GetProperty (método)

Recupera un puntero a un **valor de tipo Variant** que contiene una propiedad de descarga específica.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT GetProperty(
  DODownloadProperty propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parámetros

`propId`

IDENTIFICADOR de propiedad necesario que se va a obtener (de tipo **DODownloadProperty**).

`propVal`

Valor de propiedad resultante, almacenado en una **variante**.

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

|Valor devuelto|Descripción|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|se desconoce el *propId* .|
|DO_E_WRITE_ONLY_PROPERTY|La propiedad es de solo escritura y no se puede leer.|
|E_NOT_SET|No se ha establecido esta propiedad mediante **SetProperty**.|

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | Do. h |
