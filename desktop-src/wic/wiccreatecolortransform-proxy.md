---
description: Crea un objeto de transformación de color que implementa IWICColorTransform. Este objeto COM admite el modelo de objetos sin subprocesos.
ms.assetid: 43DCC3FB-B687-45F0-AAC6-DED76214716C
title: WICCreateColorTransform_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorTransform_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 89c7476bc32546f0a9fe77a8731f239702c6a2a874dbfb830b9d4bbafbd872b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709222"
---
# <a name="wiccreatecolortransform_proxy-function"></a>Función de proxy WICCreateColorTransform \_

Crea un objeto de transformación de color que implementa [**IWICColorTransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform). Este objeto COM admite el modelo de objetos sin subprocesos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI WICCreateColorTransform_Proxy(
  _Out_  **ppIColorTransform
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppIColorTransform* \[ out\]
</dt> <dd>

Transformación de color creada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 
