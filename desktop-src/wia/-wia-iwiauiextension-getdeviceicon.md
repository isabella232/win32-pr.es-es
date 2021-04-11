---
description: Obtiene un icono de dispositivo personalizado.
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: 'IWiaUIExtension:: GetDeviceIcon (método) (Wiadevd. h)'
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
ms.openlocfilehash: 36b61a25de1acb9b84ce68dc897514e0d4612a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154391"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a>IWiaUIExtension:: GetDeviceIcon (método)

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

*bstrDeviceId* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Especifica el identificador del dispositivo WIA para el que se va a obtener el icono.

</dd> <dt>

*phIcon* \[ enuncia\]
</dt> <dd>

Tipo: **HICON \** _

Apunta a una ubicación de memoria que recibirá un identificador para el icono del dispositivo.

</dd> <dt>

_nSize * \[ en\]
</dt> <dd>

Tipo: **ULong**

Especifica el tamaño de icono deseado, en píxeles. Se supone que el icono es cuadrado y nSize especifica el ancho y el alto del icono solicitado.

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



 

 




