---
description: Windows Función de proxy del componente de creación de imágenes (WIC) para IEnumString::Reset.
ms.assetid: 084a3de0-c6de-4ce2-ba78-5d1bacb56cb0
title: IEnumString_Reset_WIC_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumString_Reset_WIC_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0fc06a00b5e80befe1e6a69f7c2b402597699c97bf866129ca10175e18fe34a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549625"
---
# <a name="ienumstring_reset_wic_proxy-function"></a>Función IEnumString \_ Reset \_ WIC \_ Proxy

Windows Función de proxy del componente de creación de imágenes (WIC) para IEnumString::Reset.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IEnumString_Reset_WIC_Proxy(
  _In_  IEnumString *THIS_PTR,
  _In_  ULONG       celt,
  _Out_ LPOLESTR    *rgelt,
  _Out_ ULONG       *pceltFetched
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*THIS \_ PTR* \[ en\]
</dt> <dd>

Tipo: **IEnumString \***

PARAMDESC

</dd> <dt>

*celta* \[ En\]
</dt> <dd>

Tipo: **ULONG**

</dd> <dt>

*rgelt* \[ out\]
</dt> <dd>

Tipo: **LPOLESTR \***

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Tipo: **ULONG \***

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



 

 




