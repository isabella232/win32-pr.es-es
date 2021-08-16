---
description: Función de proxy para el método GetAuthor.
ms.assetid: fb76009e-cc01-4dec-9403-04bf6b53db80
title: IWICComponentInfo_GetAuthor_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetAuthor_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c83d42f499c8f821f5b342f08749a2167aac9cc61334fe2fc2d9e9134b5e2b49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206676"
---
# <a name="iwiccomponentinfo_getauthor_proxy-function"></a>Función IWICComponentInfo \_ GetAuthor \_ Proxy

Función de proxy para el [**método GetAuthor.**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getauthor)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICComponentInfo_GetAuthor_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchAuthor,
  _Inout_ WCHAR             *wzAuthor,
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

*cchAuthor* \[ En\]
</dt> <dd>

Tipo: **UINT**

Tamaño del búfer *wzAuthor.*

</dd> <dt>

*wzAuthor* \[ in, out\]
</dt> <dd>

Tipo: **WCHAR \***

Puntero que recibe el nombre del autor del componente.

La cadena devuelta es específica de la configuración regional, 1033 de forma predeterminada.

</dd> <dt>

*pcchActual* \[ out\]
</dt> <dd>

Tipo: **UINT \***

Puntero que recibe la longitud real del nombre de los autores del componente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, solo Windows de \[ escritorio de Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




