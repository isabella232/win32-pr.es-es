---
description: Función de proxy para el método CopyPixels.
ms.assetid: 020c11e9-0847-468e-b240-20529f6460cd
title: IWICBitmapSource_CopyPixels_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPixels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5c759bd1731e2f3cbc4da9c40cb590e0f39686de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278473"
---
# <a name="iwicbitmapsource_copypixels_proxy-function"></a>Función de proxy de IWICBitmapSource \_ copyPixels \_

Función de proxy para el método [**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICBitmapSource_CopyPixels_Proxy(
  _In_        IWICBitmapSource *THIS_PTR,
  _In_  const WICRect          *prc,
  _In_        UINT             cbStride,
  _In_        UINT             cbBufferSize,
  _Out_       BYTE             *pbBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Este \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Puntero a este objeto [_ *IWICBitmapSource* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .

</dd> <dt>

*PRC* \[ de\]
</dt> <dd>

Tipo: **const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _

Rectángulo que se va a copiar. Un valor NULL especifica el mapa de bits completo.

</dd> <dt>

_cbStride * \[ en\]
</dt> <dd>

Tipo: **uint**

El intervalo del mapa de bits.

</dd> <dt>

*cbBufferSize* \[ de\]
</dt> <dd>

Tipo: **uint**

Tamaño del búfer.

</dd> <dt>

*pbBuffer* \[ enuncia\]
</dt> <dd>

Tipo: **byte \** _

Puntero al búfer.

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



 

 




