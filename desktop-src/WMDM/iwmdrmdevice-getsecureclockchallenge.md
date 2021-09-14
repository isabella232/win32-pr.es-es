---
title: Método IWMDRMDevice GetSecureClockChallenge
description: El método GetSecureClockChallenge recupera el resultado del desafío de reloj seguro.
ms.assetid: cbef160c-91a3-47d1-9d7a-e649ce2c77ff
keywords:
- Método GetSecureClockChallenge windows Media Administrador de dispositivos
- Método GetSecureClockChallenge windows Media Administrador de dispositivos interfaz , IWMDRMDevice
- Interfaz IWMDRMDevice windows Media Administrador de dispositivos , método GetSecureClockChallenge
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
ms.openlocfilehash: d7e57165f75a23d13d847e028deb69de383e2855
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967840"
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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**GetSecureClock**](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[**IWMDRMDevice (interfaz)**](iwmdrmdevice.md)
</dt> </dl>

 

 





