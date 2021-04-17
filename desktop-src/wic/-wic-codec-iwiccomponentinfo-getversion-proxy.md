---
description: Función de proxy para el método GetVersion.
ms.assetid: b064b065-bc02-4943-b208-ce5e40c12aa2
title: IWICComponentInfo_GetVersion_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: bad3677068802861bce9c0c7d0c1b03e5d06d0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717214"
---
# <a name="iwiccomponentinfo_getversion_proxy-function"></a>IWICComponentInfo \_ GetVersion \_ proxy (función)

Función de proxy para el método [**GetVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICComponentInfo_GetVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchVersion,
  _Inout_ WCHAR             *wzVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Este \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _

Puntero a este objeto [_ *IWICComponentInfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .

</dd> <dt>

*cchVersion* \[ de\]
</dt> <dd>

Tipo: **uint**

Tamaño del búfer de *wzVersion* .

</dd> <dt>

*wzVersion* \[ in, out\]
</dt> <dd>

Tipo: **WCHAR \** _

Puntero que recibe una cadena de referencia cultural invariable de la versión del componente.

</dd> <dt>

_pcchActual * \[ out\]
</dt> <dd>

Tipo: **uint \** _

Puntero que recibe la longitud real de la versión del componente.

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



 

 




