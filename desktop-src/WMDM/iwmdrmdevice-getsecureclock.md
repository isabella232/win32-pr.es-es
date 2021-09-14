---
title: Método IWMDRMDevice GetSecureClock
description: El método GetSecureClock recupera el reloj seguro, por lo que se pueden aplicar licencias basadas en tiempo.
ms.assetid: 6de9b7ce-9c2a-44e5-9de7-40cfbaf4d92c
keywords:
- Método GetSecureClock windows Media Administrador de dispositivos
- Método GetSecureClock windows Media Administrador de dispositivos , interfaz IWMDRMDevice
- Interfaz IWMDRMDevice windows Media Administrador de dispositivos , método GetSecureClock
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClock
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa92c3bc2ee82facf2f2e1043e71467a0c55bd8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068508"
---
# <a name="iwmdrmdevicegetsecureclock-method"></a>IWMDRMDevice::GetSecureClock (método)

El **método GetSecureClock** recupera el reloj seguro, por lo que se pueden aplicar licencias basadas en tiempo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSecureClock(
  [out] BYTE  **ppbSecureClock,
  [out] DWORD *pcbSecureClock,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppbSecureClock* \[ out\]
</dt> <dd>

Reloj seguro recuperado.

</dd> <dt>

*pwSecureClock* \[ out\]
</dt> <dd>

Tamaño del reloj seguro, en bytes.

</dd> <dt>

*pdwFlags* \[ out\]
</dt> <dd>

Marcas de estado del dispositivo. Este valor debe ser una de las marcas siguientes.



| Marca                     | Descripción                            |
|--------------------------|----------------------------------------|
| \_ISWMDRM DE DISPOSITIVO \_ WMDRM   | El dispositivo admite Windows DRM multimedia. |
| \_NEEDCLOCK DEL DISPOSITIVO \_ WMDRM | El dispositivo necesita reloj.                |
| DISPOSITIVO WMDRM \_ \_ REVOCADO   | Se ha revocado el dispositivo.           |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**GetSecureClockChallenge**](iwmdrmdevice-getsecureclockchallenge.md)
</dt> <dt>

[**Interfaz IWMDRMDevice**](iwmdrmdevice.md)
</dt> <dt>

[**SetSecureClockResponse**](iwmdrmdevice-setsecureclockresponse.md)
</dt> </dl>

 

 





