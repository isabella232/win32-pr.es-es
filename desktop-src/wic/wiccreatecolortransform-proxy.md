---
description: Crea un objeto de transformación de color que implementa IWICColorTransform. Este objeto COM admite el modelo de objetos de subprocesamiento libre.
ms.assetid: 43DCC3FB-B687-45F0-AAC6-DED76214716C
title: WICCreateColorTransform_Proxy función)
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
ms.openlocfilehash: 451b549aa44e785e406f50ccf4eb7a8317edf6b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708267"
---
# <a name="wiccreatecolortransform_proxy-function"></a>\_Función de proxy WICCreateColorTransform

Crea un objeto de transformación de color que implementa [**IWICColorTransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform). Este objeto COM admite el modelo de objetos de subprocesamiento libre.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI WICCreateColorTransform_Proxy(
  _Out_  **ppIColorTransform
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppIColorTransform* \[ enuncia\]
</dt> <dd>

La transformación de color creada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-------------------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 
