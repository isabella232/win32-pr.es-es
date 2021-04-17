---
title: IWMDRMDevice GetSecureClock, método
description: El método GetSecureClock recupera el reloj seguro, por lo que se pueden aplicar licencias basadas en el tiempo.
ms.assetid: 6de9b7ce-9c2a-44e5-9de7-40cfbaf4d92c
keywords:
- Método GetSecureClock de Windows Media Administrador de dispositivos
- Método GetSecureClock de Windows Media Administrador de dispositivos, interfaz IWMDRMDevice
- Interfaz IWMDRMDevice de Windows Media Administrador de dispositivos, método GetSecureClock
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698512"
---
# <a name="iwmdrmdevicegetsecureclock-method"></a>IWMDRMDevice:: GetSecureClock (método)

El método **GetSecureClock** recupera el reloj seguro, por lo que se pueden aplicar licencias basadas en el tiempo.

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

*ppbSecureClock* \[ enuncia\]
</dt> <dd>

Se recuperó el reloj seguro.

</dd> <dt>

*pcbSecureClock* \[ enuncia\]
</dt> <dd>

Tamaño del reloj seguro, en bytes.

</dd> <dt>

*pdwFlags* \[ enuncia\]
</dt> <dd>

Marcas de estado de dispositivo. Este valor debe ser uno de los siguientes marcadores.



| Marca                     | Descripción                            |
|--------------------------|----------------------------------------|
| \_dispositivo \_ ISWMDRM de WMDRM   | El dispositivo es compatible con DRM de Windows Media. |
| \_dispositivo \_ NEEDCLOCK de WMDRM | El dispositivo necesita el reloj.                |
| \_dispositivo WMDRM \_ revocado   | El dispositivo se ha revocado.           |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetSecureClockChallenge**](iwmdrmdevice-getsecureclockchallenge.md)
</dt> <dt>

[**Interfaz IWMDRMDevice**](iwmdrmdevice.md)
</dt> <dt>

[**SetSecureClockResponse**](iwmdrmdevice-setsecureclockresponse.md)
</dt> </dl>

 

 





