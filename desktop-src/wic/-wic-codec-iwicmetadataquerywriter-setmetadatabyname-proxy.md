---
description: Función de proxy para el método SetMetadataByName.
ms.assetid: 467d7735-152a-4e7c-93b1-fd031cc57c19
title: IWICMetadataQueryWriter_SetMetadataByName_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryWriter_SetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e27ea57ec5b26fd2bed04ea99f6c6cbfb11c8874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716663"
---
# <a name="iwicmetadataquerywriter_setmetadatabyname_proxy-function"></a>IWICMetadataQueryWriter \_ SetMetadataByName \_ función proxy

Función de proxy para el método [**SetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-setmetadatabyname) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICMetadataQueryWriter_SetMetadataByName_Proxy(
  _In_       IWICMetadataQueryWriter *THIS_PTR,
  _In_       LPCWSTR                 wzName,
  _In_ const PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Este \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) \** _

Puntero a este objeto [_ *IWICMetadataQueryWriter* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .

</dd> <dt>

*wzName* \[ de\]
</dt> <dd>

Tipo: **LPCWSTR**

Nombre del elemento de metadatos.

</dd> <dt>

*pvarValue* \[ de\]
</dt> <dd>

Tipo: **const [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _

Los metadatos que se van a establecer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

