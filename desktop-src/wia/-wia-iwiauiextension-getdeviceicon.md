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
ms.openlocfilehash: 9bfa8e87736412822c1a70f75b129aeec30af20e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116663"
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

Especifica el tamaño del icono deseado, en píxeles. Se supone que el icono es cuadrado y nSize especifica el ancho y el alto del icono solicitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 




