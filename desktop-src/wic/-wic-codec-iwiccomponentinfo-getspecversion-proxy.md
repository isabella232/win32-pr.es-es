---
description: Función de proxy para el método GetSpecVersion.
ms.assetid: 363e55c2-d6e8-4ddc-a063-c5be08232a67
title: IWICComponentInfo_GetSpecVersion_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetSpecVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a29b57e84b7cf9ceee67ac4f64ac090e697366fbe0698a891c8fbcc87e3ff5b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206588"
---
# <a name="iwiccomponentinfo_getspecversion_proxy-function"></a>Función IWICComponentInfo \_ GetSpecVersion \_ Proxy

Función de proxy para el [**método GetSpecVersion.**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICComponentInfo_GetSpecVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchSpecVersion,
  _Inout_ WCHAR             *wzSpecVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*THIS \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[ **IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\***

Puntero a este [**objeto IWICComponentInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)

</dd> <dt>

*cchSpecVersion* \[ En\]
</dt> <dd>

Tipo: **UINT**

Tamaño del búfer *wzSpecVersion.*

</dd> <dt>

*wzSpecVersion* \[ in, out\]
</dt> <dd>

Tipo: **WCHAR \***

Cuando este método devuelve un resultado, contiene una cadena invarient de referencia cultural de la versión de especificación del componente. El formulario de versión es NN.NN.NN.NN.

</dd> <dt>

*pcchActual* \[ out\]
</dt> <dd>

Tipo: **UINT \***

Puntero que recibe la longitud real de la versión de especificación del componente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, solo Windows \[ aplicaciones de escritorio de Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




