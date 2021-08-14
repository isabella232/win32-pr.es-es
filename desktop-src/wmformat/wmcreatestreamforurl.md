---
title: Función WMCreateStreamForURL
description: La aplicación implementa la función WMCreateStreamForURL para crear un objeto IStream COM para una dirección URL determinada.
ms.assetid: df8d0e57-9f71-4be3-a0b0-cf61b68611bc
keywords:
- Formato multimedia de windows de la función WMCreateStreamForURL
topic_type:
- apiref
api_name:
- WMCreateStreamForURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c32302147eeb814c211a77555ab1c9bb3614eddf3d8001015479461e05d40ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653458"
---
# <a name="wmcreatestreamforurl-function"></a>Función WMCreateStreamForURL

La aplicación implementa la función **WMCreateStreamForURL** para crear un objeto **IStream** COM para una dirección URL determinada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WMCreateStreamForURL(
  _In_  LPCWSTR pwszURL,
  _Out_ BOOL    *pfCorrectSource,
  _Out_ IStream **ppStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszURL* \[ En\]
</dt> <dd>

Puntero a una cadena de caracteres anchos que contiene la dirección URL.

</dd> <dt>

*pfCorrectSource* \[ out\]
</dt> <dd>

Puntero a una marca, true impedirá que el SDK intente otros complementos de origen para esta dirección URL.

</dd> <dt>

*ppStream* \[ out\]
</dt> <dd>

Puntero a un puntero al **objeto IStream** creado por el método .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, debe devolver S \_ OK. Si se produce un error, debe devolver un código de error **HRESULT** adecuado y \* *ppStream* debe establecerse en **NULL.**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Complementos de origen**](source-plug-ins.md)
</dt> </dl>

 

 




