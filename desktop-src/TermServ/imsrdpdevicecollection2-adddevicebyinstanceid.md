---
title: Método IMsRdpDeviceCollection2 AddDeviceByInstanceId
description: Agrega un dispositivo no publicado a la recopilación de dispositivos.
ms.assetid: 7ef200c5-b99e-40c9-80e1-0758ddfa0902
ms.tgt_platform: multiple
keywords:
- Método AddDeviceByInstanceId Servicios de Escritorio remoto
- Método AddDeviceByInstanceId Servicios de Escritorio remoto , interfaz IMsRdpDeviceCollection2
- Interfaz IMsRdpDeviceCollection2 Servicios de Escritorio remoto , método AddDeviceByInstanceId
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.AddDeviceByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df11fa2a58aca505661da1f7643f8d1d6ff2f502e6c10bf835aa67a6e2d0615d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870825"
---
# <a name="imsrdpdevicecollection2adddevicebyinstanceid-method"></a>Método IMsRdpDeviceCollection2::AddDeviceByInstanceId

Agrega un dispositivo no publicado a la recopilación de dispositivos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddDeviceByInstanceId(
  [in] RedirectDeviceType Type,
  [in] BSTR               InstanceId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tipo* \[ En\]
</dt> <dd>

Tipo: **[ **RedirectDeviceType**](redirectdevicetype.md)**

Valor de la [**enumeración RedirectDeviceType**](redirectdevicetype.md) que especifica el tipo de dispositivo que se va a agregar.

</dd> <dt>

*InstanceId* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Identificador de instancia del dispositivo que se agregará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RedirectDeviceType**](redirectdevicetype.md)
</dt> <dt>

[**IMsRdpDeviceCollection2**](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





