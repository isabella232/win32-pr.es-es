---
description: 'Método IWiaUIExtension::GetDeviceIcon: obtiene un icono de dispositivo personalizado.'
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: Método IWiaUIExtension::GetDeviceIcon (Wiadevd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 040bcc6bcc5e4e8a7126c5ef7d0a72dbb688a6e5605512ff67527c21bfaa3026
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813865"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a>IWiaUIExtension::GetDeviceIcon (método)

Obtiene un icono de dispositivo personalizado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrDeviceId* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Especifica el identificador de dispositivo del dispositivo WIA para el que se va a obtener el icono.

</dd> <dt>

*phIcon* \[ out\]
</dt> <dd>

Tipo: **HICON \***

Apunta a una ubicación de memoria que recibirá un identificador para el icono del dispositivo.

</dd> <dt>

*nSize* \[ En\]
</dt> <dd>

Tipo: **ULONG**

Especifica el tamaño de icono deseado, en píxeles. Se supone que el icono es cuadrado y nSize especifica el ancho y el alto del icono solicitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 




