---
description: 'Función de proxy de Windows Imaging Component (WIC) para IPropertyBag2:: Write.'
ms.assetid: b97caba6-298a-4b36-9f39-9b5440b866c3
title: IPropertyBag2_Write_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertyBag2_Write_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c868ee748c3c2894daa63850284ae121f85975fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360249"
---
# <a name="ipropertybag2_write_proxy-function"></a>IPropertyBag2 \_ escribir \_ función de proxy

Función de proxy de Windows Imaging Component (WIC) para IPropertyBag2:: Write.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IPropertyBag2_Write_Proxy(
  _In_ IPropertyBag2 *THIS_PTR,
  _In_ ULONG         cProperties,
  _In_ PROPBAG2      *ppropBag,
  _In_ VARIANT       *pvarValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Este \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) \** _

PARAMDESC

</dd> <dt>

_cProperties * \[ en\]
</dt> <dd>

Tipo: **ULong**

</dd> <dt>

*ppropBag* \[ de\]
</dt> <dd>

Tipo: **[PROPBAG2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85)) \** _

</dd> <dt>

_pvarValue * \[ en\]
</dt> <dd>

Tipo: **variante \** _

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



 

