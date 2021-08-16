---
title: Método IWMDRMDevice GetSecureClockChallenge
description: El método GetSecureClockChallenge recupera el resultado del desafío de reloj seguro.
ms.assetid: cbef160c-91a3-47d1-9d7a-e649ce2c77ff
keywords:
- Método GetSecureClockChallenge windows Media Administrador de dispositivos
- Método GetSecureClockChallenge windows Media Administrador de dispositivos , interfaz IWMDRMDevice
- IWMDRMDispositivo windows Media Administrador de dispositivos , método GetSecureClockChallenge
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClockChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaed21ddffb9c2001c3b57d32d34ac9106ede7cecaff723cb95d8cee1c428fb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957255"
---
# <a name="iwmdrmdevicegetsecureclockchallenge-method"></a>IWMDRMDevice::GetSecureClockChallenge (método)

El **método GetSecureClockChallenge** recupera el resultado del desafío de reloj seguro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSecureClockChallenge(
  [out] BYTE  **ppbChallenge,
  [out] DWORD *pcbChallenge
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppbChallenge* \[ out\]
</dt> <dd>

Resultado del desafío recuperado.

</dd> <dt>

*lugarChallenge* \[ out\]
</dt> <dd>

Tamaño del resultado del desafío, en bytes.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetSecureClock**](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[**IWMDRMDevice (interfaz)**](iwmdrmdevice.md)
</dt> </dl>

 

 





