---
description: Función de proxy para el método GetDataPointer.
ms.assetid: 7256d6eb-cb7c-4067-8382-511d64da6825
title: IWICBitmapLock_GetDataPointer_STA_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetDataPointer_STA_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b693c78ba3a3d7c68c33f68ec1494997536ffb10272cc384d89d9e94ded7145b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206767"
---
# <a name="iwicbitmaplock_getdatapointer_sta_proxy-function"></a>Función proxy IWICBitmapLock \_ GetDataPointer \_ STA \_

Función de proxy para el [**método GetDataPointer.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICBitmapLock_GetDataPointer_STA_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbBufferSize,
  _Out_ BYTE           **ppbData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*THIS \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[ **IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\***

Puntero a este [**objeto IWICBitmapLock.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)

</dd> <dt>

*bufferBufferSize* \[ out\]
</dt> <dd>

Tipo: **UINT \***

Puntero que recibe el tamaño del búfer.

</dd> <dt>

*ppbData* \[ out\]
</dt> <dd>

Tipo: **\* \* BYTE**

Puntero que recibe un puntero al píxel superior izquierdo del rectángulo bloqueado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, solo Windows aplicaciones \[ de escritorio de Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




