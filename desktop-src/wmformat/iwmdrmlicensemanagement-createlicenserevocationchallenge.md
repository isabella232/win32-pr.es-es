---
title: Método IWMDRMLicenseManagement CreateLicenseRevocationChallenge (Wmdrmsdk.h)
description: El método CreateLicenseRevocationChallenge genera un desafío de revocación de licencias.
ms.assetid: 31fcf7a7-1af8-4474-abac-eddb1070975b
keywords:
- Método CreateLicenseRevocationChallenge windows Media Format
- Método CreateLicenseRevocationChallenge formato multimedia de windows, interfaz IWMDRMLicenseManagement
- IWMDRMLicenseManagement interface windows Media Format , CreateLicenseRevocationChallenge method
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseRevocationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851233229d7dde113cf21cfb38419067679843b34ae59ece0e32e326c2a91c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846963"
---
# <a name="iwmdrmlicensemanagementcreatelicenserevocationchallenge-method"></a>IWMDRMLicenseManagement::CreateLicenseRevocationChallenge (método)

El **método CreateLicenseRevocationChallenge** genera un desafío de revocación de licencias.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateLicenseRevocationChallenge(
  [in]  BYTE  *pbMachineID,
  [in]  DWORD cbMachineID,
  [in]  BYTE  *pbChallenge,
  [in]  DWORD cbChallenge,
  [out] BYTE  **ppbChallengeOutput,
  [out] DWORD *pcbChallengeOutput
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbMachineID* \[ En\]
</dt> <dd>

Identificador de máquina especificado por el usuario. Este valor se usa para consultar una licencia en el servidor y debe ajustarse al formato que use el servidor de licencias.

</dd> <dt>

*cbMachineID* \[ En\]
</dt> <dd>

Tamaño, en bytes, del identificador de la máquina.

</dd> <dt>

*pbChallenge* \[ En\]
</dt> <dd>

Datos de desafío especificados por el usuario. Estos datos, además del identificador de la máquina, se usan para consultar al servidor de licencias las licencias que se deben revocar.

</dd> <dt>

*cbChallenge* \[ En\]
</dt> <dd>

Tamaño, en bytes, de los datos de desafío.

</dd> <dt>

*ppbChallengeOutput* \[ out\]
</dt> <dd>

Dirección de un puntero que recibe la dirección de la salida del desafío. Este búfer son los datos que se envían al servicio de revocación de licencias. Cuando termine con estos datos, debe liberar la memoria mediante una llamada **a CoTaskMemFree**.

</dd> <dt>

*pwChallengeOutput* \[ out\]
</dt> <dd>

Dirección de una variable que recibe el tamaño de los datos de salida de desafío asignados, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMLicenseManagement (interfaz)**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





