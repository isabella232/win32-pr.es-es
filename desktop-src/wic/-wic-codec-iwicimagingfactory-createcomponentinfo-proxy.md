---
description: Función de proxy para el método CreateComponentInfo.
ms.assetid: 7d3b791a-d65e-4b90-8050-373a949e6d9c
title: IWICImagingFactory_CreateComponentInfo_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateComponentInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 208b8b09b402e01f59a925f3dc6de6694b196db2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361171"
---
# <a name="iwicimagingfactory_createcomponentinfo_proxy-function"></a>IWICImagingFactory \_ CreateComponentInfo \_ función proxy

Función de proxy para el método [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICImagingFactory_CreateComponentInfo_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _In_  REFCLSID           clsidComponent,
  _Out_ IWICComponentInfo  **ppIInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFactory* \[ de\]
</dt> <dd>

Tipo: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_clsidComponent * \[ en\]
</dt> <dd>

Tipo: **REFCLSID**

CLSID del componente deseado.

</dd> <dt>

*ppIInfo* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\*\***

Puntero que recibe un puntero a un nuevo [**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




