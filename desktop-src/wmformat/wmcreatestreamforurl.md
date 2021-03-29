---
title: WMCreateStreamForURL función)
description: La aplicación implementa la función WMCreateStreamForURL para crear un objeto IStream COM para una dirección URL determinada.
ms.assetid: df8d0e57-9f71-4be3-a0b0-cf61b68611bc
keywords:
- Función WMCreateStreamForURL formato de Windows Media
topic_type:
- apiref
api_name:
- WMCreateStreamForURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05fddd6d5359f1eada6a2691b51a692217d4a9dd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419603"
---
# <a name="wmcreatestreamforurl-function"></a>WMCreateStreamForURL función)

La aplicación implementa la función **WMCreateStreamForURL** para crear un objeto **IStream** com para una dirección URL determinada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WMCreateStreamForURL(
  _In_  LPCWSTR pwszURL,
  _Out_ BOOL    *pfCorrectSource,
  _Out_ IStream **ppStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszURL* \[ de\]
</dt> <dd>

Puntero a una cadena de caracteres anchos que contiene la dirección URL.

</dd> <dt>

*pfCorrectSource* \[ enuncia\]
</dt> <dd>

Puntero a una marca, true impedirá que el SDK intente otros complementos de origen para esta dirección URL.

</dd> <dt>

*ppStream* \[ enuncia\]
</dt> <dd>

Puntero a un puntero al objeto **IStream** creado por el método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, debe devolver S \_ correcto. Si se produce un error, debe devolver un código de error **HRESULT** adecuado y \* *ppStream* debe establecerse en **null**.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Complementos de origen**](source-plug-ins.md)
</dt> </dl>

 

 




