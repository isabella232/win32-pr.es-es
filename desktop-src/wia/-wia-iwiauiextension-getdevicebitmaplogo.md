---
description: Obtiene un logotipo de mapa de bits personalizado para el dispositivo.
ms.assetid: 56b3c7c9-64f4-4853-9eb7-d876d02a851f
title: 'IWiaUIExtension:: GetDeviceBitmapLogo (método) (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceBitmapLogo
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 51db237c93a2167eb3c4bdae648f9d79da13319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696516"
---
# <a name="iwiauiextensiongetdevicebitmaplogo-method"></a>IWiaUIExtension:: GetDeviceBitmapLogo (método)

Obtiene un logotipo de mapa de bits personalizado para el dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDeviceBitmapLogo(
  [in]  BSTR    bstrDeviceId,
  [out] HBITMAP *phBitmap,
  [in]  ULONG   nMaxWidth,
  [in]  ULONG   nMaxHeight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrDeviceId* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Especifica el identificador del dispositivo WIA para el que se va a obtener el icono.

</dd> <dt>

*phBitmap* \[ enuncia\]
</dt> <dd>

Tipo: **hBitmap \** _

Apunta a una ubicación de memoria que recibirá un identificador para el logotipo de mapa de bits para el dispositivo.

</dd> <dt>

_nMaxWidth * \[ en\]
</dt> <dd>

Tipo: **ULong**

Especifica el ancho deseado del mapa de bits.

</dd> <dt>

*nMaxHeight* \[ de\]
</dt> <dd>

Tipo: **ULong**

Especifica el alto deseado del mapa de bits.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




