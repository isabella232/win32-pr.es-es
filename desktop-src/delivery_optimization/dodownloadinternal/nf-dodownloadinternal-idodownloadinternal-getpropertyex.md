---
title: 'IDODownloadInternal:: GetPropertyEx (método)'
description: Recupera un puntero a una **variante** que contiene un valor de propiedad de descarga extendida específico.
keywords:
- 'IDODownloadInternal:: GetPropertyEx (método)'
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
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420974"
---
# <a name="idodownloadinternalgetpropertyex-method"></a>IDODownloadInternal:: GetPropertyEx (método)

> [!IMPORTANT]
> La interfaz **IDODownloadInternal** está en desuso. En su lugar, use la interfaz [IDODownload](../do/nn-do-idodownload.md) .

Recupera un puntero a una **variante** que contiene un valor de propiedad de descarga extendida específico.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT GetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parámetros

`propId`

IDENTIFICADOR de propiedad necesario que se va a obtener (de tipo **DODownloadPropertyEx**).

`propVal`

Valor de propiedad resultante, almacenado en una **variante**.

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

|Valor devuelto|Descripción|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|se desconoce el *propId* .|
|DO_E_WRITE_ONLY_PROPERTY|La propiedad es de solo escritura y no se puede leer.|
|E_NOT_SET|No se estableció esta propiedad a través de **SetPropertyEx**.|

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | DODownloadInternal. h |