---
description: Función de proxy para crear el IWICImagingFactory.
ms.assetid: e4f575b0-878f-461e-92e7-9494e505ea6f
title: WICCreateImagingFactory_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateImagingFactory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Windowscodecs.lib
ms.openlocfilehash: 6717764d0c25d64f99ab5d864bd0e77a63b88330
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706484"
---
# <a name="wiccreateimagingfactory_proxy-function"></a>\_Función de proxy WICCreateImagingFactory

Función de proxy para crear el [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT WICCreateImagingFactory_Proxy(
  _In_  UINT               SDKVersion,
  _Out_ IWICImagingFactory **ppIImagingFactory
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*SDKVersion* \[ de\]
</dt> <dd>

Tipo: **uint**

</dd> <dt>

*ppIImagingFactory* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función es una aplicación auxiliar para crear un generador WIC para la vinculación de DLL explícita, que era necesaria para Windows XP. En el uso normal, se usaría [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en su lugar (consulte generadores de clases de la [API de WIC](./-wic-api.md#class-factories)), ya que siempre se incluye en todas las versiones más recientes de Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>WindowsCodecs. lib</dt> </dl> |



 

